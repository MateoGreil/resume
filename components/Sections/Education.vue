<template>
  <div class="my-auto">
    <h2 class="mb-5">{{ $t("educationDegrees.title") }}</h2>

    <div
      v-for="degree in $t('educationDegrees.degrees')"
      :key="degree.name"
      class="resume-item d-flex flex-column flex-md-row mb-5"
    >
      <div class="resume-content mr-auto">
        <h3 class="mb-0">{{ degree.collage }}</h3>
        <div class="subheading mb-3">{{ degree.name }}</div>
        <div v-for="item in degree.itemList" :key="item">{{ item }}</div>
      </div>
	  <div class="my-auto align-space-between text-md-right">
        <div class="resume-date mb-3">
          <span class="text-primary">{{ degree.startEndDate }}</span>
        </div>
        <img class="mt-3" :src="degree.imageUrl" :alt="degree.collage + Image" width="auto" height="100vh">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  }
};
</script>
