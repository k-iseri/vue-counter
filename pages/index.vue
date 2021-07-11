<template>
  <div>
    <div>カウント：{{ count }}</div>
    <div>
      <button @click="increment">加算</button>
      <button @click="reset">リセット</button>
    </div>
    <div>カウントx2：{{ countx2 }}</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      /* 変数を用意する。初期値は0 */
      count: 0,
    }
  },
  computed: {
    countx2: function() {
      /* 常にcountの2倍を返す */
      return this.count * 2
    },
  },
  methods: {
    increment: function() {
      /* 呼ばれたらcountに1を足す */
      this.count++
    },
    reset: function() {
      /* 呼ばれたらcountに0を代入 */
      this.count = 0
    },
  },
}
</script>
