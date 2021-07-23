<template>
  <div>
    <input type="checkbox" v-model="done" />
    <span :class="{ doneTask: done }">{{ task }}</span>
  </div>
</template>

<script>
export default {
  props: { task: { type: String, require: true, default: '' } },
  data() {
    return { done: false }
  },
}
</script>
<style scoped>
.doneTask {
  text-decoration: line-through;
}
</style>
