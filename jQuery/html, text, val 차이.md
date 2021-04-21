# html(), text(), val() 차이

### 1. $().html() vs $().text()
내용을 가져오거나, 내용을 다시 넣는 메소드. 태그 처리가 다름

html()으로 내용을 가져올 때는 태그 포함해서 가져오고, text()으로 내용을 가져올 때는 텍스트만 가져옴


html()으로 내용을 넣을 때는 태그가 html로 인식,text()으로 내용을 넣을 때는 태그가 텍스트로 인식


사용 예1) 

id="html"에는 **태그 인식**으로, id="text"에는 __&lt;p&gt;태그 인식&lt;&#47;p&gt;__ 으로 출력
``` javascript
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>jQuery</title>
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <script>
    $( document ).ready( function() {
        var Tag = "<p>태그 인식</p>";
        $("#html").html(Tag);
        $("#text").text(Tag);
    });
    </script>

</head>
<body>
    <div id="html" style="border-width: 1px;border-style: solid;border-color: red;"></div>
    <br/>
    <div id="text" style="border-width: 1px;border-style: solid;border-color: blue;"></div>
</body>
</html>
```

### 2. $().val()
값을 가져오거나 값을 설정하는 메소드. 주로 input에 쓰임


사용 예1) 

id가 Notice인 element의 value를 가져와서 콘솔 출력
``` javascript
var Notice = $("#Notice").val();
console.log(Notice);
```



사용 예2) 

id가 Notice인 element의 value를 점검 중으로 설정
``` javascript
$("#Notice").val("점검 중");
```



사용 예2-2)
``` javascript
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>jQuery</title>
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <script>
    $( document ).ready( function() {
        var Notice = $("#Notice").val("점검 중");
    });
    </script>
</head>
<body>
    <input type="text" id="Notice" value = "">
</body>
</html>
```

### 3. 응용 버전 

예) input 태그 value에 HTML Entity를 decoding 해야할 경우 방법(오늘 해결한 문제)
``` javascript
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>jQuery</title>
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <script>
    $( document ).ready( function() {

        var Tag = "HTML Entity: &lt; &gt; &amp;";

        $('#Notice1').val($("#Notice1").html(Tag).text());

    });
    </script>

</head>
<body>
    <input type="text" id="Notice1" value = "">
</body>
</html>
```