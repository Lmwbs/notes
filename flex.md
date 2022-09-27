flex

css中的一种布局手段，用来代替浮动来完成页面的布局，使元素具有弹性，跟随页面大小的改变而改变

弹性容器：要使用弹性盒，必须先将一个元素设置为弹性容器，通过`display`设置弹性容器

> display: flex				设置为块级弹性容器
>
> display: inline-flex	  设置为行内弹性容器

弹性元素：弹性容器的直接子元素是弹性容器，一个元素可以同时是弹性容器和弹性元素

`flex-direction:` 指定容器中弹性元素的排列方式

> 可选值
>
> ​	row						默认值，弹性元素在容器中水平排列（左→右）
>
> ​	row-reverse			弹性元素在容器中反向水平排列（右→左）
>
> ​	column					弹性元素纵向排列（上→下）
>
> ​	column-reverse		弹性元素反纵向排列（下→上）

主轴：弹性元素的排列方向称为主轴

侧轴：与主轴垂直的称为侧轴

弹性容器的样式：

>flex-wrap: 设置弹性元素是否在弹性容器中自动换行
>
>​		可选值：
>
>​				nowrap			默认值
>
>​				wrap				元素沿着辅轴方向自动换行
>
>​				wrap-reverse	元素沿着辅轴反方向换行
>
>flex-flow: wrap和direction的简写属性，无顺序要求，两者之间用空格隔开
>
>justify-content: 设置如何分配主轴上的空白区域（justuify表示与主轴有关）
>
>​		可选值：
>
>​				flex-start			元素沿着主轴起始边排列
>
>​				flex-end			元素沿着主轴终边排列
>
>​				center				元素居中排列
>
>​				space-around	空白分布到元素两侧
>
>​				space-between	空白均匀分布到元素之间
>
>​				space-evenly	空白分布到元素单侧
>
>align-items: 设置元素在辅轴上如何对齐（align表示与辅轴有关）
>
>​		可选值：
>
>​				stretch				默认值，每个元素的长度相等
>
>​				flex-start			元素沿着辅轴起始边排列
>
>​				flex-end			元素沿着辅轴终边排列
>
>​				center				元素居中排列
>
>​				baseline			基线对齐
>
>`align-content:`用法与`justify-content:`一致
>
>align-self: 用于给弹性容器中的某个元素设置对齐方式

弹性元素的样式：

>flex-grow: 指定弹性元素的伸展系数，默认为1，当父元素有多余空间时，子元素会按比例分配父元素剩余的空间
>
>flex-shrink: 指定弹性元素的收缩系数，默认为1，当父元素的空间不足以容纳所有的子元素时，会按比例缩小子元素的空间
>
>flex-basis: 指定元素主轴上的长度，默认值为auto，表示参考元素自身的高度或宽度
>
>flex: 指定元素以上的三个属性，顺序为伸展 收缩 长度，`initial`相当于`0 1 auto`，`auto`相当于`1 1 auto`，`none`相当于`0 0 auto`
>
>order: 决定弹性元素的排列顺序，数字小的排在前面

