<template>
  <p class="main">
    2ページ目です<br />
    <Greeting text="ようこそVueの世界へ" />
    <nuxt-link to="/">トップへ</nuxt-link>
  </p>
</template>

<script>
import Greeting from '~/components/Greeting.vue'

export default {
  components: { Greeting },
  data() {
    return {
      displayText: 'こんにちは',
    }
  },
}
</script>

<style scoped>
.main {
  text-align: center;
}

.logo {
  margin-top: 32px;
  margin-bottom: 32px;
}
</style>
