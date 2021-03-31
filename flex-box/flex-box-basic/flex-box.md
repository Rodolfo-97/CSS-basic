## Flex-box

- 플렉스 박스는 플렉스 컨테이너(flex container=부모 요소)와 플렉스 요소(flex item=자식 요소)로 구성되고 레이아웃을 잡을 때 사용한다.

- 주 축과 교차축의 개념이 굉장히 중요하다.

### flex container 의 속성

#### display - Flex Container를 정의

```css
.container {
    display: flex;
    /* displat: inline-flex; */
}
```

- display 값으로 flex, inline-flex 가 있다.

    - flex는 컨테이너가 block 요소(수직 쌓임)이고 inline-flex는 inline-block 요소(수평쌓임)가 된다.

#### flex-direction

- flex item 들의 주 축(main-axis)을 설정한다.

```css
.container {
    flex-direction: row; /* 기본값 */
    /* flex-direction: column;
    flex-direction: row-reverse;
    flex-direction: column-reverse; */

}
```
- row는 주 축이 가로방향.
- column은 주 축이 세로방향.
- row-reverse는 주 축은 row와 동일하지만 흐름이 오른쪽에서 왼쪽으로 row의 반대로 흐른다.
- column-reverse는 주 축은 column과 동일하지만 흐름이 밑에서 위로 column의 반대로 흐른다.


#### flex - wrap

- flex-item들을 한줄 또는 여러줄에 묶을 때 쓰는 속성이다.

```css
.container {
    flex-wrap: nowrap; /* 기본값 */
    /* flex-wrap: wrap: */
}
```

- 모든 item들을 한 줄로 묶음(그 줄에 다 들어가도록 요소들의 width값이 줄어든다.)

- item들을 여러줄로 묶음.

#### justify-content

- 주 축을 기준으로 flex-item들을 정렬함.

```css

.container {
    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    /* justify-content: flex-end;
    justify-content: center;
    justify-content: space-between;
    justify-content: space-around;     */
}
```
- flex-start
    - Items를 시작점(flex-start)으로 정렬.
  
- flex-end:	
    - Items를 끝점(flex-end)으로 정렬.
  
- center: 
    - Items를 가운데 정렬.	
  
- space-between: 
    - 시작 Item은 시작점에, 마지막 Item은 끝점에 정렬되고 나머지 Items는 사이에 고르게 정렬됨.
  
- space-around:	
    - Items를 균등한 여백을 포함하여 정렬.


#### align-content

- 주 축에 수직인 교차축을 기준으로 item들을 정렬한다.

    - flex-wrap 속성을 통해 Items가 여러 줄(2줄 이상)이고 여백이 있을 경우만 사용할 수 있다.

```css
.container {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    align-content: stretch;
    /* align-content: center;
    align-content: flex-start;
    align-content: flex-end;
    align-content: space-between;
    align-content: space-around; */
}
```
- stretch
    - Container의 교차 축을 채우기 위해 Items를 늘림.(기본값)
  
- flex-start
    - Items를 시작점(flex-start)으로 정렬.	
  
- flex-end:	
    - Items를 끝점(flex-end)으로 정렬.	
  
- center:	
    - Items를 가운데 정렬.	
  
- space-between:	
    - 시작 Item은 시작점에, 마지막 Item은 끝점에 정렬되고 나머지 Items는 사이에 고르게 정렬됨.	
  
- space-around:	
    - Items를 균등한 여백을 포함하여 정렬.


#### align-items

- 교차 축(cross-axis)에서 Items의 정렬 방법을 설정.

- Items가 한 줄일 경우 많이 사용함.
    - items가 여러줄일 경우 주 축과 교차축도 item들의 줄 마다 생겨 item들이 따로 놀기 때문이다.

```css
.container {
    align-items: flex-start;
    /* align-items: stretch;
    align-items: flex-end;
    align-items: center;
    align-items: baseline; */
}
```

- stretch	
    - Container의 교차 축을 채우기 위해 Items를 늘림.(기본값)
  
- flex-start	
    - Items를 각 줄의 시작점(flex-start)으로 정렬.
  	
- flex-end	
    - Items를 각 줄의 끝점(flex-end)으로 정렬.

- center	
    - Items를 가운데 정렬.
  	
- baseline	
    - Items를 문자 기준선에 정렬.

### flex - item 의 속성

#### order

- html문서에 마크업한 순서대로가 아니라 자유롭게 Flex Item의 순서를 설정할 수 있다.

```css
.item1 {
    order: 1;
}

- 마크업이 첫 번째가 아니라도 웹에서 첫번 째 item으로 출력됨.
