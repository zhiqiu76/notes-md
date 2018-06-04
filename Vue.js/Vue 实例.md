#### Vue 实例

- 创建一个实例

==每个 Vue 应用都是通过用 `Vue` 函数创建一个新的 **Vue 实例**开始的==

```
vm (ViewModel 的缩写)
var vm = new Vue({   
    // 选项
})
```

- 数据与方法

> 当一个 Vue 实例被创建时，它向 Vue 的**响应式系统**中加入了其 `data` 对象中能找到的所有的属性。当这些属性的值发生改变时，视图将会产生“响应”，即匹配更新为新的值。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <script src="js/vue.js"></script>
</head>
<body>
<div id="app">
{{mydata.name}}
</div>
</body>
<script>
var data = {name:'stefan'}
var vm = new Vue({        // 这里时一个 Vue 的实例
    el:'#app',            // 这里指定时那个元素 这里时 id 选择器
    data:{                // 这里时我们的数据
        mydata:data,
        name:'test_name',
        age:'18'
    }
})
</script>
</html>
```

