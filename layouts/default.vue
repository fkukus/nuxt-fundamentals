<template>
  <div class="container">
    <TheNavbar />
    <nuxt />
    <div class="footer">
      Test automatic deploy with <a href="https://www.heroku.com/" target="_blank">Heroku</a>
    </div>
  </div>
</template>

<script>
import TheNavbar from '~/components/TheNavbar.vue'
export default {
  components: {
    TheNavbar
  }
}
</script>
