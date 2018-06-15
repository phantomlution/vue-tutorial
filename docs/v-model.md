# v-model

<vuep template="#example"></vuep>

<script v-pre type="text/x-template" id="example">
<template>
  <div>
    <p>{{ message }}</p>
    <input v-model="message">
  </div>
</template>

<script>
module.exports = {
  data(){
    return {
      message: 'Hello Vue.js!'
    }
  }
}
</script>
</script>