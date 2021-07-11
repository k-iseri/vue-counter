<template>
  <div>
    <input v-model="inputString" />
    <div>
      <label for="check">下線を表示する</label>
      <input type="checkbox" v-model="ifUnderLine" id="check" />
      <button @click="reset">リセット</button>
    </div>
    <br />
    <span :class="{ underline: ifUnderLine }" class="item">{{
      inputString
    }}</span>
  </div>
</template>

<script>
export default {
  data() {
    return {
      inputString: '',
      ifUnderLine: false,
    }
  },
  methods: {
    reset: function() {
      this.inputString = ''
      this.ifUnderLine = false
    },
  },
}
</script>

<style scoped>
.underline {
  text-decoration: underline;
}

.item {
  font-size: 2rem;
}
</style>
