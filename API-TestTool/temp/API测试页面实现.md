+ [上一章 请求类型按钮功能实现](请求类型按钮功能实现.md)  

### <a id="catlog">API测试页面实现</a>
<a href="#p1"><font size=3 color=blue>-设置路由和视图函数</font></a>  
<a href="#p2"><font size=3 color=blue>-设置菜单链接</font></a>   
<a href="#p3"><font size=3 color=blue>-实现模板文件：请求区域</font></a>  
<a href="#p4"><font size=3 color=blue>-实现模板文件：响应区域</font></a>
---

+ + ##### <a id="p1" href="#catlog">-设置路由和视图函数</a>
+ + + + ![avatar](https://github.com/deadGeeker/django_API_TestTool/blob/main/API-TestTool/temp/image/50.png)
---

+ + ##### <a id="p2" href="#catlog">-设置菜单链接</a>
+ + + + ![avatar](https://github.com/deadGeeker/django_API_TestTool/blob/main/API-TestTool/temp/image/51.png)

---

+ + ##### <a id="p3" href="#catlog">-实现模板文件：请求区域</a>
+ + + + 定基本框架，将页面的内容展示分为请求区域和响应区域
+ + + + ![avatar](https://github.com/deadGeeker/django_API_TestTool/blob/main/API-TestTool/temp/image/52.png)
---
+ + + + 请求区域实现
+ + + + ![avatar](https://github.com/deadGeeker/django_API_TestTool/blob/main/API-TestTool/temp/image/53.png)
+ + + + 请求类型数据实现数据库到模板文件的传输
+ + + + ![avatar](https://github.com/deadGeeker/django_API_TestTool/blob/main/API-TestTool/temp/image/55.png)
+ + + + 实现模板文件内调用请求类型数据
+ + + + ![avatar](https://github.com/deadGeeker/django_API_TestTool/blob/main/API-TestTool/temp/image/56.png)
+ + + + 实现模板文件内选择功能，下拉选项中的请求类型点击后能够同步到请求类型字段处。
+ + + + ![avatar](https://github.com/deadGeeker/django_API_TestTool/blob/main/API-TestTool/temp/image/57.png)
+ + + + ![avatar](https://github.com/deadGeeker/django_API_TestTool/blob/main/API-TestTool/temp/image/58.png)
---
+ + + + 请求参数显示处理
+ + + + 请求参数字段只有类型为POST时才需要显示，其余类型无需显示请求参数字段
+ + + + ![avatar](https://github.com/deadGeeker/django_API_TestTool/blob/main/API-TestTool/temp/image/59.png)
+ + + + 发送请求按钮功能实现，对发送请求按钮添加 onclick 事件
+ + + + ![avatar](https://github.com/deadGeeker/django_API_TestTool/blob/main/API-TestTool/temp/image/61.png)
+ + + + 实现 onclick 事件 send_request() 函数
+ + + + ![avatar](https://github.com/deadGeeker/django_API_TestTool/blob/main/API-TestTool/temp/image/60.png)
---
+ + + + 请求地址校验
+ + + + 这里用到了JavaScript中的test()方法，test()方法用于检测一个字符串是否匹配某个模式，可以将请求地址视为一个字符串。
+ + + + 对请求地址添加 id 属性
+ + + + ![avatar](https://github.com/deadGeeker/django_API_TestTool/blob/main/API-TestTool/temp/image/62.png)
+ + + + 新建 isURL() 函数对请求地址合法性进行校验
+ + + + 如果请求地址错误，则提示错误信息。反之则执行下一行代码。
+ + + + ![avatar](https://github.com/deadGeeker/django_API_TestTool/blob/main/API-TestTool/temp/image/63.png)
+ + + + ![avatar](https://github.com/deadGeeker/django_API_TestTool/blob/main/API-TestTool/temp/image/64.png)
---
+ + + + 请求头信息校验
+ + + + 对请求头信息添加 id
+ + + + ![avatar](https://github.com/deadGeeker/django_API_TestTool/blob/main/API-TestTool/temp/image/65.png) 
+ + + + 校验手段是检测请求头信息是不是JSON格式，新建isJSON()函数和isHeader函数
+ + + + ![avatar](https://github.com/deadGeeker/django_API_TestTool/blob/main/API-TestTool/temp/image/66.png)
+ + + + ![avatar](https://github.com/deadGeeker/django_API_TestTool/blob/main/API-TestTool/temp/image/67.png)
---
+ + + + 请求参数校验
+ + + + 对请求参数添加 id
+ + + + ![avatar](https://github.com/deadGeeker/django_API_TestTool/blob/main/API-TestTool/temp/image/68.png)
+ + + + 新建 isParameter() 函数检测请求参数是否合法
+ + + + ![avatar](https://github.com/deadGeeker/django_API_TestTool/blob/main/API-TestTool/temp/image/69.png)
+ + + + ![avatar](https://github.com/deadGeeker/django_API_TestTool/blob/main/API-TestTool/temp/image/70.png)
---
+ + ##### <a id="p4" href="#catlog">-实现模板文件：响应区域</a>
+ + + + 响应区域实现
+ + + + ![avatar](https://github.com/deadGeeker/django_API_TestTool/blob/main/API-TestTool/temp/image/54.png)
+ + + + 响应区域页面实现，点击响应区域三个按钮后能够分别显示对应的展示区域
+ + + + ![avatar](https://github.com/deadGeeker/django_API_TestTool/blob/main/API-TestTool/temp/image/71.png)
+ + + + ![avatar](https://github.com/deadGeeker/django_API_TestTool/blob/main/API-TestTool/temp/image/72.png)

+ + + + 响应区域数据展示
+ + + + 将响应结果放置到响应区域对应的位置
+ + + + ![avatar](https://github.com/deadGeeker/django_API_TestTool/blob/main/API-TestTool/temp/image/73.png)
+ + + + ![avatar](https://github.com/deadGeeker/django_API_TestTool/blob/main/API-TestTool/temp/image/74.png)
---
+ [下一章 已存测试页面实现](已存测试页面实现.md)  
