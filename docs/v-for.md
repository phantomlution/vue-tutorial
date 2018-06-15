# v-for

<vuep template="#example"></vuep>

<script v-pre type="text/x-template" id="example">
<template>
  <div>
  	<ol>
	  <li v-for="todo in todos">
	    {{ todo.text }}
	  </li>
	</ol>
  </div>
</template>

<script>
module.exports = {
  data() {
	return { 
	  todos: [
	    { text: 'todo 1' },
	    { text: 'todo 2' },
	    { text: 'todo 3' }
	  ]
	}
  }
}
</script>
</script>