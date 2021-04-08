# 在HTML中使用JavaScript

---

## 1. <script>元素

### 1.1 <script>属性

| 属性名称 | 定义                                             | 备注                                                         |
| -------- | ------------------------------------------------ | ------------------------------------------------------------ |
| async    | 可选；应立即下载脚本，但不应妨碍页面中其他操作   | 仅对外部脚本文件有效                                         |
| charset  | 可选；通过src属性指定的代码的字符集              |                                                              |
| defer    | 可选；脚本可以延迟到文档完全解析和显示之后再执行 | 仅对外部脚本文件有效                                         |
| language | 已废弃；表示编写代码使用的脚本语言               |                                                              |
| src      | 可选；包含要执行代码的外部文件                   |                                                              |
| type     | 必选；表示编写代码使用的脚本语言的内容类型       | 常规：text/javascript；<br/>非IE浏览器：application/javascript |



### 1.2 <script>使用方法

- 直接嵌入代码

  ```html
  <script type="text/javascript">
  	function foo() {
      alert('直接嵌入代码')
    }
  </script>
  ```

- 引用外部js文件

  ```html
  <script type="text/javascript" src="./example.js"></script>
  ```

- 注意：

  1. 直接嵌入代码时，使用的代码不能包含`</script>`字符串。可通过转义字符\解决：`alert("<\/script>")`
  2. es6中支持：`<script type="text/javascript" src="./example.js" />`
  3. 只要不存在async和defer属性，浏览器会按照<script/>元素在页面中出现的顺序对他们依次解析

-  `<script/>`标签位置：常规：`<head>`中，现代浏览器：`<body>`中，以加快解析速度



### 1.3 defer属性

- 定义：脚本会被延迟到，整个页面都解析后再运行（脚本立即下载，但延迟执行）

- 样例：

  ```html
  <script type="text/javascript" src="./example.js" defer="defer"></script>
  ```



### 1.4 async属性

- 定义：不让页面等待两个脚本下载和执行，从而异步加载页面其他内容。故建议异步脚本不要在加载期间修改DOM

- 备注：async并不保证按指定先后顺序执行

- 样例：

  ```html
  <script type="text/javascript" src="./example.js" async></script>
  ```

  

## 2. <noscript>元素 - 用在不支持JavaScript的浏览器中显示替代内容

```html
<noscript>
	<p>
    本页面需浏览器支持（启用）JavaScript。
  </p>
</noscript>
```

备注：浏览器支持JavaScript后，则该内容隐藏，不显示

