<template>
  <div class="my-auto">
    <h2 class="mb-5">{{ $t('workExperiences.title') }}</h2>

    <div
      v-for="work in $t('workExperiences.works')"
      :key="work.title"
      class="resume-item d-flex flex-column flex-md-row mb-5"
    >
      <div class="resume-content mr-auto">
        <h3 class="mb-0">{{ work.position }}</h3>
        <a :href="work.url" class="subheading mb-3">{{ work.companie }}</a>
        <p
          v-for="responsabilitie in work.responsabilities"
          :key="responsabilitie"
        >
          - {{ responsabilitie }}
        </p>
      </div>
	  <div class="my-auto align-space-between text-md-right">
        <div class="resume-date text-md-right">
          <span class="text-primary">{{ work.startEndDate }}</span>
        </div>

		<ul class="fa-ul mb-0">
          <li v-for="icon in work.devIcons" :key="icon" style="font-size: 2rem;">
            <i :class="icon"></i>
          </li>
	    </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return { };
  }
};
</script>
