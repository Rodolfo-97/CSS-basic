## Box - Sizing

- 기본적으로 width와 height는 content박스에 적용된다.

```css
.box {
    width: 200px;
    height: 200px;
    padding-top: 20px;
    padding-left: 30px;
}
```
- 위 코드는 가로 세로가 200px인 정사각형이 나오는 것이 아니라 세로가 220px 가로가 230px인 직사각형이 나온다.

    - box-sizing: content-box; 가 기본설정이기 때문에 width와 height가 박스 전체(padding과 border도 포함한 박스)에 적용되는 것이 아니라 content-box에만 적용된다.


### box 전체에 width와 height를 주는 방법

```css
* {
    box-sizing: border-box;
}
```
- box-sizing을 명시적으로 border-box로 설정해주면 padding과 border값까지 포함하여 width값과 height값이 적용된다. 
    
    - 앵간하면 css를 작성할 때 위 코드를 적어주도록 하자.