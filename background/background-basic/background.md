## Back - ground

- 요소의 배경에 이미지를 삽입하거나 색을 넣어줄 때 사용.

### 관련 속성들

#### background-color

```css
div {
    width: 300px;
    height: 300px;
    background-color: black;
    /* 배경 색 */
}
```
#### background-image

```css
div {
    background-image: url("이미지의 경로")
    /* div요소안에 배경으로 이미지가 들어감. 
    이미지가 반복되는게 기본값. */
}
```

##### background-image 와 관련된 속성들.

###### background-repeat

```css
div {
    width:300px;
    height:300px;
    background-image: url("삽입할 이미지 경로")
    background-repeat: no-repeat;
    /* 이미지 반복X  */
}
```

###### background-size

```css
div {
    width: 300px;
    height: 300px;
    background-image: url("삽입할 이미지 경로")
    background-size: contain;
    /* background-size 값으로 contain, cover, 직접설정(custom)이 있다. */
    /* contain: div 안에 이미지 요소가 전부 들어감
       cover: div요소에 빈칸이 없도록 이미지가 들어감 -> 이미지가 잘림
       custom: background-size: 300px 200px; 처럼 width값과 height값을 정할 수 있음 */
}
```

###### background-position

```css
div {
    width: 300px;
    height: 300px;
    background-image: url("삽입할 이미지 경로")
    background-position: center center;
    /* x값,y값으로 이미지의 위치 설정하고 %, px을 위치값으로 사용할 수 있다.*/
}
```


