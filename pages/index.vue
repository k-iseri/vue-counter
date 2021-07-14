<template>
  <div>
    <h1>Todoリストメモ</h1>
    <input v-model="inputString" placeholder="予定を入力してください" />
    <button @click="addItem">追加</button>
    <ul>
      <li v-for="(todo, index) in todoList" :key="index">
        {{ todo }}
      </li>
    </ul>
    <button @click="reset">リセット</button>
    リロードすると最初の状態に戻ります
  </div>
</template>

<script>
export default {
  data() {
    return {
      inputString: '',
      todoList: ['ラジオ体操', '掃除', '朝食'],
    }
  },
  methods: {
    addItem: function() {
      if (this.inputString) {
        this.todoList.push(this.inputString)
        this.inputString = ''
      }
    },
    reset: function() {
      this.todoList = []
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
