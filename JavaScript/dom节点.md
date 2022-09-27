dom节点

dom树里每一个内容都称为节点

节点类型

- 元素节点

  所有的标签，如body，div。html为根节点

- 属性节点

  所有的属性，比如href

- 文本节点

  所有的文本

- 其他

作用：可以更好地让我们理清标签元素之间的关系

查找节点

- 父节点查找

  返回最近一级的父节点，找不到返回null

  ~~~javascript
  子元素.parentNode
  ~~~

- 子元素查找

  ~~~JavaScript
  父元素.childrenNodes	//获得所有子节点，包括文本节点（空格、换行）、注释节点等
  父元素.children		//仅获得所有元素节点，返回一个伪数组
  ~~~

- 兄弟关系查找

  ~~~javas
  兄弟元素.nextElementSibling			//下一个兄弟元素
  兄弟元素.previousElementSibling		//上一个兄弟元素
  ~~~


增加节点

创建一个新的节点，把创建的新的节点放入指定的元素内部

- 创建节点

  ~~~JavaScript
  document.creatElement('标签名')
  ~~~

- 追加节点

  ~~~javascript
  父元素.appendChild(要插入的元素)		//插入到这个父元素的最后，不支持追加字符串的元素
  父元素.insertBefore(要插入的元素，插在哪个元素之前)		//插入到某个子元素的前面
  insertAdjacentHTML('插入的位置',要插入的元素)			//可以直接把字符串格式元素添加到父元素
  ~~~

> beforebegin		//元素自身的前面
>
> afterbegiin			//插入元素内部的第一个子节点之前
>
> afterend				//插入元素内部的最后一个子节点之后
>
> beforeend			//元素自身的后面

复制节点

复制一个原有的节点，将复制的节点放入指定的元素内部

- 克隆节点

  ~~~JavaScript
  元素.cloneNode(布尔值)		//为true,则代表克隆时会包含后代节点一起克隆，false代表克隆时不包含后代节点，括号							为空为默认值，默认值为false
  ~~~

删除节点

在原生dom操作中，删除节点必须通过父元素删除，如果不存在父子关系则删除不成功，删除是直接在html中删除，之后不会存在，隐藏则依旧存在

~~~JavaScript
父元素.removeChild(要删除的元素)
~~~



