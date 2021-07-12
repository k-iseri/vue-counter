<template>
  <div>
    <input v-model="inputString" placeholder="文字を入力してください" />
    <button @click="reset">リセット</button>
    <div>
      <label for="check">下線を表示する</label>
      <input type="checkbox" v-model="isChecked" id="check" />
      <span v-if="isChecked" class="checkSpan">チェック済</span>
    </div>
    <br />
    <span :class="{ underline: isChecked }" class="item">{{
      inputString
    }}</span>
  </div>
</template>

<script>
export default {
  data() {
    return {
      inputString: '',
      isChecked: false,
    }
  },
  methods: {
    reset: function() {
      this.inputString = ''
    },
  },
}
</script>

<style scoped>
.underline {
  text-decoration: underline;
}

.checkSpan {
  color: #636363;
}

.item {
  font-size: 2rem;
}
</style>
