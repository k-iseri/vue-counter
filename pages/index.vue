<template>
  <div>
    <input v-model="inputString" />
    <div>文字列：{{ outputString }}</div>
    <div>
      <button @click="increment">加算</button>
      <button @click="reset">リセット</button>
    </div>
    {{ stringx2 }}
  </div>
</template>

<script>
export default {
  data() {
    return {
      inputString: '',
      outputString: '',
    }
  },
  computed: {
    stringx2: function() {
      /* 常にcountの2倍を返す */
      return this.outputString + this.outputString
    },
  },
  methods: {
    increment: function() {
      /* 呼ばれたらcountに1を足す */
      this.count++
      this.outputString += this.inputString
    },
    reset: function() {
      this.inputString = ''
    },
  },
}
</script>
