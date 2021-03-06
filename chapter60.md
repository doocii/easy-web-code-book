第六十章 开始玩玩
===

当发生某个特定事件的时候，程序会做出相应的反应，那么就是程序对这一事件进行了响应。我们也说我们把某些代码绑定到了这一事件上。
那么现在我们就认识了单击和双击事件，当然还有很多其它的事件，但是因为用法基本一样，比较简单，我们就不再一一敷述，大家自行查看手册即可。

当然，其实在后面也是会不断涉及的。

 这不好玩！但是，再加上属性就有点意思了。其实真写起来你未必会在乎哪个是事件，哪个是属性的。来看我~~七十二变~~写个~~栗子~~例子。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>JQuery 的第一个测试</title>
    <script type="text/javascript" src="http://cdn.bootcss.com/jquery/3.0.0/jquery.min.js"></script>
    <script>
        $(document).ready(function(){
            $("button").click(function(){
                var text = $("#one").val();
                $("#two").val(text);
            });
        });
    </script>
</head>
<body>
    <input type="text" id="one">
    <input type="text" id="two">
    <button>点我试一下</button>
</body>
</html>
```

试试这个吧~我来教大家怎么玩。

![](http://coffee.zji.me/imgs/60-1.jpg)

打开之后有两个输入框和一个按钮，先在第一个输入框内输入任意文字，然后点击按钮试试看~

你会发现第一个输入框的内容被复制到了第二个输入框里。那么究竟发生了什么呢，我们一起来分析一下代码：

当按钮惨遭单击之后，依次发生了两件事情。第一件，获得当前 `#one` 元素的值，并存入变量 `text` 中。第二件，将 `#two`元素的值，设置为变量 `text` 的值。

所以， `val` 可以做两件事情，获取和设置。如果小括号里面是空的，则获取这个元素的值；否则，将小括号里的值设置给这个元素。

事情从此变得有意思起来了呢！

---

[**上一章**](chapter59) - [**目录**](index) - [**下一章**](chapter61)

---

**本书是收费的，不过交费凭自觉。**价格定义为每人请我喝一杯咖啡（哪种品质的咖啡随意），支付宝账号：

> **alay9999@163.com  （刘源）**

为了让大家阅读方便，本书将在如下站点发布，但最终内容以主站为准：

* 主站首发： http://coffee.zji.me/
* Gitbook: http://codeme.gitbooks.io/easy-web-code-book/
* 简书： http://www.jianshu.com/users/d37eaf3de0ff
* 站酷： http://www.zcool.com.cn/u/12927742

未经本人许可，禁止任何形式转载。相关事宜请联系： dms@zji.me