# $().focus()와 $().blur()

### 1. $().focus()
1. 특정 요소에 강제로 포커스를 준다.
2. 클릭하여 포커스를 주었을 때 이벤트를 발생

### 2. $().blur()
1. 특정 요소에 강제로 포커스(초점)을 해제시킨다.
사용 예) 특정 요소 클릭 후 그 요소의 포커스 해제

``` javascript
$("#changepwd").on("click", function(){

    $("#changepwd").blur();
    //버튼 클릭 후 포커스가 남아있기 때문에 Enter 키(혹은 스페이스바) 눌렀을 때 또 실행이 되지 않도록 포커스를 해제함.
    ChangePassword();
});

```

2. 포커스 해제할 때 이벤트 발생
사용 예) 포커스를 해제할 때 팝업(경고창)을 보여주고 싶을 때 사용

``` javascript
$(document).ready(function(){
  $("input").blur(function(){
    alert("This input field has lost its focus.");
  });
});
```