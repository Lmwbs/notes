Web API基本认识

作用：使用JS去操作html和浏览器

分类：DOM(文档对象模型)、BOM(浏览器对象模型)

DOM

Document Object Model，用来呈现以及与任意HTML或XML文档交互的API。即是浏览器提供的一套专门用来操作网页内容的功能

作用：开发网页内容特效和实现用户交互

DOM树：

将HTML文档以树状结构直观的表现出来，也称为文档树

作用：直观的体现标签与标签之间的关系

DOM对象：

浏览器会根据html标签自动生成js对象，所有的标签属性都可以在这个对象上面找到，修改这个对象的属性会自动映射到标签身上

DOM的核心思想：把网页内容当做对象来处理

获取DOM元素

1. 根据CSS选择器获取DOM元素

> 1. 获取第一个元素
>
>    语法：`document.querySelector('css选择器')`
>
>    返回值：CSS选择器匹配到的第一个元素，一个HTMLelement对象，如果没有匹配到，则返回null
>
> 2. 获取多个元素
>
>    语法：`document.querySelectorAll('css选择器')`
>
>    返回值：伪数组
>
>    ==只有一个元素时，使用该语法获得的也是一个伪数组==

2. 其他获取DOM元素的方法

   ~~~JavaScript
   document.getElementById('')			  //根据id获取元素
   document.getElementByTagName('')	  //根据标签获取一类元素
   document.getElementByClassName('')	  //根据类名获取元素
   ~~~

设置/修改DOM元素内容

1. `document.write()`
   - 只能将文本内容追加到</body>前面的位置
   - 文本中包含的标签会被解析
2. 元素的innerText属性
   - 将文本内容添加/更新到任意标签位置
   - 文本中包含的标签不会被解析
3. 元素的innerHTML
   - 将文本内容添加/更新到任意标签位置
   - 文本中包含的标签不会被解析

设置/修改元素常用的属性

1. `对象.属性=值`

   设置/修改常见的属性，如：href、title、src等

设置/修改样式的属性

用途：通过轮播图小圆点自动更换颜色样式

​		  点击按钮滚动图片

1. `对象.style.样式属性=值`
   - 如果属性有-连接符，需要转换为小驼峰命名法（background-color为backgroundColor）
   - 赋值时，有单位的不要忘记单位
   - 样式会转换在行内
   - 适合修改较少的样式属性

2. `元素.className='类名'`
   - 该方法的类名是用新值替换旧值
   - 修改的样式较多时，可以将样式放入一个类中，利用该方法修改

3. classList操作类

   ~~~JavaScript
   元素.classList.add('类名')		//追加一个类
   元素.classList.remove('类名')	//删除一个类
   元素.classList.toggle('类名')	//切换一个类
   ~~~

   - 解决了className容易覆盖以前的类名的问题

设置/修改表单元素属性

获取：`对象.属性名`

设置：`对象.属性名=新值`

==表单中有些属性添加就有效果，不添加就没有效果，这种情况的值一律使用布尔值。如：disabled、checked、selected==

获取标签中的内容

- div、span、ul、li标签利用`元素.innerText`
- 表单input单选、复选、textarea、select利用表单的`value`
- 特殊的，button通过`inner`获取