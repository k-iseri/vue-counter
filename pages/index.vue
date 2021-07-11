<template>
  <div>
    <div>
      カウント：{{ count }}
    </div>
    <div>
      <button @click="increment">加算</button>
      <button @click="reset">リセット</button>
    </div>
    <div>
      カウントx2：{{ countx2 }}
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      count: 0
    }
  },
  computed: {
    countx2: function() {
      return this.count * 2;
    }
  },
  methods: {
    increment : function() {
      this.count++;
    },
    reset: function() {
      this.count = 0;
    }
  }  
}
</script>
