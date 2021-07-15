<template>
  <div id="greeting">{{ text }}</div>
</template>

<script>
export default {
  props: { text: { type: String, require: false, default: 'Hello World!!' } },
}
</script>
<style scoped>
#greeting {
  font-size: 48px;
}
</style>
