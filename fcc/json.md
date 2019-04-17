# Get JSON with the jQuery getJSON Method 

使用jQuery getJSON方法获取JSON

$.getJSON("/json/cats.json", function(json) {
  $(".message").html(JSON.stringify(json));
});







# Convert JSON Data to HTML

将JSON数据转换为HTML



json.forEach(function(val) {
  var keys = Object.keys(val);
  html += "<div class = 'cat'>";
  keys.forEach(function(key) {
    html += "<b>" + key + "</b>: " + val[key] + "<br>";
  });
  html += "</div><br>";
});









{"id":0,

"imageLink":"/images/funny-cat.jpg",

"codeNames":["Juggernaut","Mrs. Wallace","Buttercup"]},





{"id":1,"imageLink":"/images/grumpy-cat.jpg","codeNames":["Oscar","Scrooge","Tyrion"]},{"id":2,"imageLink":"/images/mischievous-cat.jpg","codeNames":["The Doctor","Loki","Joker"]}









# Render Images from Data Sources



渲染来自数据源的图像

<script>
  $(document).ready(function() {

    $("#getMessage").on("click", function() {
      $.getJSON("/json/cats.json", function(json) {

        var html = "";
    
        json.forEach(function(val) {
    
          html += "<div class = 'cat'>";
    
          // 请把你的代码写在这条注释以下
            
         //html+="<img src="+val.imageLink+">"
          html += "<img src = '" + val.imageLink + "'>";
          
          // 请把你的代码写在这条注释以上
    
          html += "</div>";
    
        });

        $(".message").html(html);

      });
    });
  });





# Prefilter JSON

预滤器JSON





<script>
  $(document).ready(function() {

    $("#getMessage").on("click", function() {
      $.getJSON("/json/cats.json", function(json) {

        var html = "";
    
        // 请把你的代码写在这条注释以下
        
        json=json.filter(function(val){
          return val.id!==1;
        })
        
        // 请把你的代码写在这条注释以上
    
        json.forEach(function(val) {
    
          html += "<div class = 'cat'>"
    
          html += "<img src = '" + val.imageLink + "'>"
    
          html += "</div>"
    
        });

        $(".message").html(html);

      });
    });
  });



# Get Geolocation Data

获取地理位置数据

我们还可以通过浏览器`navigator`获得我们当前所在的位置`geolocation`。

位置的信息包括经度`longitude`和纬度`latitude`。

你将会看到一个是否允许获取当前位置的提示。不管你选择允许或者禁止，只要代码正确，这关就能过了。

如果你选择允许，你将会看到右侧手机输出的文字为你当前所在位置的经纬度。

代码如下：

> if (navigator.geolocation) {
>   navigator.geolocation.getCurrentPosition(function(position) {
>     $("#data").html("latitude: " + position.coords.latitude + "<br>longitude: " + position.coords.longitude);
>   });
> }

