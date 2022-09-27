对象

JavaScript中的一种数据类型，可以理解为一种无序的数据集合

对象由属性和方法组成：

属性：数据描述性的信息，多个属性之间用`,`隔开，最后一个不需要加，属性就是依附在对象上的变量

方法：数据行为性的信息，本质是函数方法由方法名和函数构成，之间使用`:`分隔

> 声明语法：
>
> ~~~JavaScript
> let 对象名={
>     属性名:属性值
>     方法名:函数			//此处的函数为匿名函数
> }
> ~~~
>
> 访问属性：
>
> ~~~JavaScript
> console.log(对象名.属性名)
> console.log(对象名['属性名'])
> ~~~
>
> 访问对象：
>
> ~~~JavaScript
> 对象名.方法名()
> ~~~

对象的操作：

>修改：
>
>~~~JavaScript
>对象名.属性=新值
>对象名['属性']=新值
>对象.方法=founction(){}
>~~~
>
>增加：
>
>~~~JavaScript
>对象名.新属性名=值
>对象名['新属性']=值
>对象.新方法=founction(){}
>~~~
>
>==新增一个属性的时候，js会先去对象里找是否存在这个属性，存在则修改，不存在则新增==
>
>删除：
>
>~~~JavaScript
>delete 对象名.属性名
>delete 对象名['属性名']
>delete 对象名.方法名
>~~~
>
>遍历：
>
>~~~JavaScript
>for(let k in 对象名){
>    console.log(k)				//遍历属性名
>    console.log(对象名[k])		  //遍历属性值
>}
>~~~
>
>==k是变量，可以随便设定，但一般使用k或者key==

内置对象

JavaScript内部提供的对象，包含各种属性和方法供开发者调用。例如：`document.write()、console.log()`

内置对象Math

Math对象是JavaScript中提供的一个可以进行一系列数学运算的方法

> random()			------生成0到1之间的随机数（包括0不包括1）
>
> ceil(x)					------向上取整
>
> floor(x)				 ------向下取整
>
> round(x)				------就近取整
>
> max(x,y)				  ------找最大数
>
> min(x,y)					------找最小数
>
> pow()					------幂运算
>
> abs()					 ------绝对值

生成N~M之间的随机数

~~~JavaScript
Math.floor(Math.random()*(M-N+1))+N
~~~

时间对象

用来表示时间的对象，可以得到当前的系统时间

- 实例化

  在代码中发现new关键字时，一般将这个操作称为实例化

  获得当前时间

  ~~~JavaScript
  let date = new Date()
  new Date().toLocaleString()		//
  ~~~

  获得指定时间

  ~~~JavaScript
  let date = new Date('年-月-日 时:分:秒')
  ~~~

- 时间对象方法

  时间对象返回的数据不能直接使用，要转换为实际开发中常用的格式

  ~~~javascript
  getFullYear()	//获得四位年份
  getMonth()		//获得取值为0至11的月份
  getDate()		//获取月份中的每一天，月份不同值不同
  getDay()		//获取值为0至6的星期
  getHours()		//获取0至23的小时
  getMinutes()	//获取0至59的分钟
  getSeconds()	//获取0至59的秒数
  ~~~

- 时间戳

  指1970年01月01日00时00分00秒起至现在的毫秒数，它是一种特殊的计量时间的方式

  获取时间戳

  ~~~JavaScript
  getTime()
  +new Date()		
  Date.now()		//不需要实例化，只能得到当前的时间戳，前两个可以返回指定时间的时间戳
  ~~~

  ==为了防止输入无意义的空格，可以利用`.trim()`去掉首尾空间，用法参考dom微博发布案例==
  

事件对象

有事件触发时的相关信息的对象

获取

在事件绑定的回调函数的第一个参数就是事件对象，一般命名为event、ev、e

~~~JavaScript
元素.addEventListener('click',function(e)){}
~~~

部分常用属性

> type						获取当前的事件类型
>
> clientX/clientY		获取光标相对于浏览器可见窗口左上角的位置
>
> offsetX/offsetY		获取光标相对于当前DOM元素左上角的位置
>
> pageX/pageY			获取光标相对于文档坐标
>
> key							用户按下的键盘的值

