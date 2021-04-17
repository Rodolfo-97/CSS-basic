## block 박스(영역) 
- 다른 요소들이 옆에 오지 못하게 길막한다!
- layout을 잡을 떄 **영역-면**을 담당.

### 특징

1. 따로 width값을 지정해주지 않을 경우 부모의 content-box의 100%.</br>
2. width 값을 지정한 경우 남은 공간은 자동으로 margin으로 채워짐.(개발자 도구에서는 나타나지 않음)</br>
3. 부모요소에게 별도의 height값을 지정해주지 않을 경우 자식요소의 height의 합이 부모요소의 height값임.
    - 자식요소에게 margin이 있다면 그 값도 합친것이 부모의 height값이다. </br>
4. 영역을 담당하기 때문에 width, height, padding, border, margin 등 box-model의 속성 전부 사용가능 </br>
   
### 코드 설명

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .child {
            background-color: blue;
            width: 200px;
            /* 200px을 제외한 공간이 magin으로 채워진다. */
            height: 200px;
            margin-left: auto;
            /* 자동으로 생긴 마진을 왼쪽으로 전부 보낸다. */
            margin-right: auto;
            /* 자동으로 생긴 마진을 오른쪽으로 전부 보낸다. */
            /* margin: 0 auto; ->  left, right 값을 둘다 auto로 주면 좌우정렬됨. */
        }
        .other {
            background-color: brown;
            width: 200px;
            height: 200px;
            margin: 0 auto;
            /* top과 bottom은 0,  좌우는 가운데로 정렬된다. */
        }
    </style>
</head>
<body>
    <div class="parent">
        <div class="child">child</div>
        <div class="other">other</div>  
    </div>
</body>
</html>
```
- parent의 height 속성값을 지정하지 않은 경우 자동이로 자식요소의 height 값의 합인 400px이 된다.
- parent도 body의 자식요소로 볼 수 있기 때문에 이 코드에서는 parent의 width 값은 body요소의 width 값과 일치한다.

