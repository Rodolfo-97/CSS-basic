## Position

- 요소들의 위치를 이동할 때 사용.
  
- **positon type**에 따른 **기준점**이 핵심이다.

### position의 5가지 type

#### static

- **요소들의 위치 기본값**(자연스럽게 있어야 할 위치)이다.

#### relative 

- **자기자신이 원래 있던 자리**를 기준으로 이동한다.
  
    - 요소가 float되지만 원래 자리를 기억하고 있기 때문에 다른 형제요소들의 위치가 변하지 않는다.

#### absolute

- absolute position인 요소의 부모 요소들 중 **static position이 아닌 부모 요소**를 기준으로 삼는다.
   
- float 속성을 사용했을 때와 비슷하게 absolute position인 요소들의 display가 길막을 하지 못하는 block 요소가 되고 부모 요소와 형제 요소가 absolute position인 요소를 무시한 채로 배치된다.
  
    - 즉 요소들이 겹치게 됨.
  
    - 다른 inline 요소들도 absolute position인 요소를 무시한채 위치한다는 점에서 float 속성을 사용했을 때와 차이가 있다. 
        - float속성을 사용했을때는 inline 요소들이 해당 float된 요소를 찾아낼 수 있었다.

#### fixed

- absolute position과 결과는 똑같고 기준점이 **viewport size(디바이스의 화면)**으로 고정되었다는 점이 유일한 차이이다.

    - 스크롤을 내려도 fixed position인 요소는 화면의 원래 있던 자리에 고정되어있다.

#### sticky


## z-index

- position 되어 수직방향으로 떠 있는 요소들의 z축의 위치 즉 떠있는 높이라고 생각하면 된다.

- position 을 정해주면 요소들은 z축으로 float되는데 이때 떠 있는 요소들의 z축 높이를 지정해주어 요소들이 겹치는 것을 조절할 수 있다.