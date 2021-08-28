<template>
  <div class="container">
  <router-link v-for="post in posts" :to="post.path" :key="post.id">
        <div class="card">
      <img class="imgage" src="../public/home.png" alt="" />
      <div class="details">
        <div class="title">{{ post.title }}</div>
        <div class="desc">{{ post.frontmatter.description }}</div>
        <div class="author">{{ post.frontmatter.author }}</div>
      </div>
    </div>
  </router-link>
  </div>
</template>

<script>
export default {
  data() {
    return {
      posts: [],
    };
  },
  mounted() {
    this.$site.posts.forEach((page) => {
      if (page.frontmatter.type === "blog") {
        this.posts.push(post);
      }
    });
  },
};
</script>

<style></style>
