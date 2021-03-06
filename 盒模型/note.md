# 盒模型

盒模型分为两种:

1. IE 盒模型,也叫作**怪异盒模型**
2. **标准盒模型**

## 怎么使用两种模型

默认情况下, 正常的盒子采用的是`box-sizing: content-box`**标准盒模型**
我们可以通过`box-sizing: border-box`来切换成为 **IE 盒模型**

## 两种盒模型的差别

两种盒模型的差别主要体现在宽高的计算上.

- 怪异盒模型: `width = content + padding + border`.
- 标准盒模型: `width = content`

> 这里我们需要注意的是,在怪异盒模型下,当我们增加了 padding 和 border 的宽度之后,content 的对应的宽度就会缩减.
>
> 关注点不同:
>
> - 怪异盒模型它会保持总体的 width 不变,而去调整 content 的大小. 他的关注点是总体的宽度
> - 标准盒模型,在 padding 或者 border 增加之后,整体宽度会对应增加,content 区域不变,所以它的关注点是在 content

## 行内元素和块级元素

### 常见的标签:

- 行内元素: span / img / a / strong / em / i
- 块级元素: div / p / h1~h6 / footer / ul / ol / li / section
- 行内盒元素: input / textarea / select

### 区别

1. 行内元素设置宽高无效 / 行内盒和块级元素都有效
2. 行内元素 margin,padding 只有左右有效,上下是无效的(准确来说 padding 的上下是只是不会挤压其他元素,所以在视觉上看着是不生效的,其实加了 border 之后能看出来是生效的) / 行内盒和块级元素都有效
3. 块级元素独占一行 / 行内元素和行内盒元素在一行内顺序排列,直到行慢之后才会换行
