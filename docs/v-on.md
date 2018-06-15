# v-on

<vuep template="#example"></vuep>

<script v-pre type="text/x-template" id="example">
<template>
  <div>
  	<p>{{ message }}</p>
  	<button @click="reverseMessage">逆转消息</button>
  </div>
</template>

<script>
module.exports = {
  data(){
    return {
      message: 'Hello Vue.js!'
    }
  },
  methods: {
    reverseMessage: function () {
      this.message = this.message.split('').reverse().join('')
    }
  }
}
</script>
</script>