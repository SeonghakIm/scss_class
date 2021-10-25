# scss_class

1.2
justify-content는 main axis 방향으로 아이템을 옮김
align-item은 cross axis 방향으로 아이템을 옮김
flex-direction이 row면 main axis는 horizonal
align-item을 할 때는 wrapper의 높이를 잘 고려해야함

1.4
align self는 child에 포함되는 몇 안되는(강의에서는 오직 둘뿐) property 중 하나!
order 역시 child에 포함되는 property이다
order의 default값은 0, 뒤로 갈 수록 order가 밀린다.

1.5
flexbox는 width를 신경쓰지 않고 child들을 같은 줄에 있도록 만드는 것에 신경쓴다
flex-wrap의 기본 값은 nowrap
wrap일 경우 flexbox에게 child의 크기를 유지하라고 함
box사이 공간(cross axis에 있는 line)은 align-content로 조절할 수 있다.