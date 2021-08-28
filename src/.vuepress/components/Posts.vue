<template>
    <div>
        <div v-for="post in posts" :key="post.id">
              <div>
          <img v-if="post.frontmatter.image" :src="$withBase(post.frontmatter.image)" alt="">
        </div>
            <h2>
            <router-link :to="post.path">{{ post.frontmatter.title }}</router-link>
        </h2>
        
        <p>{{ post.frontmatter.description }}</p>
        <p>Written By : {{post.frontmatter.author}}</p>

        <p><router-link :to="post.path">Read more</router-link></p>
        </div>
    </div>
</template>
<script>
export default {
    computed:{
        posts(){
            return this.$site.pages
            .filter(x => x.path.startsWith('/blog/') &&  !x.frontmatter.posts)
        }
    }
    
}
</script>
