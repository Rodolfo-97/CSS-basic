## Box-Model


![CSS-Box_Model](./box.png)

- 내용(content) : 텍스트나 이미지가 들어있는 박스의 실질적인 내용 부분. 

- 패딩(padding) : 내용과 테두리 사이의 간격. 패딩은 눈에 보이지 않는다.

- 테두리(border) : 내용와 패딩 주변을 감싸는 테두리.

- 마진(margin) : 테두리와 이웃하는 요소 사이의 간격. 마진은 눈에 보이지 않음.

### 위 이미지에 해당하는 부분을 구현부에 적어주면 box를 조정할 수 있음.

#### margin을 왼쪽을 10px 주고 싶을 때

```css
    .box {
        margin-left: 10px;
    }
```


### 속기형

- 시계 방향으로 속성값을 적어주면됨
    - top -> right -> bottom -> left

```css
.box {
    padding: 10px 20px 30px 40px;
}
```

- margin, border도 같은 방법으로 작성가능.

```css
.box {
    padding: 10px 20px;
}
```

- 위의 코드와 같이 top, right의 값만 준다면 bottom은 top의 값으로 left는 right의 값으로 자동으로 설정됨.
    - **top과 bottom, right와 left는 세트임!!**


### border

- 반드시 굵기, 선의종류, 선의색깔에 대한 속성을 적어주어야 한다.

```css
.box {
    border: 1px solid black;
}
```