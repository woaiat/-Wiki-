 **`Complete Bootstrap 4.1.3 Notes`** 

这一章本质上讲的是一句话：

**如何不用自己从零写大量 CSS，而是直接用 Bootstrap 提供的类，快速做出响应式网页。**

你可以先把 Bootstrap 理解成：

* 一套现成的 CSS 工具箱
* 一套现成的页面组件库
* 一套帮助你快速布局的规则系统

---

## 1. 什么是 Bootstrap

### 定义 / 原理

Bootstrap 是一个  **免费、开源的 CSS 框架** ，最早由 Twitter 开发。

它提供：

* 响应式栅格系统
* 现成 UI 组件
* 一些 JavaScript 插件
* 跨浏览器的统一样式

### 文字化解释

如果没有 Bootstrap，你要自己写很多 CSS 才能做：

* 按钮样式
* 表单样式
* 导航栏
* 卡片
* 下拉菜单
* 响应式布局

如果用了 Bootstrap，很多时候只要加几个类名就行。

所以它的核心价值就是：

**省时间，风格统一，适合快速开发。**

---

## 2. Bootstrap 的核心思想

这一章开头给了几个很重要的概念。

### 2.1 Mobile-first

Bootstrap 是 **移动端优先** 的。

### 解释

意思不是“只能做手机网页”，而是说：

* 先按小屏幕设计
* 再逐步扩展到大屏幕

这是一种现代网页设计的常见思路。

---

### 2.2 12 栏栅格系统

Bootstrap 的布局核心是  **12 列 grid** 。

### 解释

一行被想象成 12 份。
你可以让元素占其中几份，比如：

* 占 4 列
* 占 6 列
* 占 12 列

这样就能灵活排版。

---

### 2.3 组件丰富

它内置了很多常见组件，比如：

* navbar
* forms
* cards
* dropdowns
* badges
* breadcrumb

### 解释

你不需要从零设计这些东西，直接套类名就能用。

---

## 3. Bootstrap 怎么引入

### 原理

要先把 Bootstrap 的 CSS 和 JS 引进页面，才能使用它的类和交互功能。

### 例子

```
<meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/css/bootstrap.min.css">
<script src="https://code.jquery.com/jquery-3.3.1.slim.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.3/umd/popper.min.js"></script>
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/js/bootstrap.min.js"></script>
```

### 解释

这里有几个关键点：

* `bootstrap.css`：负责样式
* `bootstrap.js`：负责交互组件
* `jQuery` 和 `Popper.js`：Bootstrap 4 的某些功能依赖它们
* `meta viewport`：确保网页在不同设备上缩放正常

### 例题

问：为什么 `viewport` 很重要？
答：因为它保证页面在手机、平板等不同设备上能正确响应式缩放。

---

## 4. 栅格系统 Grid System

这是第六章最重要的内容之一。

### 定义 / 原理

Bootstrap 的 grid 是基于 **flexbox** 的。
它用：

* `.row`
* `.col-*`

来控制布局。

### 文字化解释

你可以把它理解成：

* `row`：一整行
* `col`：这一行里的列

整行总共按 12 份分配。

---

### 4.1 断点 breakpoints

Bootstrap 用不同前缀来表示不同设备宽度。

* `.col-`：超小屏
* `.col-sm-`：`>=576px`
* `.col-md-`：`>=768px`
* `.col-lg-`：`>=992px`
* `.col-xl-`：`>=1200px`

### 解释

这表示“从这个宽度开始，用这个布局规则”。

比如：

```
<div class="col-md-4"></div>
```

意思是：

* 到了中等屏幕及以上，占 4 列
* 更小屏幕下，会自动堆叠或按默认规则显示

---

### 4.2 常见栅格类

* `.row`：一行
* `.col`：自动宽度列
* `.col-{breakpoint}-{number}`：指定列宽
* `.offset-{breakpoint}-{number}`：向右偏移
* `.order-{breakpoint}-{number}`：视觉顺序调整
* `.no-gutters`：去掉列间距

### 例子

```
<div class="row">
  <div class="col-md-4">col-md-4</div>
  <div class="col-md-4">col-md-4</div>
  <div class="col-md-4">col-md-4</div>
</div>
```

### 解释

这一行被分成三块，每块占 4 列，总共 12 列。

---

### 4.3 偏移 offset

```
<div class="row mt-3">
  <div class="col-md-6 offset-md-3 text-center">Centered with offset</div>
</div>
```

### 解释

* 元素本身占 6 列
* 向右偏移 3 列
* 所以它在中间

### 例题

问：如果你想让一个区域在 12 列里居中，占 6 列，最常见思路是什么？
答：`col-md-6 offset-md-3`

---

## 5. Typography 和文本工具类

### 定义 / 原理

Bootstrap 提供了一套统一的字体、行高、标题和文字工具类。

### 常见类

* `.display-1` 到 `.display-4`
* `.lead`
* `.text-muted`
* `.text-primary`
* `.text-success`
* `.text-danger`
* `.text-warning`
* `.text-uppercase`
* `.text-capitalize`
* `.font-weight-bold`
* `.font-italic`

### 例子

```
<h1 class="display-4">Display heading</h1>
<p class="lead">This paragraph uses .lead for emphasis.</p>
<p class="text-primary font-weight-bold">Primary bold text</p>
<p class="text-danger text-uppercase">danger uppercase alert</p>
```

### 解释

* `.display-4`：大号标题
* `.lead`：强调段落
* `.text-primary`：主色文字
* `.font-weight-bold`：粗体
* `.text-uppercase`：大写显示

### 例题

问：如果想让一段文字看起来更突出，常用哪个类？
答：`.lead`

---

## 6. 表单样式 Forms & Form Controls

### 定义 / 原理

Bootstrap 给表单做了统一美化。
你只要加类名，输入框、复选框、按钮就会更规范。

### 常见类

* `.form-control`
* `.form-control-lg`
* `.form-control-sm`
* `.form-group`
* `.form-check`
* `.form-check-input`
* `.form-inline`

### 例子

```
<div class="form-group">
  <label>Email</label>
  <input type="email" class="form-control" placeholder="name@example.com">
</div>

<div class="form-check">
  <input class="form-check-input" type="checkbox">
  <label class="form-check-label">Remember me</label>
</div>

<button class="btn btn-primary">Submit</button>
```

### 解释

* `.form-control`：最重要，给输入框统一样式
* `.form-group`：给表单项之间加合理间距
* `.form-check`：美化单选框/复选框结构
* `.form-inline`：表单横着排

### 例题

问：想让输入框自动变成 Bootstrap 风格，最关键的类是什么？
答：`.form-control`

---

## 7. Buttons、Button Groups、Badges

### 定义 / 原理

Bootstrap 通过按钮类和徽章类，让按钮和数量提示很容易做出来。

### 常见按钮类

* `.btn`
* `.btn-primary`
* `.btn-secondary`
* `.btn-success`
* `.btn-danger`
* `.btn-outline-*`
* `.btn-lg`
* `.btn-sm`
* `.btn-block`

### 按钮组

* `.btn-group`
* `.btn-group-vertical`

### 徽章

* `.badge`
* `.badge-pill`
* `.badge-primary`

### 例子

```
<button class="btn btn-primary">Primary</button>
<button class="btn btn-outline-danger">Outline Danger</button>
<button class="btn btn-success btn-sm">Small Success</button>

<div class="btn-group">
  <button class="btn btn-secondary">Left</button>
  <button class="btn btn-secondary">Middle</button>
</div>

<h3>Alerts <span class="badge badge-warning">3</span></h3>
```

### 解释

* `.btn` 是基础类
* 后面再加颜色类、大小类
* `.btn-group` 把多个按钮并成一组
* `.badge` 常用来显示数量提示

### 例题

问：如果你只写 `.btn-primary` 不写 `.btn`，规范上完整吗？
答：不完整，`.btn` 是基础类，通常要一起写。

---

## 8. Dropdowns 下拉菜单

### 定义 / 原理

Bootstrap 的 dropdown 是一个点击后展开菜单的组件。

### 关键依赖

它需要：

* Bootstrap JS
* jQuery
* Popper.js

### 常见类

* `.dropdown`
* `.dropdown-toggle`
* `.dropdown-menu`
* `.dropdown-item`
* `.dropdown-divider`
* `.dropup`
* `.dropright`

### 例子

```
<div class="dropdown">
  <button class="btn btn-secondary dropdown-toggle" type="button" data-toggle="dropdown">
    Dropdown
  </button>
  <div class="dropdown-menu">
    <a class="dropdown-item" href="#">Profile</a>
    <a class="dropdown-item" href="#">Settings</a>
    <div class="dropdown-divider"></div>
    <a class="dropdown-item" href="#">Logout</a>
  </div>
</div>
```

### 解释

* `.dropdown`：整体包起来
* `.dropdown-toggle`：触发按钮
* `.dropdown-menu`：菜单
* `.dropdown-item`：菜单项
* `.dropdown-divider`：分割线

### 例题

问：哪个属性常配合下拉触发按钮使用？
答：`data-toggle="dropdown"`

---

## 9. List Group 和 Input Group

### 9.1 List Group

用于显示一组列表内容。

### 常见类

* `.list-group`
* `.list-group-item`
* `.list-group-item-action`
* `.list-group-flush`

### 例子

```
<ul class="list-group">
  <li class="list-group-item active">Inbox <span class="badge badge-light">12</span></li>
  <li class="list-group-item">Sent</li>
</ul>
```

### 解释

这适合做消息列表、菜单列表、侧边列表。

---

### 9.2 Input Group

用于给输入框加前缀、后缀、按钮、图标等。

### 常见类

* `.input-group`
* `.input-group-prepend`
* `.input-group-append`
* `.input-group-text`

### 例子

```
<div class="input-group">
  <div class="input-group-prepend">
    <span class="input-group-text">@</span>
  </div>
  <input type="text" class="form-control" placeholder="username">
</div>
```

### 解释

这里输入框前面有个 `@`，很适合用户名、邮箱之类场景。

### 例题

问：如果想在输入框左边加一个固定符号，比如 `@`，应该想到哪个组件？
答：`input-group`

---

## 10. Navigation 和 Responsive Navbar

### 定义 / 原理

Navbar 是 Bootstrap 非常经典的组件，能自动适配不同屏幕宽度。

### 常见类

* `.navbar`
* `.navbar-brand`
* `.navbar-nav`
* `.nav-item`
* `.nav-link`
* `.navbar-toggler`
* `.collapse`
* `.navbar-collapse`
* `.navbar-expand-md`
* `.navbar-dark`
* `.navbar-light`
* `.ml-auto`
* `.mr-auto`

### 例子

```
<nav class="navbar navbar-expand-md navbar-dark bg-dark">
  <a class="navbar-brand" href="#">MyApp</a>
  <button class="navbar-toggler" data-toggle="collapse" data-target="#demoNav">
    <span class="navbar-toggler-icon"></span>
  </button>
  <div class="collapse navbar-collapse" id="demoNav">
    <ul class="navbar-nav ml-auto">
      <li class="nav-item active"><a class="nav-link" href="#">Home</a></li>
      <li class="nav-item"><a class="nav-link" href="#">Features</a></li>
    </ul>
  </div>
</nav>
```

### 解释

* `.navbar`：整体导航栏
* `.navbar-brand`：品牌名
* `.navbar-expand-md`：从 `md` 开始横向展开
* `.navbar-dark bg-dark`：深色导航栏
* `.navbar-toggler`：小屏幕折叠按钮
* `.collapse navbar-collapse`：折叠区域
* `.ml-auto`：菜单靠右

### 例题

问：哪个类控制“从什么屏幕尺寸开始横向展开”？
答：`.navbar-expand-{breakpoint}`

---

## 11. 图标：Font Awesome

### 原理

Bootstrap 4 自己 **不内置图标** ，所以课程里让你配合 Font Awesome 用。

### 例子

```
<i class="fas fa-home"></i> Home
<i class="fas fa-heart text-danger"></i> Like
<button class="btn btn-primary"><i class="fas fa-save"></i> Save</button>
```

### 解释

* `<i class="fas fa-home"></i>`：房子图标
* 可以和 Bootstrap 的颜色类、按钮类一起用

### 重点

你只要记住：

* Bootstrap 4 没内置图标
* 课程里常搭配 Font Awesome

---

## 12. Breadcrumb 面包屑导航

### 定义 / 原理

Breadcrumb 用来表示“当前页面在网站结构中的位置”。

### 常见类

* `.breadcrumb`
* `.breadcrumb-item`

### 例子

```
<nav>
  <ol class="breadcrumb">
    <li class="breadcrumb-item"><a href="#">Home</a></li>
    <li class="breadcrumb-item active">Bootstrap</li>
  </ol>
</nav>
```

### 解释

显示效果类似：
`Home / Bootstrap`

### 例题

问：面包屑最核心的两个类是什么？
答：`.breadcrumb` 和 `.breadcrumb-item`

---

## 13. Spacing Utilities 间距工具类

这一块考试很喜欢考，因为它很“规律化”。

### 定义 / 原理

Bootstrap 提供一套统一缩写来控制：

* 外边距 `margin`
* 内边距 `padding`

### 公式

```
{property}{sides}-{size}
```

### 解释

* `property`
  * `m`：margin
  * `p`：padding
* `sides`
  * `t`：top
  * `b`：bottom
  * `l`：left
  * `r`：right
  * `x`：左右
  * `y`：上下
* `size`
  * `0` 到 `5`
  * `auto`

### 例子

* `.mt-3`：上外边距
* `.px-4`：左右内边距
* `.mx-auto`：左右自动，常用于水平居中

### 例子代码

```
<div class="bg-light p-4 mb-3">Large padding + margin bottom</div>
<div class="bg-warning p-2 mx-auto text-center" style="max-width: 250px;">Centered block</div>
```

### 解释

* `p-4`：内边距较大
* `mb-3`：下外边距
* `mx-auto`：左右自动，居中块元素
* `text-center`：文字居中

### 例题

问：如果想让元素上边距增加，常用哪类写法？
答：`.mt-*`

问：如果想水平居中块元素，常见类是什么？
答：`.mx-auto`

---

## 14. 最小工作例子

这个例子能把主线串起来：

```
<div class="container">
  <div class="row mt-3">
    <div class="col-md-6 offset-md-3">
      <h1 class="display-4 text-center">Login</h1>
      <div class="form-group">
        <input type="text" class="form-control" placeholder="Username">
      </div>
      <button class="btn btn-primary btn-block">Submit</button>
    </div>
  </div>
</div>
```

### 你要看懂什么

* `container`：内容容器
* `row`：一行
* `col-md-6 offset-md-3`：中等屏幕下居中
* `display-4`：大标题
* `form-control`：输入框样式
* `btn btn-primary`：Bootstrap 按钮
* `btn-block`：按钮横向占满

---

## 15. 本章小结

本章最核心的一句话是：

**Bootstrap 是一套“靠类名快速搭界面”的前端框架。**

你现在最该记住的点：

* Bootstrap 是 CSS 框架
* 它是 mobile-first
* 栅格系统是 12 列
* `.row` + `.col-*` 是布局核心
* `.form-control` 是表单控件核心类
* `.btn` + 颜色类是按钮核心写法
* `.dropdown-*` 是下拉菜单核心
* `.navbar-*` 是导航栏核心
* `.breadcrumb` 是面包屑
* `m/p + 方向 + 数字` 是间距工具类规律
* Bootstrap 4 图标常配 Font Awesome

最简单总结一句：

**这一章是在学：如何不用自己写太多 CSS，而是直接用 Bootstrap 的现成类快速做响应式页面。**
