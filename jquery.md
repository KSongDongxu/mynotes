####JQuery写法

``` (function($){})(jQuery) ```相当于匿名函数，形成闭包，内部定义的函数和变量只能在此范围内有效。

```$(function(){})```相当于```$(document).ready(function(){})```或```$(window).ready(function(){})```，在DOM加载完成之后执行那些预定义好的函数。

#### 判断checkbox是否选中

```javascript
<input type="checkbox" id="chk" name="chk" value="1" checked>
// 监听checkbox的change事件
$("#chk").change(function(){
  var checked = $("#chk").is(":checked");
  if(checked){
    console.log("checked");
  }else{
    console.log("cancel checked");
  }
});
```



