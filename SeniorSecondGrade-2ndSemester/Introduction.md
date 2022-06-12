# SeniorSecondGrade 2st Semester
<div style="text-align:right;color:white;font-size:18px"><b>——高二第二学期</b></div>

[toc]

## Introduction
<div style="text-align:right;color:white;font-size:16px"><b>——介绍</b></div>

经过上一学期的测试，摸索出部分规则，暂时写在下面，可以随时进行补充。

---

用`<script>document.write("<p id=e><e>"+"—".repeat(72)+"</e></p>")</script>`分割每个单元，取代了之前的序号标注单元。

具体效果：

<script>document.write("<p id=e><e>"+"—".repeat(72)+"</e></p>")</script>

使用案例：

```md
XXX

<script>document.write("<p id=e><e>"+"—".repeat(72)+"</e></p>")</script>

YYY
```

> 此法明显优于「序号法」的一个地方就是自定义的空间多了，不像「序号法」一样受序号的拘束；且序号一旦错乱修改起来极为麻烦；同时也更加美观。
> 但也是存在缺陷的：在源码区占据了很多空间，使文本大小「虚高」，~~也不美观（曾采用 Conceal 插件来解决这个问题，但是 Conceal 只能做到显示替换，并不能做到将占据两三行的 HTML 显示为一行，吃过很多亏）~~[^00-1]已改进，现在只会显示为一行（但还需要配备 `style.less` 文件，可移植性 $-\infty$ ）；转成 HTML 后偏短，美观只局限在编辑器中；可移植性差（尝试过去给 Markdown 语法添加一个简写方式，但始终没能看懂，最终不了了之，还是采用这样的方法）；编辑器中无法显示（刷新时可以看见，HTML 也可以看见）且没有占位。

> 原分割线为`<div style="text-align:center;padding-bottom:20px;"><code>————————————————————————————————————————————————————————————————————————</code></div>`
> 具体效果：

<div style="text-align:center;padding-bottom:20px;"><code>————————————————————————————————————————————————————————————————————————</code></div>

---

脚注格式为`[^Week-Num]`，Week 为周号码，Num 为该周脚注序号。

具体效果：

测试[^00-0]

使用案例：

```md
XXX[^00-01]XXXX
YYYY[^00-02]YYY

[^00-01]: AAA
[^00-02]: BBB
```

## Notes
<div style="text-align:right;color:white;font-size:16px"><b>——笔记</b></div>

## Others
<div style="text-align:right;color:white;font-size:16px"><b>——其他</b></div>

[^00-0]: 测试脚注
[^00-1]: 编写本文当日改进，花了两个小时。。。