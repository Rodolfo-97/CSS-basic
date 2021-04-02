## Web-font

- 폰트를 쓰기 위해서는 2가지 방법이 있다

### 갖다 쓰기

```html
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link href="https://fonts.googleapis.com/css2?family=Nanum+Pen+Script&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="style.css">
</head>
```

- head 태그 안에 link 태그로 사용할 폰트 주소를 연결 해주기만 하면 됨.

```css
body {
    font-family: 'Nanum Pen Script', cursive;
}
```

- css에 font를 사용한다고 선언해 주어야함.

### 직접 제공하기

- 생각보다 복잡함으로 필요시 공부 ㄱㄱ