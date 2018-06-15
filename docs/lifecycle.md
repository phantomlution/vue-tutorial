# vue 组件的生命周期

![Lifecycle](static/lifecycle.png 'Lifecycle')

### mounted
```
当前状态下，元素已经挂在到DOM中，可以使用DOM元素操作
```
### destroyed
```
组件被销毁后调用的HOOK，用于释放额外的资源（例如定时器）
```

### 下面是一个例子

<vuep template="#example"></vuep>

<script v-pre type="text/x-template" id="example">
<template>
  <div> 
  	<countdown :log="log" v-if="!destroy"></countdown>
  	<div v-for="item in log">
  	  <div>{{ item }}</div>
  	</div>
  	<button @click="destroy = true">销毁组件</button>
  </div>
</template>

<script>
module.exports = {
  components: {
    'countdown': {
      props: ['log'],
      template: '<button @click="start" v-if="!started">启动定时器</button>',
      data: function(){
       return{
       	  log: [],
      	  interval: null,
      	  started: false
      	}
      },
      methods: {
      	start(){
		  const $this = this;
          this.interval = setInterval(function(){ $this.log.push('logging');}, 1000);
          this.started = true;
      	}
      },
      // destroyed(){
      // 	if(this.interval){
      // 	  clearInterval(this.interval);
      // 	}
      // }	
    }
  },
  watch: {
    destroy(val){
      if(val){
        this.log.length = 0;	
      }
    }
  },
  data(){
    return {
      log: [],
      destroy: false
    }
  }
}
</script>
</script>
