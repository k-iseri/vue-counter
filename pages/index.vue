<template>
  <div class="main">
    <NuxtLogo class="logo" />
    <Greeting /><!-- Hello World!! -->
    <Greeting :text="displayText" /><!-- こんにちは -->
    <Greeting text="你好" />
    <nuxt-link to="page2">2ページへ</nuxt-link>
  </div>
</template>

<script>
import NuxtLogo from '~/components/NuxtLogo.vue'
import Greeting from '~/components/Greeting.vue'

export default {
  components: { NuxtLogo, Greeting },
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
