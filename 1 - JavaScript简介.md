# JavaScript简介

---

## JavaScript简史

1. 最初：处理服务器端语言负责的一些输入验证工作，校验表单
2. Netscape Navigator 2 脚本语言 LiveScript 改名为JavaScript
3. 微软在IE 3中加入JScript
4. 1997年，ECMA立标准 ： ECMAScript，此后，浏览器开发商将ECMAScript作为各自JavaScript实现的基础



## JavaScript实现

三个部分：ECMAScript、DOM、BOM（备注：BOM为浏览器对象模型）

1. ECMAScript：

   > 由ECMA-262定义，提供核心语言功能

   规定了：语法、类型、语句、关键字、保留字、操作符、对象

   版本进化：第一版：本质上与Netscape中的JavaScript1.1相同，并支持Unicode标准，支持多语言开发

   ​				  第二版：编辑加工的结果，目的是为了与ISO/IEC-16262保持一致，但无更新内容

   ​				  第三版：对标准第一次正式修改，修改字符串处理、错误定义、数值输出；新增正则、新控制语句、try-catch异常控制

   ​				  第四版：对语言进行全面检核修订。包含强类型变量、新语句、新数据结构、类、集成，并定义数据交互新方式

   ​				  第五版：包含原生JSON、继承方法、高级属性定义、严格模式等

2. 文档对象模型DOM：

   > 提供访问和操作网页内容的方法与接口

   针对XML但经过扩展，用于HTML的应用程序编程接口（API)。将整个页面映射为多层节点结构

   DOM级别：

   - DOM1：映射文档结构

   - DOM2：扩充鼠标和用户界面事件、范围、遍历，支持CSS

   - DOM3：DOM加载和保存模块：统一方式加载和保存文档的方法；

   ​				     DOM验证模块：新增文档方法

   其他DOM标准：SVG、MathML、DMIL

3. 浏览器对象BOM

   > 提供与浏览器交互的方法和接口

   BOM：可控制浏览器显示的界面以外的部分，但缺乏相关标准；（H5中解决该问题）

   BOM扩展：

   	- 弹出浏览器窗口
   	- 移动、缩放、关闭浏览器窗口
   	- 提供浏览器详细信息的navigator对象
   	- 提供浏览器所加载页面的详细信息的location对象
   	- 提供用户显示器分辨率详细信息的screen对象
   	- 支持cookie
   	- 类似XMLHttpRequest和IE的ActiveXObject的自定义对象

