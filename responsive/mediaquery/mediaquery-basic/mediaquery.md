## Responsive Web

- 디바이스의 화면 크기에 따라 웹이 다르게 보이도록 한 웹 사이트를 말한다.


### 반드시 하는 2가지 작업

#### HTML

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

- html의 head 태그 안에 반드시 해당 코드를 적어주어야 한다.
    -  html 요소들이 화면의 크기에 따라 다르게 보임.


#### CSS

```css
@media screen and (min-width: 768px) {
    /* 화면 폭이 최소 768px 이상 일때 보여줄 웹사이트의 style 구현 */
}
```

### 반응형 웹 사이트를 만들 때엔 모바일부터 시작하도록 한다.

