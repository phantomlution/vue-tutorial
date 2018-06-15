# Vue事件

### 订阅事件
```
vm.$on()
vm.$once();(防止表单重复提交)
```

### 发送事件
```
vm.$emit()
```

### 取消订阅事件
```
vm.$off()	
```

# 如何在SPA页面中构建全局事件中心

```
Vue.prototype.$bus = new Vue();

```

### 用法
```
vm.$bus.$on();
vm.$bus.$once();
vm.$bus.$emit();
vm.$bus.$off()
```