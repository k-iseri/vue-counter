<template>
  <div id="area">
    <h1>タスクリスト</h1>
    <div class="main">
      <input v-model="inputTask" /><button @click="addTask">追加</button>
    </div>
    <div v-for="(task, index) in taskList" :key="index">
      <TaskView :task="task" :index="index" @deleteTask="deleteTask" />
    </div>
  </div>
</template>

<script>
import TaskView from '~/components/TaskView.vue'

export default {
  components: { TaskView },
  data() {
    return {
      inputTask: '',
      taskList: [],
    }
  },
  methods: {
    addTask() {
      this.taskList.push(this.inputTask)
      this.inputTask = ''
    },
    deleteTask(index) {
      this.taskList.splice(index, 1)
    },
  },
}
</script>

<style scoped>
#area {
  width: 320px;
  margin: 0 auto;
}

.main {
  text-align: center;
}

.logo {
  margin-top: 32px;
  margin-bottom: 32px;
}
</style>
