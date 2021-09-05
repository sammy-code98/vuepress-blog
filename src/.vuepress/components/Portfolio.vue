<template>
  <div>
    <div class="portfolio-card" v-for="project in projects" :key="project.name">
      <div class="project-image">
        <img :src="project.image" alt="project image" />
      </div>
      <div class="project-desc"></div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      projects: [
        {
          name: "Lola",
          image: "../image/img1.png",
          description:
            "Legends of Runeterra is a 2020 digital collectible card game developed and published by Riot Games. Inspired by the physical collectible card game Magic: The Gathering, the developers sought to create a game within the same genre that significantly lowered",
        },
        {
          name: "Lola2",
          image: "../image/img1.png",
          description:
            "Legends of Runeterra is a 2020 digital collectible card game developed and published by Riot Games. Inspired by the physical collectible card game Magic: The Gathering, the developers sought to create a game within the same genre that significantly lowered",
        },
        {
          name: "Lola23",
          image: "../image/img1.png",
          description:
            "Legends of Runeterra is a 2020 digital collectible card game developed and published by Riot Games. Inspired by the physical collectible card game Magic: The Gathering, the developers sought to create a game within the same genre that significantly lowered",
        },
      ],
    };
  },
};
</script>
<style scoped>
.portfolio-card {
  width: 100%;
  height: 300px;
  border-radius: 12px;
  margin-top: 80px;
  box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
}
</style>
