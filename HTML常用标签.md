# HTML 重点标签
## 1、a 标签

a标签是超链接，a是anchor的缩写。

**作用**：利用a标签，可以跳转到外部页面、内部的锚点以及跳转到邮箱或电话等。

### 1.1语法：

```
<a href="跳转目标" target="目标窗口的弹出方式">文本或图像</a>
```

注： <a>标签内部不仅可以放置文字，也可以放置段落、文字、图片等其他元素。

### 1.2属性：

#### href：链接目标地址

（h-hyper ref-reference）

href的取值：

##### 1). 网址

- https:// google.com
- http:// google.com
- //google.com (无协议网址)

三个都可以，建议选无协议网址。

##### 2). 路径

- /a/b/c.html 以及 a/b/c.html（相对路径和绝对路径。）

##### 3). 伪协议

- javascript:代码;
- mailto:邮箱
- tel:电话

##### 4). id

指向内部锚点

```
<h1 id="xxx">胡歌</h1>
<!-- 点击链接会跳转到胡歌 -->
<a href="#xxx">查看胡歌</a>
```



#### target：链接页面的打开方式

|  取值   | 描述                               |
| :-----: | :--------------------------------- |
|  _self  | 在当前窗口打开，是target的默认值   |
| _blank  | 在新窗口打开                       |
|  _top   | 有两个窗口才有作用，在顶级窗口打开 |
| _parent | 上层窗口打开                       |

- download：下载页面

此属性指示浏览器下载页面，但不是所有浏览器都支持，不好用。

## 2、img 标签

简单介绍：

图像标签，是image的缩写。

### 2.1语法：

```
<img src="图像URL" alt="替换文本" title="图片标题"/>
```

### 2.2属性：

|  属性  | 描述                                                 |
| :----: | :--------------------------------------------------- |
|  src   | 图像的路径，source的缩写，必要属性，其他属性可省略。 |
| title  | 鼠标悬停时显示的文本内容                             |
|  alt   | 图像不能显示时的替换文本                             |
| width  | 图片宽度                                             |
| height | 图片高度                                             |

**注意：**

高度和宽度只设置一个，不然会变形，设置任意一个，另一个属性会按照比例自适应。

## 3、table 标签

### 3.1简单介绍：

表格标签，可以用来展示表格式数据。

分为表格头部<thead>，表格正文<tbody>，表格尾部<tfoot>。

- `<tr>`是表示表格中的一行，嵌套在<thead>、<tbody>、<tfoot>的里面，包含<th>、<td>

- `<th>`、`<td>`用来定义表格的单元格，`<th>`是标题单元格，`<td>`是数据单元格。

```
 <table>
      <!-- 这是头部 -->
      <thead>
        <tr>
          <th>XXX</th> 
        </tr>
      </thead>  
      <!-- 这是正文 -->
      <tbody>
        <tr>
          <td>XXX</td>
        </tr>
      </tbody>
      <!-- 这是尾部 -->
      <tfoot>
        <tr>
          <td>XXX</td>
        </tr>
      </tfoot>
    </table>
```

### 3.2属性

- table-layout

  取值：

  - auto

  表格及单元格的宽度取决于其包含的内容。

  - fixed

  表格每列基本等距分布。

- border-spacing

单元格边框间的距离，实际应用常会设置为0。

- border-collapse
  用来决定表格的边框是分开的还是合并的。在分隔模式下，相邻的单元格都拥有独立的边框。在合并模式下，相邻单元格共享边框。 

  取值：

  - `collapse`

  相邻的单元格共用同一条边框。

  - `separate`

  默认值。每个单元格拥有独立的边框。

### 3.3示例：

```
<style>
      table,
      td,
      th {
        border: 1px solid black;
        text-align: center;
        border-collapse: collapse;
      }
      table {
        width: 500px;
        height: 200px;
      }
    </style>
  </head>
  <body>
    <table>
      <thead>
        <caption>
          <h3>小说排行榜</h3>
        </caption>
      </thead>
      <tbody>
        <tr>
          <th>排名</th>
          <th>关键词</th>
          <th>今日搜索</th>
          <th>最近七日</th>
        </tr>
        <tr>
          <td>1</td>
          <td>鬼吹灯</td>
          <td>345</td>
          <td>134523</td>
        </tr>
        <tr>
          <td>2</td>
          <td>盗墓笔记</td>
          <td>124</td>
          <td>23853</td>
        </tr>
        <tr>
          <td>3</td>
          <td>斗罗大陆</td>
          <td>212</td>
          <td>23423</td>
        </tr>
      </tbody>
    </table>
  </body>
```

#### 效果展示：

![image-20210121232634740](../../../AppData/Roaming/Typora/typora-user-images/image-20210121232634740.png)