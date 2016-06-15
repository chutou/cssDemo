title: cssppt
speaker: zhouwenyong
url: https://github.com/ksky521/nodePPT
transition: slide3
files: /js/demo.js,/css/demo.css

[slide]

# css 趣味学习
## 分享人：周文勇

[slide]

# 简介

[slide]

## CSS(Cascading Style Sheets) 层叠样式表
----
* CSS目前最新版本为CSS3，是能够真正做到网页表现与内容分离的一种样式设计语言。相对于传统HTML的表现而言，CSS能够对网页中的对象的位置排版进行像素级的精确控制，支持几乎所有的字体字号样式，拥有对网页对象和模型样式编辑的能力，并能够进行初步交互设计，是目前基于文本展示最优秀的表现设计语言。CSS能够根据不同使用者的理解能力，简化或者优化写法，针对各类人群，有较强的易读性 {:&.rollIn}


[slide]

## 引入方法
----
* 外联式 {:&.rollIn}
<pre>
    <code>
        <link rel="stylesheet" href="styles/main.css">
    </code>
</pre>
* 嵌入式 
<pre>
    <code>
    <style type='text/css'>
        * {
            padding: 0;
        }
    </style>
    </code>
</pre>
* 内联式 
<pre>
        <p style="padding: 10px;">123456</p>
</pre>
* 优先级：内联式 > 嵌入式 > 外联式

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
        pre{ 
            white-space: pre-wrap!important;    /*保留空白，进行换行*/
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

# 选择符

[slide]

# 元素选择符
---
* 通配选择符: *{}  {:&.rollIn}
* 类型选择符: h1{}
* id选择符: #id{}
* 类选择符: .class{}

[slide]

# 关系选择符
---
* 包含选择符: E F { sRules}  {:&.rollIn}
<pre>
    <code>
        .demo div { border: 1px solid #fff;}
    </code>
</pre>
* 子选择符: E > F { sRules }
<pre>
    <code>
        .demo > div { border: 1px solid #fff; }
    </code>
</pre>
* 相邻选择符:  E+F { }
<pre>
    <code>
        p+p { color: red;}
    </code>
</pre>
* 兄弟选择符 E~F { sRules }
<pre>
    <code>
        .p~p { font-size: 36px;}
    </code>
</pre>

[slide]

# 属性选择符
---
* E[attr]: 选择具有att属性的E元素  {:&.rollIn}
<pre>
    <code>
        img[alt] { margin: 10px; }
    </code>
</pre>
* E[att="val"]： 选择具有att属性且属性值等于val的E元素。
<pre>
    <code>
        . input[type="text"]{ border: 1px solid #fff; }
    </code>
</pre>
* E[att~="val"]: 选择具有att属性（包含只有一个值且该值等于val的情况）
* E[att*="val"]：选择具有att属性且属性值为包含val的字符串的E元素
* E[att$="val"]：选择具有att属性且属性值为以val结尾的字符串的E元素

[slide]

# 伪类选择符
---
* E:link  {:&.rollIn}
* E:visited
* E:hover
* E:active
* E:focus

[slide]

# 伪对象选择符
---
* E:before 设置在对象前（依据对象树的逻辑结构）发生的内容。用来和content属性一起使用  {:&.rollIn}
* E:after 设置在对象后（依据对象树的逻辑结构）发生的内容。用来和content属性一起使用
* E::placeholder 设置对象文字占位符的样式
* E:first-letter 设置对象内的第一个字符的样式
* E:first-line 设置对象内的第一行的样式
* E::selection 设置对象被选择时的颜色

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
---
<pre>
    <code>
    <style>
        .relative1 {
          position: relative;
          border: 2px solid red;
        }
        .relative2 {
          position: relative;
          top: -20px;
          left: 20px;
          background-color: white;
          width: 500px;
          border: 2px solid green;
        }
    </style>
    <div class="relative1">
        relative 表现的和 static 一样，除非你添加了一些额外的属性。
    </div>
    <div class="relative2">
        在一个相对定位（position属性的值为relative）的元素上设置 top 、 right 、 bottom 和 left 属性会使其偏离其正常位置。其他的元素则不会调整位置来弥补它偏离后剩下的空隙。
    </div>
    </code>

</pre>

[slide]
## Z-index: 检索或设置对象的层叠顺序

[slide]
## float: 浮动
---
* clear: 清除浮动
<pre>
    <code>
        <style>
            nav {
              float: left;
              width: 200px;
            }
            section {
              margin-left: 200px;
            }
            .clearfix:after{
                content: ".";
                display: block;
                height: 0;
                clear: both;
                visibility: hidden;
            }
        </style>
        <!--<div class="clearfix">
            <nav>
            <ul>
              <li>
                <a href="float-layout.html">Home</a>
              </li>
              <li>
                <a href="float-layout.html">Taco Menu</a>
              </li>
              <li>
                <a href="float-layout.html">Draft List</a>
              </li>
              <li>
                <a href="float-layout.html">Hours</a>
              </li>
              <li>
                <a href="float-layout.html">Directions</a>
              </li>
              <li>
                <a href="float-layout.html">Contact</a>
              </li>
            </ul>
            </nav>
            <section class="elem elem-green">
                <p>
                  这个例子和之前那个外观一模一样。请注意我们在容器上做了“清除浮动”。原本在这个例子中是不需要的，但是当 <code>nav</code> 比非浮动的内容还要高时就需要了。
                </p>
            </section>
            <section class="elem elem-green ipsum">
                <p>
                  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus imperdiet, nulla et dictum interdum, nisi lorem egestas odio, vitae scelerisque enim ligula venenatis dolor. Maecenas nisl est, ultrices nec congue eget, auctor vitae massa. Fusce luctus vestibulum augue ut aliquet. Mauris ante ligula, facilisis sed ornare eu, lobortis in odio. Praesent convallis urna a lacus interdum ut hendrerit risus congue. Nunc sagittis dictum nisi, sed ullamcorper ipsum dignissim ac. In at libero sed nunc venenatis imperdiet sed ornare turpis. Donec vitae dui eget tellus gravida venenatis. Integer fringilla congue eros non fermentum. Sed dapibus pulvinar nibh tempor porta. Cras ac leo purus. Mauris quis diam velit.
                </p>
            </section>
        </div>-->
    </code>
</pre>

[slide]
## 百分比布局
---
<pre>
    <code>
        <style>
            nav {
              float: left;
              width: 25%;
            }
            section {
              margin-left: 25%;
            }
            .clearfix:after{
                content: ".";
                display: block;
                height: 0;
                clear: both;
                visibility: hidden;
            }
        </style>
        <!--<div class="clearfix">
            <nav>
            <ul>
              <li>
                <a href="float-layout.html">Home</a>
              </li>
              <li>
                <a href="float-layout.html">Taco Menu</a>
              </li>
              <li>
                <a href="float-layout.html">Draft List</a>
              </li>
              <li>
                <a href="float-layout.html">Hours</a>
              </li>
              <li>
                <a href="float-layout.html">Directions</a>
              </li>
              <li>
                <a href="float-layout.html">Contact</a>
              </li>
            </ul>
            </nav>
            <section class="elem elem-green">
                <p>
                  这个例子和之前那个外观一模一样。请注意我们在容器上做了“清除浮动”。原本在这个例子中是不需要的，但是当 <code>nav</code> 比非浮动的内容还要高时就需要了。
                </p>
            </section>
            <section class="elem elem-green ipsum">
                <p>
                  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus imperdiet, nulla et dictum interdum, nisi lorem egestas odio, vitae scelerisque enim ligula venenatis dolor. Maecenas nisl est, ultrices nec congue eget, auctor vitae massa. Fusce luctus vestibulum augue ut aliquet. Mauris ante ligula, facilisis sed ornare eu, lobortis in odio. Praesent convallis urna a lacus interdum ut hendrerit risus congue. Nunc sagittis dictum nisi, sed ullamcorper ipsum dignissim ac. In at libero sed nunc venenatis imperdiet sed ornare turpis. Donec vitae dui eget tellus gravida venenatis. Integer fringilla congue eros non fermentum. Sed dapibus pulvinar nibh tempor porta. Cras ac leo purus. Mauris quis diam velit.
                </p>
            </section>
        </div>-->
    </code>
</pre>

[slide]
## inline-block 布局
---
* vertical-align 属性会影响到 inline-block 元素，你可能会把它的值设置为 top 。
* 你需要设置每一列的宽度
* 如果HTML源代码中元素之间有空格，那么列与列之间会产生空隙

[slide]

## column 多列布局
---
<pre>
    <code>
        <style>
            .three-column {
              padding: 1em;
              -moz-column-count: 3;
              -moz-column-gap: 1em;
              -webkit-column-count: 3;
              -webkit-column-gap: 1em;
              column-count: 3;
              column-gap: 1em;
            }
        </style>
        <!--<section class="elem three-column ipsum">
            <div>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus imperdiet, nulla et dictum interdum, nisi lorem egestas odio, vitae scelerisque enim ligula venenatis dolor. Maecenas nisl est, ultrices nec congue eget, auctor vitae massa. Fusce luctus vestibulum augue ut aliquet. Mauris ante ligula, facilisis sed ornare eu, lobortis in odio. Praesent convallis urna a lacus interdum ut hendrerit risus congue. Nunc sagittis dictum nisi, sed ullamcorper ipsum dignissim ac. In at libero sed nunc venenatis imperdiet sed ornare turpis. Donec vitae dui eget tellus gravida venenatis. Integer fringilla congue eros non fermentum. Sed dapibus pulvinar nibh tempor porta. Cras ac leo purus. Mauris quis diam velit.
            </div>
        </section>-->
    </code>
</pre>

[slide]

## flexbox 弹性布局
---
<pre>
    <code>
        <style>
            .container {
              display: -webkit-flex;
              display: flex;
            }
            nav {
              width: 200px;
            }
            .flex-column {
              -webkit-flex: 1;
                      flex: 1;
            }
        </style>
        <!--<div class="container">
            <nav>
            <ul>
              <li>
                <a href="float-layout.html">Home</a>
              </li>
              <li>
                <a href="float-layout.html">Taco Menu</a>
              </li>
              <li>
                <a href="float-layout.html">Draft List</a>
              </li>
              <li>
                <a href="float-layout.html">Hours</a>
              </li>
              <li>
                <a href="float-layout.html">Directions</a>
              </li>
              <li>
                <a href="float-layout.html">Contact</a>
              </li>
            </ul>
            </nav>
            <div class="flex-column">
                <section class="elem elem-green">
                    <p>
                      这个例子和之前那个外观一模一样。请注意我们在容器上做了“清除浮动”。原本在这个例子中是不需要的，但是当 <code>nav</code> 比非浮动的内容还要高时就需要了。
                    </p>
                </section>
                <section class="elem elem-green ipsum">
                    <p>
                      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus imperdiet, nulla et dictum interdum, nisi lorem egestas odio, vitae scelerisque enim ligula venenatis dolor. Maecenas nisl est, ultrices nec congue eget, auctor vitae massa. Fusce luctus vestibulum augue ut aliquet. Mauris ante ligula, facilisis sed ornare eu, lobortis in odio. Praesent convallis urna a lacus interdum ut hendrerit risus congue. Nunc sagittis dictum nisi, sed ullamcorper ipsum dignissim ac. In at libero sed nunc venenatis imperdiet sed ornare turpis. Donec vitae dui eget tellus gravida venenatis. Integer fringilla congue eros non fermentum. Sed dapibus pulvinar nibh tempor porta. Cras ac leo purus. Mauris quis diam velit.
                    </p>
                </section>
            </div>
        </div>-->
    </code>
</pre>

[slide]
## @media 媒体查询
---
<pre>
    <code>
        <style>
            nav {
              display: inline-block;
              vertical-align: top;
              width: 25%;
            }
            .column {
              display: inline-block;
              vertical-align: top;
              width: 75%;
            }
            section {

            }
            .clearfix:after{
                content: ".";
                display: block;
                height: 0;
                clear: both;
                visibility: hidden;
            }
            
        </style>
        <!--<div class="clearfix">
            <nav>
            <ul>
              <li>
                <a href="float-layout.html">Home</a>
              </li>
              <li>
                <a href="float-layout.html">Taco Menu</a>
              </li>
              <li>
                <a href="float-layout.html">Draft List</a>
              </li>
              <li>
                <a href="float-layout.html">Hours</a>
              </li>
              <li>
                <a href="float-layout.html">Directions</a>
              </li>
              <li>
                <a href="float-layout.html">Contact</a>
              </li>
            </ul>
            </nav>
            <div class="column">
                <section class="elem elem-green">
                    <p>
                      这个例子和之前那个外观一模一样。请注意我们在容器上做了“清除浮动”。原本在这个例子中是不需要的，但是当 <code>nav</code> 比非浮动的内容还要高时就需要了。
                    </p>
                </section>
                <section class="elem elem-green ipsum">
                    <p>
                      Lorem ipsum dolor sit amet, consectetur adipiscing elit. 
                    </p>
                </section>
            </div>
        </div>-->
    </code>
</pre>
