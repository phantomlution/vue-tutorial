# v-if

<vuep template="#example"></vuep>

<script v-pre type="text/x-template" id="example">
<template>
  <div v-if="show">
  	{{ msg }}
  </div>
</template>

<script>
module.exports = {
  data() {
	return { 
	  msg: 'Hello Vue',
	  show: true
	}
  }
}
</script>
</script>