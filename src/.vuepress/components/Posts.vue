<template>
  <div>
    <div class="card" v-for="post in posts" :key="post.id">
      <div>
        <img
          class="post-img"
          v-if="post.frontmatter.image"
          :src="$withBase(post.frontmatter.image)"
          alt=""
        />
      </div>
      <h2 class="title">
        <router-link :to="post.path">{{ post.frontmatter.title }}</router-link>
      </h2>
      <p>Written By : {{ post.frontmatter.author }}</p>
      <p class="desc">{{ post.frontmatter.description }}</p>
      <p>{{ post.readingTime.text }}</p>

      <p><router-link :to="post.path">Read more</router-link></p>
    </div>
  </div>
</template>
<script>
export default {
  computed: {
    posts() {
      return this.$site.pages.filter(
        (x) => x.path.startsWith("/blog/") && !x.frontmatter.posts
      );
    },
  },
};
</script>
<style scoped>
.card {
  height: auto;
  width: 80%;
  margin: 20px;
  padding: 20px;
  border-radius: 12px;
  box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;
}
.title {
  text-align: center;
}
.post-img {
  height: 200px;
  width: 100%;
  border-radius: 8px;
}
.desc {
  width: 600px;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}
/* media query for description text */
@media only screen and (max-width: 600px) {
    .desc{
        width: 250px;
    }
}
@media only screen and (min-width: 600px) {
    .desc{
        width: 500px;
    }
}
</style>
