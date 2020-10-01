<template>
  <div class="container">
    <div>
      <Logo />
      <h1 class="title">
        nuxt-fundamentals
      </h1>
      <div class="links">
        <nuxt-link
          v-for="post in posts"
          :key="post.id"
          class="button--grey"
          :to="{name: 'posts-id', params:{id: post.id}}"
        >
          {{ post.title }}
        </nuxt-link>
      </div>
      <p>Test automatic deploy from Heroku</p>
    </div>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  },
  computed: {
    posts () {
      return this.$store.state.posts.all
    }
  },
  head: {
    title: 'Home page',
    meta: [
      { name: 'description', content: 'Nuxt + Vue School tutorial' },
      { name: 'twitter:title', content: 'Nuxt Fundamentals by Vue School' },
      { name: 'twitter:description', content: 'Nuxt + Vue School tutorial' },
      { name: 'twitter:image', content: 'https://picsum.photos/300/200' },
      { name: 'twitter:card', content: 'summary_large_image' }
    ]
  }
}
</script>

<style scoped>
  .container {
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
  }
  .title {
    font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
    display: block;
    font-weight: 300;
    font-size: 100px;
    letter-spacing: 1px;
  }
  .subtitle {
    font-weight: 300;
    font-size: 42px;
    color: #526488;
    word-spacing: 5px;
  }
  .links {
    padding-top: 15px;
  }
</style>
