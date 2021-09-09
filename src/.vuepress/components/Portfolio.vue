<template>
  <div>
    <div class="portfolio-card" v-for="project in projects" :key="project.name">
      <div class="project-image">
        <img :src="project.image" alt="project image" class="project-image" />
      </div>
      <div class="project-desc">
        <h3>{{ project.name }}</h3>
        <p>{{ project.description }}</p>
        <button class="live-btn">View Live</button>
      </div>
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
          image: require("../../assets/image/img1.png"),
          description:
            "Legends of Runeterra is a 2020 digital collectible card game developed and published by Riot Games. Inspired by the physical collectible card game Magic: The Gatheri",
          link: "www.google.com",
        },
        {
          name: "Lola2",
          image: require("../../assets/image/img2.png"),
          description:
            "Legends of Runeterra is a 2020 digital collectible card game developed and published by Riot Games. Inspired by the physical collectible card game Magic: The Gatheri",
          link: "www.google.com",
        },
        {
          name: "Lola23",
          image: require("../../assets/image/img3.png"),
          description:
            "Legends of Runeterra is a 2020 digital collectible card game developed and published by Riot Games. Inspired by the physical collectible card game Magic: The Gatheri",
          link: "www.google.com",
        },
      ],
    };
  },
};
</script>
<style scoped>
.portfolio-card {
  background: rgb(235, 234, 234);
  display: flex;
  width: 100%;
  height: 300px;
  border-radius: 12px;
  margin-top: 80px;
  box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
}
.project-desc {
  width: 50%;
  margin: 5px;
  padding-right: 30px;
 
}
.live-btn {
  border: none;
  outline: none;
  border-radius: 8px;
  color: #3eaf7c;
  background: #fff;
  font-size: 15px;
  cursor: pointer;
  padding: 10px;
}
.live-btn:hover {
  box-shadow: rgba(0, 0, 0, 0.16) 0px 1px 4px;

}
.project-image {
  width: 80%;
  height: 95%;
  margin: 7px;
  border-radius: 5px;
}

</style>
