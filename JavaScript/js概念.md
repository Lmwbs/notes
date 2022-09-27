概念：

JavaScript是一种运行在客户端（浏览器）的编程语言，实现人机交互效果。

作用：

- 网页特效（监听用户的一些行为让网页做出对应的反馈）

- 表单验证（针对表单数据的合法性进行判断）
- 数据交互（获取后台数据，渲染到前端）
- 服务端编程（node.js）

JavaScript的发展历史：

JavaScript诞生于1995年，它的出现只要是用于处理网页中的前端验证

> 前端验证：指检查用户输入的内容是否符合一定的规则，比如用户名的长度，密码的长度，邮箱的格式等

JavaScript由网景（Netscape）公司发明，起初命名为LiveScript，后来由SUN公司介入更名为JavaScript。微软公司在1996年在最新的IE3浏览器中引入了自己的JScript，于是市面上存在两个版本的JavaScript。为了确保不同浏览器上运行的JavaScript标准一致，所以几个公司共同定制了JS的标准命名为ECMAScript

一般来说JavaScript与ECMAScript意思一样，但事实上JavaScript的范围更大一些。一个完整的JavaScript由ECMAScript和Web APIS组成，Web APIS由DOM（页面文档对象模型）和BOM（浏览器对象模型）两部分组成

> ECMAScript：规定了JS基础语法的核心知识（变量、分支语句、循环语句、对象等等）
>
> Web APIS：DOM：操作文档，比如对页面元素的移动、调整大小和删除添加等操作
>
> ​					BOM：操作浏览器，比如对窗口的宽度进行检、页面弹窗、存储数据等操作

JS的特点：

- 解释型语言（写完不用编译，直接运行）
- 类似于C和Java的语法结构
- 动态语言
- 基于原型的面向对象

JS代码可以编写在`script`标签中（`script`标签在`body`标签内部写）

```
<script></script>
```

基本用法：

`alert("");`						控制浏览器弹出一个警告框

`document.write("");`		 让计算机在页面中输入一个内容

`console.log("");`			  向控制台输出一个内容

`prompt("")`						提示用户输入

```html
alert("FBI，Open the door！！！");
document.write("看见我了吗？看见我了吗？");
console.log("我在控制台中显示");
```

==注：JS代码会一行一行按照顺序执行==

JS代码也可以编写在标签的`onclick`属性中，当点击按钮时，代码才会执行（此时结构与行为耦合，不方便维护）

```html
<button onclick="alter('别点了');">点击一下</button>
```

JS代码可以写在超链接中的`href`属性中，点击超链接会执行JS代码

```html
<a href="javascript:alert('点就点，who怕who！');">点我一下</a>
```

可以将JS代码写在外部的JS文件中，通过`script`标签引入

```html
<script src="文件路径"></script>
```

==注：`script`标签一旦引入文件就不能再编写代码了，==浏览器会忽略，可以创建一个新的`script`标签进行编写代码

注释：

> //			单行注释（ctrl+/）
>
> /**/		 多行注释(shift+alt+a)

==JS中的结束符是`;`，结束符可以省略不写，因为JS中的换行会被识别为结束符==

字面量：

在计算机科学中，字面量是在计算机中描述事/物。比如：

> 1234			数字字面量
>
> "前端"		  字符串字面量
>
> [1,2,3]		  数组字面量
>
> {1,2,3,a}		对象字面量