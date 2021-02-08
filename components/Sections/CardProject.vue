<template>
  <div>
    <div
      class="card shadow mb-5 bg-white rounded"
      style="width: 80%; text-align: center"
    >
      <a :href="projectInfo.siteUrl" v-if="projectInfo.image != ''" >
        <img class="card-img-top" :src="projectInfo.image" :alt="projectInfo.name"
      /></a>
      <div class="card-body">
        <h5 class="card-title">
          <a :href="projectInfo.nameUrl">{{ projectInfo.name }}</a>
		</h5>
        <p class="card-text">
          {{ projectInfo.description }}
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["projectInfo"],
  data() {
    return {};
  }
};
</script>

<style>
.card {
  border: none;
}
</style>
