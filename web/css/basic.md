# CSS基础知识

### 1. position: relative absolute fixed sticky   (clip-path(t, r, b, l) 剪切)
    - relative: 相对于文档流
    - absolute：相对于第一个定位的父元素，或body
    - sticky：  显示时正常显示，滚动后固定

### 2. 布局
    - display      隐藏不接受操作
    - float        
    - visibility   隐藏占位子不接受操作
    - overflow     隐藏接受操作
    - clip-path    隐藏接受操作
如果display设置为none，float及position属性定义将不生效；
如果position既不是static也不是relative或者float不是none或者元素是根元素，当display:inline-table时，display的计算值为table；当display:inline | inline-block | run-in | table-* 系时，display的计算值为block，其它情况为指定值；
IE6,7支持inline元素转换成inline-block，但不支持block元素转换成inline-block，所以非inline元素在IE6,7下要转换成inline-block，需先转换成inline，然后触发hasLayout，以此来获得和inline-block类似的效果
IE6 IE7 block 转 inline-block
```javascript
    div {
	  display: inline-block;
	  *display: inline;
	  *zoom: 1;
    }
```

### 3. 边框
    - border
    - border-radius
    - box-shadow
    - border-image

### 4. 颜色
    - opacity IE -> filter:alpha(opacity=50)   其他 -> opacity:.5
    - color
    - rgba

### -. 知识
    - line-height
    - hasLayout  BFC
    - rem em % 无单位