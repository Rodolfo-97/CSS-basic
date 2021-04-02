## Typography

- text를 디자인할 때 사용하는 속성이다.
- 
### 중요한 속성 정리

```css
.text {
    font-size: 1px;
    /* text 크기 */
    line-height: 2;
    /* 줄 간격 */
    letter-spacing: 2em;
    /* text끼리의 자간 */
    font-family: 글꼴1, 글꼴2, serif;
    /* 글꼴, 해당 글꼴이 없을 경우 순서대로 대체. */
    font-weight: 400;
    /* text 굵기 */
    color: (0, 0, 0, 0.5);
    /* text 색 */
}
```

#### 단위

- px(절대 단위)

- em(상대 단위)
    - text에 적용된 font-size 기준. 
- rem(상대 단위)
    - text에 html 태그에 적용된 font-size 기준.

#### 각 속성들의 특징

- line-height
    - 주로 em 을 생략하여 숫자만 적어준다.
    - text는 항상 줄 간격의 가운데에 위치한다.

- letter-spacing
    - line-height와 마찬가지로 em을 주로 사용하지만 생략하지 않는다.

- font-weight
    - 100씩 조절
    - 400은 regular, 700은 bold이다.(기준으로 생각)

- color
    - hex, rgb, rgba 방식으로 값을 줄 수 있다.
        - rgba의 a는 투명도를 조절한다.

### 기타 속성

```css
.text {
    text-align: center;
    /* 정렬 */
    text-indent: 50px;
    /* 문단의 시작부분 들여쓰기 */
    text-transform: capitalize;
    /* text의 대문자-소문자 변경 */
    text-decoration: none;
    /* text에 줄을 긋거나 없앨 때 사용 */
    font-style: italic;
    /* text를 기울게함 */
}
```

#### 각 속성의 값들

- text align
    - left, center, right

- text-transform
    - capitalize: 모든 단어의 앞글자를 대문자로 변경
    - uppercase: 모든 text를 대문자로 변경
    - lowercase: 모든 text를 소문자로 변경

- text-decoration
    - none: 밑줄을 없앰(주로 a태그에 사용)
    - 나머지 속성값은 필요할 때 검색 ㄱㄱ

- font-style
    - normal: 기울기를 없앰(em태그로 기우러진 text를 바로 세울 때 사용)
    - italic, oblique: text를 기울게 함

