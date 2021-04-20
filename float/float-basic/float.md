## float 속성

- **block요소들을 가로배치 하기위해 사용한다.** 

### 특징

- float속성의 핵심은 요소들을 **부유(float)**시키는 것이다.

- 부모요소와 형제요소는 float된 자식요소를 무시한다.

    - 부모요소의 height값이 없어진 자식요소의 height값만큼 줄어든다.
  
    - float된 요소의 자리에 다른 형제요소들이 이동한다. (떠 있는 요소 밑에 형제요소가 깔려있음).

- float된 요소들은 block요소(하자있는? block 요소)로 바뀐다.
  
    - block요소에서만 쓸 수 있는 속성을 사용 할 수 있다.
  
    - float된 요소가 block요소라 하더라도 width의 값을 정하지 않은 경우 일반 block요소와 다르게 컨텐츠만큼의 width 값을 가지기 때문에 옆에 다른 요소들이 올 수 있다. 
    
    - width의 값을 정해준 경우에도 margin이 자동으로 생성되지 않기 때문에 옆에 다른 요소가 올 수 있다.  

- float된 요소들은 width의 값을 정한다 하더라도 margin이 자동으로 만들어지진 않는다.(일반 block요소들과의 차이)

- inline 요소들은 float된 요소들을 무시하지 않는다.

**float요소를 사용하면 다른 block요소들이 float된 요소들을 무시하기 때문에 요소들이 겹쳐서 안보이는 등 레이아웃이
박살나는 큰 단점이 있다.**


<br>

## float로 박살난 레이아웃을 보수하는 방법

### 방법 1

- 부모 요소에 **overflow: hidden;** 속성을 사용해주면 된다.

```css
.parent {
    overflow: hidden;
}
```
- 부모요소가 float된 자식 요소를 바로 찾아서 레이아웃을 맞춘다.

### 방법 2 - clearfix

- **clear 요소**를 이용한다.

    - left, right, both값이 있다.
     
    - clear: 방향; 속성을 쓴 요소들은 그 방향의 float된 요소들을 고려하기 때문에 레이아웃이 겹치지 않는다.
  
        - 부모 요소는 clear속성을 쓴 요소를 통해 없어진 float요소들을 알 수 있기 때문에 레이아웃이 똑바로 잡힘.

#### 예시코드

- **가상 요소**를 이용해 float로 박살난 레이아웃 잡기.
    - 레이아웃을 고치기 위해 html에 불필요한 요소를 넣지 않기 위해 가상요소를 이용한 것.
  
```css
.parent::after {
    /* parent요소의 마지막 자식요소인 가상요소를 선택한 것 */
    content: "";
    /* 무조건 적어줘야함. */
    display: block;
    /* clear 속성을 사용하려면 반드시 block요소여야 한다. */
    clear: left;
    /* 이 가상요소는 float: left;된 요소를 고려한다. 
    이 가상요소를 통해 부모요소가 레이아웃을 잡을 수 있음.*/
}

.child1 {
    float: left;        
}

.child2 {
    float: left;
}
```

