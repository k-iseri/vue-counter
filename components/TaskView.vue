<template>
  <div>
    <input type="checkbox" v-model="done" />
    <span :class="{ doneTask: done }">{{ task }}</span>
    <button @click="sendDelete">削除</button>
  </div>
</template>

<script>
export default {
  props: {
    task: { type: String, require: true, default: '' },
    index: { type: Number, require: true, default: 0 },
  },
  data() {
    return { done: false }
  },
  methods: {
    sendDelete() {
      this.$emit('deleteTask', this.index)
    },
  },
}
</script>
<style scoped>
.doneTask {
  text-decoration: line-through;
}
</style>
