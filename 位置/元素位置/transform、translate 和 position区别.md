详细介绍 transform、translate 和 position 之间的关系与区别
1. position 属性
position 属性用于控制元素的位置。它定义了元素在文档流中的定位方式，并与其他定位相关属性（如 top、left、bottom 和 right）共同作用来决定元素的具体位置。

position 的常见值：
static（默认值）：元素按文档流自然布局，不受 top、left、right 和 bottom 的影响。
relative：元素相对于其原始位置进行偏移。设置了 top、left、right 或 bottom 后，元素会相对于其原始位置进行移动。
absolute：元素相对于最近的已定位父元素（即 position 为 relative、absolute 或 fixed 的父元素）进行定位。若没有已定位的父元素，则相对于 <html> 元素进行定位。
fixed：元素相对于浏览器窗口进行定位，不随页面滚动而变化。
sticky：结合了 relative 和 fixed 的特性，元素在滚动时会相对于其最近的滚动祖先进行定位。
2. transform 属性
transform 是一个强大的 CSS 属性，允许我们对元素进行2D或3D变换。通过 transform，我们可以对元素进行平移、旋转、缩放、倾斜等操作。

transform 不会影响元素的文档流（即不会影响其他元素的位置），它仅仅是在视觉上改变元素的外观和位置。
transform 可以组合多种变换效果，例如 rotate、scale、skew、translate 等。
transform 的常见值：
rotate(angle)：旋转元素，角度单位可以是 deg 或 rad。
scale(x, y)：缩放元素，x 和 y 是缩放的比例。
skew(x, y)：倾斜元素，x 和 y 是水平方向和垂直方向的倾斜角度。
translate(x, y)：平移元素，x 和 y 是元素在水平和垂直方向上的移动距离。
3. translate 属性
translate 是 transform 中的一种变换操作，用于移动元素。它可以沿着 X 和 Y 轴平移元素，并且不影响元素的原始位置（不会影响其他元素的位置或文档流）。

translate 只影响元素的视觉效果，并不会改变元素在页面中的位置或大小。
translate 接受两个参数：
translateX(x)：沿 X 轴平移 x 距离。
translateY(y)：沿 Y 轴平移 y 距离。
translate(x, y)：同时沿 X 和 Y 轴平移元素。
position 与 transform / translate 的区别与联系
position 是在页面布局时决定元素位置的方式，position 会影响元素在文档流中的位置。改变 position 会使元素在页面中重新排布。

transform 是对元素的可视效果进行操作，它不会影响元素的文档流，也不会改变其他元素的位置。使用 transform 可以让元素看起来移动、旋转、缩放，但它仍然保持在原始的布局位置。

translate 是 transform 中的一种变换操作，它本质上是一种“视觉平移”操作。使用 translate 可以让元素看起来移动，但它不会修改元素的实际位置或文档流。