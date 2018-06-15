# 组件系统

?> 组件可以对整块业务进行封装

<vuep template="#example"></vuep>

<script v-pre type="text/x-template" id="example">
<template>
  <div>
  	<user-info :user="user" />
  </div>
</template>

<script>
module.exports = {
  components: {
    'user-info': {
      template: '<p>{{ user.name}}<br/>{{ user.age }}</p>',
      props: ['user']	
    }
  },
  data(){
    return {
      user: {
        name: '姓名',
        age: '18'
      }
    }
  }
}
</script>
</script>