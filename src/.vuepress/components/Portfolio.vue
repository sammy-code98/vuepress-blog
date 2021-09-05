<template>
  <div>
    <div class="portfolio-card">
        <div class="project-image"></div>
        <div class="project-desc"></div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      projects: [
        { name: "", description: "" },
        { name: "", description: "" },
        { name: "", description: "" },
      ],
    };
  },
};
</script>
<style scoped>
.portfolio-card{
    width: 100%;
    height: 300px;
    border-radius: 12px;
    box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
}

</style>
