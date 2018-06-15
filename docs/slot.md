# slot

?> 组件封装更彻底，代码简练

![page](static/page.jpg 'page')

```
<sl-page-list @search="doSearch">
  <div slot="search">
    <!-- 搜索区的内容 -->
  </div>
  <div slot="action">
    <el-button>新建活动页</el-button>
  </div>
  <div slot="table">
    <!-- table -->
  </div>
  <div slot="dialog">
    <!--  弹出层 -->
  </div>
</sl-page-list>
```


### slot-scope