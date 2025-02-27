box-sizing 是 CSS 中用于控制元素的宽度和高度计算方式的属性。它有两个常用的值：content-box 和 border-box。理解这两者的区别可以帮助你更好地控制元素的布局。

1. box-sizing: content-box（默认值）
在 content-box 模式下，元素的宽度和高度只包括内容区，不包括内边距和边框。

2. box-sizing: border-box
在 border-box 模式下，元素的宽度和高度包括内容区、内边距和边框，也就是说，设置的宽度和高度会包含所有这些部分。


为什么 box-sizing: border-box 更加常用？
box-sizing: border-box 是响应式设计和布局中非常重要的特性。它使得在设置 width 和 height 时，元素的边框和内边距都已经计算在内，避免了布局错位或尺寸计算出错的情况。大多数前端开发者在进行布局时都会使用 border-box 来确保更容易控制元素的尺寸。

例如，很多 UI 框架（如 Bootstrap）都默认使用 box-sizing: border-box 来简化布局计算。