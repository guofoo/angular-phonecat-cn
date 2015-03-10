我们现在添加了一个```<input>```标签，并且使用AngularJS的```$filter```函数来处理```ngRepeat```指令的输入。

这样允许用户输入一个搜索条件，立刻就能看到对电话列表的搜索结果。我们来解释一下新的代码：

1. 数据绑定： 这是AngularJS的一个核心特性。当页面加载的时候，AngularJS会根据输入框的属性值名字，将其与数据模型中相同名字的变量绑定在一起，以确保两者的同步性。

 在这段代码中，用户在输入框中输入的数据名字称作```query```，会立刻作为列表迭代器（```phone in phones | filter:query```）其过滤器的输入。当数据模型引起迭代器输入变化的时候，
 迭代器可以高效得更新DOM将数据模型最新的状态反映出来。

2. 使用```filter```过滤器：```filter```函数使用```query```的值来创建一个只包含匹配```query```记录的新数组。

 ```ngRepeat```会根据```filter```过滤器生成的手机记录数据数组来自动更新视图。整个过程对于开发者来说都是透明的。