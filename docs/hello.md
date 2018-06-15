# Hello Vue

<vuep template="#example"></vuep>

<script v-pre type="text/x-template" id="example">
<template>
  <div>
  	{{ msg }}
  </div>
</template>

<script>
module.exports = {
  data() {
	return { 
	  msg: 'Hello Vue'
	}
  }
}
</script>
</script>