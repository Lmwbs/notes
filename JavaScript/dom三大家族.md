scroll家族

- 获取宽高

  获取元素的内容的总宽高（不包含滚动条），返回值不带单位

  `scrollWidth`和`scrollHeight`

- 获取位置

  获取元素内容往左、往上滚出去看不到的距离,这两个属性的值可修改，修改时不要带单位

  `scrollLeft`和`scrollTop`

offset家族

- 获取宽高

  获取元素自身的宽高，包含元素自身设置的宽高、padding、border

  `offsetWidth`和`offsetHeight`

- 获取位置

  获取元素距离自己定位父级元素的左、上距离。两个都为只读属性

  `offsetLeft`和`offsetTop`

client家族

- 获取宽高

  获取元素的宽高，不包含边框、滚动条等

  `clientWidth`和`clientHeight`

- 获取位置

  获取左边框和上边框的宽度。两个都为只读属性

  `clientLeft`和`clientTop`

  会在窗口尺寸发生改变时触发条件

  `resize`