BOM

BOM（Browser Object Model）是浏览对象模型，window是浏览器内置中的全局对象，所有的web APIs 都是基于window对象实现的，window对象下包含了navigator、location、document、history、screen共5个属性，即所谓的BOM

JS执行机制

JavaScript语言最大的特点是单线程，即同一时间只能做一件事，因此所有的任务需要排队，前一个任务结束才会执行下一个任务，为了解决这个问题，利用多核CPU的计算能力，HTML5提出了web worker标准，允许JavaScript脚本创建多个线程。因此出现了同步和异步

> 同步：前一个任务执行结束后再执行下一个任务，程序的执行顺序与任务的排列顺序一致
>
> 异步：一个任务需要很长时间，在处理这个任务的同时可以去处理其他任务
>
> 同步任务：同步任务都在主线程上执行，形成一个执行栈
>
> 异步任务：JS的异步通过回调函数实现，异步任务相关添加到任务队列，也称作消息队列一般包含以下三种类型
>
> - 普通事件，如click、resize等
> - 资源加载，如load、error等
> - 定时器，如setInterval、setTimeout等

==1. 先执行栈中的同步任务==

==2. 异步任务放入任务队列中==

==3.一旦执行栈中的所有同步任务执行完毕，系统会按次序读取任务队列中的异步任务，被读取的异步任务结束等待状态，进入执行栈，开始执行==

location对象

该对象拆分并保存了URL地址的各个组成部分

> 常见属性与方法
>
> href属性获取完整的URL地址，对其赋值时用于地址的跳转
>
> ~~~JavaScript
> location.href='url'		//可以跳转到该页面
> ~~~
>
> search属性获取地址中携带的参数，符号?后面部分
>
> hash属性获取地址中的哈希值，符号#后面部分，为vue做铺垫，不刷新页面就可以显示不同页面
>
> reload方法用来刷新当前页面，出入参数true时表示强制刷新

navigator对象

该对象记录了浏览器自身的相关信息

history对象

该对象与浏览器地址栏的操作相对应，如前进、后退、历史记录等

> 常用方法与属性
>
> back()			//后退功能
>
> forward()		//前进功能
>
> go(参数)		 //前进后退功能，参数为0，前进一个页面，如果是-1后退一个页面

swiper插件

就是利用别人写好的代码直接复制过来实现对应的效果

本地存储

特性：

- 数据存储在用户浏览器中
- 设置、读取方便、甚至刷新也不会丢失数据
- 容量较大，sessionStrorage和loaclStorage约5M作用

localStorage

- 生命周期永久生效，除非手动删除，否则关闭页面也存在
- 可以多窗口（页面）共享（同一浏览器可以共享）
- 以键值对的形式存储使用

~~~JavaScript
localStorage.setItem('key','value')		  //存取数据
localStorage.getItem('key')				//获取数据
localStorage.removeItem('key','value')	  //删除数据
~~~

存储复杂数据类型

本地只能存储字符串，无法存储复杂数据类型，需要将复杂数据类型转换成JSON字符串，然后存储到本地

~~~javascript
JSON.stringify(复杂数据类型)		//将复杂数据转换成JSON字符串存储到本地
JSON.parse(JSON字符串)			//将JSON字符串转换成对象，取出时使用
~~~

sessionStorage

- 生命周期为关闭浏览器窗口
- 在同一个窗口（页面）下数据可以共享
- 以键值对的形式存储使用
- 用法跟localStorage基本相同

自定义属性

固有属性：标签自带的属性，如class、id、title等，可以直接使用点语法操作

自定义属性：由程序员自己添加的属性，在DOM对象中找不到，无法使用点语法操作，必须使用专门的API

~~~JavaScript
getAttribute('属性名')				  //获取自定义属性
setAttribute('属性名','属性值')		 //设置自定义属性
removeAttribute('属性名')			  //删除自定义属性
~~~

因为自定义属性没有专门的定义规则，开发者随意规定不太规范，因此html5中推出了`data-自定义属性`，自定义标签一律以`data-`开头，以`dataset`对象方式获取
