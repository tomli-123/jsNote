# DESK

### 1.组件

```
dataset 数据集合
align 布局 前 中 后
raised-button 是按钮 可以加字体图标
common-dialog 弹出框
datepicker-ctrl 时间选择器
html-dataset  可以解析 html标签
upload-dataset 上传文件
mat-checkbox mat-icon 复选框 字体图标 mat关键字
button 三种不同类型 
drawer类型  下拉型 出现子按钮 父按钮无作用 
icon类型  图标按钮 不会有形状 是一个字体图标
raised类型  普通类型 就是一个简单的按钮
anchor类型 是一个导航 （锚点导航）
```

### 2.包裹标签类型

```
1.div-form 是form类型的标签 里面包裹 form元素
2.align 布局标签 会创建三个不同 位置（横向）的三个子标签
3.sidenav 侧边栏 标签  可以通过自身的 isopen属性 来控制 是否弹出
```

### 3.注意点

```
1.属性中的名称 类似于id  当不写的时候 使用当时的 diskid 如果写 名称则用名称（一般不写）
2.select 中的 全选空值 直接写空选项 这样传递给后端的就是null
3.treeselect-ctrl 另类下拉框  可以多选  得到的值是一个数组  给treeselect赋值 给 options赋值
```

### 4.方法

```
1.在qiuer框架中使用 this.cid('名称').getValue(true, true, true) 即可获取本条root上的所有值
form表单的方法   getValue中的值分别代表 是否取 禁用值 是否取 被动值  是否取 隐藏值
2.得到方法后需要使用call调用该方法 这时才不会报错 
call的第二个参数是方法的参数
3.this 指向 本组件  this.cid("mingcheng") 可以获取本root下的组件
4.Form表单配合 getValue 使用 可以获取 form表单的值
5.this._columns  获取本地 columns 的值
this._getValue  传入参数 参数1 rowdata 参数2 item（数组项即每行数据） 就可以获取本行数据
```

### 5.权限

```
首先确定字段 其次配置页面 然后配置功能点 接着配置路由 然后配置菜单 最后给权限(超级用户) 
```

### 6.报表迁移

```
1.qiuer25 可以直接使用 报表迁移  如果是生产 迁移到 测试 那就可以互换
2.如果不是qiuer25 那么在工作台 使用 导入导出 将 导出的 roots部分黏贴 复制到 需要导入的里面的 
```

