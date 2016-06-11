[在线预览](http://htmlpreview.github.com/?https://github.com/EPSON-LEE/Baidu_IFE/blob/master/Sesson1/Task2/index.html) 
## 任务目的

了解HTML的定义、概念、发展简史
掌握常用HTML标签的含义、用法
能够基于设计稿来合理规划HTML文档结构
理解语义化，合理地使用HTML标签来构建页面 

## 任务笔记

1. height:100%不起作用
问题：继承了之前的全局属性
CSS属性是有继承性的，而百分比都又是相对的，那么height：100%就是相当于容器父级而言的。所以并不是这个高度100%没有效果，只是没有达到我们预期的效果，我们理解上的错误。理解了高度100%的意义，剩下的就简单了，给body一个100%高度即可。

2. ``text-indext:2em`` 前两格子缩进 
3. ``text-align`` 设置文本的对齐方式
4. table 标签里面直接可以写样式
5. ``border-collapse: separate border-collapse: collapse``  将两条边框变为 border-collapse 属性设置表格的边框是否被合并为一个单一的边框，还是象在标准的 HTML 中那样分开显示。
6. ``border-spacing:2px``


7. 逻辑分区 ```<aside></aside>```
8. select用法
``<select>
    <option>上海</option>
    <option>北京</option>
</select>
``
<select>
    <option>上海</option>
    <option>北京</option>
</select>

9. border-radius 
10. ``display:inline-block`` 内部block外部inline
 
11.  在新的标签页打开href的方法是target="_blank"
 
 12. name id value的区别.