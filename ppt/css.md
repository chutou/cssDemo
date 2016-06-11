title: cssppt
speaker: zhouwenyong
url: https://github.com/ksky521/nodePPT
transition: slide3
files: /js/demo.js,/css/demo.css

[slide]

# css 趣味学习
## 分享人：周文勇

[slide]

# 基本属性

[slide]
## 尺寸
----
* width: 对象宽度 {:&.rollIn}
* height: 对象高度
* min-width: 对象最小宽度
* max-width: 对象最大宽度
* min-height: 对象最小高度
* max-height: 对象最大高度

[slide]
## 外补白
---
* margin: 设置对象外延的四周边距 {:&.fadeIn}
* margin-top: 外延顶部边距
* margin-left: 外延左边边距
* margin-right: 外延右边边跑
* margin-bottom: 外延底部边距

[slide]
## 内补白
---
* padding: 设置对内部边距的的四周边距 {:&.fadeIn}
* padding-top:内部边距的顶部边距
* padding-left:内部边距的左边边距
* padding-right:内部边距的右边边跑
* padding-bottom:内部边距的底部边距

[slide]
## 边框
---
* border: 复合属性 设置对象边框的特性 {:&.fadeIn}
* border-width: 对象边框宽度
* border-style: 对象边框样式
* border-color: 对象边框颜色
* border-radius: 对象使用圆角边框
* box-shadow: 检索对象阴影
* box-sizing: border-box padding和border被包含在定义的width和height之内。对象的实际宽度就等于设置的width值，即使定义有border和padding也不会改变对象的实际宽度，即 ( Element width = width )

[slide]
## 背景
---
* background: 复合属性 {:&.fadeIn}
* background-color: 背景颜色
* background-repeat: 背景填充
* background-image: 背景图像
* background-position: 背景位置
* background-size: 尺寸大小
    <pre>
        <code>
        background-image:url(test1.jpg),url(test2.jpg),url(test3.jpg);
        background-repeat:no-repeat,no-repeat,no-repeat;
        background-attachment:scroll,scroll,scroll;
        background-position:10px 20px,10px 20px,10px 20px;
        background-size:50px 60px,70px 90px,110px 130px;
        background-origin:content-box,content-box,content-box;
        background-clip:padding-box,padding-box,padding-box;
        background-color:#aaa;
        </code>
    </pre>

[slide]
## 色彩
---

* color: 文字颜色 {:&.rollIn}
* opacity: 透明度

[slide]

## 字体
---
* font: 复合属性 {:&.rollIn}
* font-style: 对象中的字体样式
* font-variant: 对象中的文本是否为小型的大写字母
* font-weight: 对象中的文本字体的粗细
* font-size: 对象中的字体尺寸
* font-family: 对象中文本的字体名称序列
<pre>
    <code>
        .font1 p{font:18px Simsun,arial,sans-serif;}
        .font2 p{font:italic 18px Simsun,arial,sans-serif;}
        .font3 p{font:italic small-caps 18px Simsun,arial,sans-serif;}
        .font4 p{font:italic small-caps bold 18px Simsun,arial,sans-serif;}
        .font5 p{font:italic small-caps bold 18px/2 Simsun,arial,sans-serif;}
    </code>
</pre>

[slide]
## 自定义字体
---
* @font-face:

<pre>
    <code>
        @font-face {
            font-family: 'diyfont';
            src: url('diyfont.eot'); /* IE9+ */
            src: url('diyfont.eot?#iefix') format('embedded-opentype'), /* IE6-IE8 */
                  url('diyfont.woff') format('woff'), /* chrome、firefox */
                              url('diyfont.ttf') format('truetype'), /* chrome、firefox、opera、Safari, Android, iOS 4.2+*/
                  url('diyfont.svg#fontname') format('svg'); /* iOS 4.1- */
        }
    </code>
</pre>

[slide]
## 文本
----
* text-align: 文本水平对齐方式 {:&.rollIn}
* white-space: 对象内空格的处理方式
* word-wrap: 当内容超过指定容器的边界时是否断行
* overflow-wrap: 设置或检索当内容超过指定容器的边界时是否断行
* word-break: 设置或检索对象内文本的字内换行行为
* text-indent: 检索或设置对象中的文本的缩进
* vertical-align: 对象内容的垂直对其方式
* line-height: 对象的行高
<pre>
    <code>
        pre{ white-space: pre-wrap!important;    /*保留空白，进行换行*/
            word-wrap: break-word!important;    /*连续字符换行*/
            /*white-space:normal!important;*/    /*忽略空白，进行换行*/
        }
    </code>
</pre>

[slide]
## 文本装饰
----
* text-decoration: 检索或设置对象中的文本的装饰 {:&.rollIn}
* text-shadow: 设置或检索对象中文本的文字是否有阴影及模糊效果
<pre>
    <code>
        a{
            text-decoration: none;
        }
    </code>
</pre>

[slide]
## 内容
----
* content: 用来和:after及:before伪元素一起使用，在对象前或后显示 {:&.rollIn}
* quotes: 设置或检索对象内使用的嵌套标记
<pre>
    <code>
        .string p:after{margin-left:-16px;background:#fff;content:"是";color:#f00;}
    </code>
    <div class="string">
        <p></p>
    </div>
</pre>

[slide]
## 表格
---
* border-collapse: 设置表格的行和单元格的边是合并在一起还是按照标准的HTML样式分开 {:&.rollIn}
* border-spacing: 设置当表格边框独立时，行和单元格的边框在横向和纵向上的间距
* empty-cells: 设置当表格的单元格无内容时，是否显示该单元格的边框

[slide]

# 布局

[slide]
## display
---
* block: 块级元素 {:&.rollIn}
* inline: 行内元素
* none: 隐藏，不会占位
* visibility: hidden还会保留占位空间

[slide]
## display
---
<pre>
    <code>
        display: none;
        display: inline;
        display: block;
        display: inline-block;
        display: contents;
        display: list-item;
        display: inline-list-item;
        display: table;
        display: inline-table;
        display: table-cell;
        display: table-column;
        display: table-column-group;
        display: table-footer-group;
        display: table-header-group;
        display: table-row;
        display: table-row-group;
        display: table-caption;
        display: flex;
        display: inline-flex;
        display: grid;
        display: inline-grid;
        display: ruby;
        display: ruby-base;
        display: ruby-text;
        display: ruby-base-container;
        display: ruby-text-container;
        display: run-in;

        /* Global values */
        display: inherit;
        display: initial;
        display: unset;
    </code>
</pre>

[slide]
## Position 定位方式
----
* static：此时4个定位偏移属性不会被应用 {:&.rollIn}
* relative：对象遵循常规流，并且参照自身在常规流中的位置通过top，right，bottom，left这4个定位偏移属性进行偏移时不会影响常规流中的任何元素
* absolute：对象脱离常规流，此时偏移属性参照的是离自身最近的定位祖先元素，如果没有定位的祖先元素，则一直回溯到body元素
* fixed：与absolute一致，但偏移定位是以窗口为参考。当出现滚动条时，对象不会随着滚动

[slide]
## Z-index: 检索或设置对象的层叠顺序


[slide]

# 封面样式2 {:&.flexbox.vleft}
## 左对齐

[slide style="background-image:url('/img/bg1.png')"]

## 使用背景

[slide]
## 使用.class/#id/自定义属性样式
----

```javascript
alert('nodeppt');
```

[slide]

## 主页面样式
### ----是上下分界线
----

nodeppt是基于nodejs写的支持 **Markdown!** 语法的网页PPT，当前版本：1.4.2

Github：https://github.com/ksky521/nodePPT
