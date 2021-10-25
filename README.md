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

1.6
flex-grow, flex-shrink는 child에게 줄 수 있는 property
flex-wrap이 nowrap일 때 width를 무시하고 box가 찌그러지는데, 어느 박스가 찌그러질지 이제 명령할 수 있다.
flex-shrink의 기본 값은 1
flex-shrink의 값이 n이 되면 다른 box들보다 n배 더 많이 찌그러진다.
flex-grow의 기본 값은 1
flex-grow는 n만큼의 지분으로 여분의 main axis의 공간을 가져옴!
경쟁자가 있을 경우 각자 n/sum의 지분으로 여분 공간을 가져감
반응형 디자인을 할 때 유용함

1.7
flex-basis는 width와 유사(default가 low인 main axis에서 작용하기 때문!)
element의 처음 값을 줌
찌그러지거나 늘어나기 전에는 element의 값이 flex-basis의 값을 유지함