<template>
  <div>
    <div class="portfolio-card" v-for="project in projects" :key="project.name">
      <div class="project-image">
        <img :src="project.image" alt="project image" class="project-image" />
      </div>
      <div class="project-desc">
        <h3>{{ project.name }}</h3>
        <p>{{ project.description }}</p>
        <a
          :href="project.link"
          class="live-btn"
          target="_blank"
          rel="noreferrer noopener"
          >View Live</a
        >
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
          name: "Documentation site",
          image: require("../../assets/image/img1.png"),
          description:
            "Built with Vuepress, this site utilises the benefits of markdown and houses the documentation for the react-image-plugin.",
          link: "https://image-upload-plugin.netlify.app",
        },
        {
          name: "Ebsirs",
          image: require("../../assets/image/img2.png"),
          description:
            "A demo template for the Ebonyi State Internal Revenue Service Board",
          link: "https://ebonyi-rev.netlify.app/",
        },
        {
          name: "Prudent Words Blog",
          image: require("../../assets/image/img3.png"),
          description:
            "Blog Template built with Quasar",
          link: "https://prudent-words.netlify.app",
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
  text-decoration: none;
  outline: none;
  border-radius: 8px;
  color: #3eaf7c;
  background: #fff;
  font-size: 15px;
  cursor: pointer;
  padding: 10px;
}
.live-btn:hover {
  background: #3eaf7c;
  color: #fff;
  text-decoration: none;
  box-shadow: rgba(0, 0, 0, 0.16) 0px 1px 4px;
}
.project-image {
  width: 80%;
  height: 95%;
  margin: 7px;
  border-radius: 5px;
}
/* media query */
@media only screen and (max-width: 600px) {
  .portfolio-card {
    display:grid;
    height: 430px;
    
  }
  .project-image{
    width:300px;

  }
  .project-desc{
    text-align: center;
    width: 100%;
    padding-right: 8px;
    margin-right: 40px;
  }

  
 
  
}
</style>
