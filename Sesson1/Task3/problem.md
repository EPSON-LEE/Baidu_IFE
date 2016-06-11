- 三栏布局 顺序的影响 中间放在最后 否则会出现中间栏把右侧栏挤下来
成因：[点击这里1](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Positioning/Understanding_z_index/Stacking_without_z-index)
     [点击这里](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Positioning/Understanding_z_index/Stacking_and_float)
overflow:hidden
现在已知正常元素先出现于浮动元素时 会出现被正常元素高度阻挡
一种貌似正确的解释为：
```
main放在中间，会占据这块的高度，下一个元素right的位置会在#main的下面
main放在后面的话，他前面的left和right都是浮动元素，脱离了文档流，所以#main的位置还与他们并排
```


- 三栏布局的三种方法：
1. 绝对定位：position
2. margin负值
3. 两侧float wrap overflow:hiddden 中间必须放在最后
不足在于：中间主体存在克星，clear:both属性。如果要使用此方法，需避免明显的clear样式。

- 宽度100%时候相对谁？？
相对父元素
如果大于100%则出父元素范围

- ``overflow:auto``与``overflow:hidden``
- BFC

## stacking context（堆叠上下文） ##
- 渲染方式
1. 不适用Z-index 默认情况 是从bottom到top中
2. 正常流中非定位后代元素（这些元素顺序按照HTML文档出现顺序）
3. 已定位后代元素（这些元素顺序按照HTML文档出现顺序）
解释一下后两条规则：

- 浮动堆叠顺序
1. 浮动元素z-index位置介于非定位元素和定位元素之间。（从下到上）
2. 浮动元素(浮动元素之间是不会出现z-index重叠的)
min-width
