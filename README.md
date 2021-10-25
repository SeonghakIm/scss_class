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

2.2 
grid도 flex와 같이 father가 관리한다.
grid-template-columns는 일단 절대좌표(px)로 grid 내부의 공간(세로축)의 크기를 조절한다.
grid-template-rows는 일단 절대좌표(px)로 grid 내부의 공간(세로축)의 크기를 조절한다.
grid block 사이의 간격은 column-gap, row-gap으로 나누어 지정하거나 아니면 둘 모두를 gap으로 조절할 수 있다.
※ 앞으로 추가될 모든 block들의 크기를 지정하고 싶을 때는 어떻게 할까?

2.3
repeat을 사용하면 반복해서 절대좌표를 적어줄 필요가 없다.
grid-template-areas로 element들이 template의 어느 장소에 위치할지 지정할 수 있다.
grid-template-areas로 element의 이름을 인식하게 하려면 element마다 grid-area를 지정해주어야 한다.
class name은 아무것도 하지 않음!
.으로 template-area의 공간을 비워둘 수 있다.
auto는 가능한 만큼 큰 공간을 가져가고 그 다음 절대 좌표가 온다.

2.4
grid-column-start와 grid-column-end에 들어가는 숫자는 line을 뜻함
gap을 주어 line의 위치를 확인할 수 있음
grid-column-start와 grid-row-start를 조절함으로써 html의 변경없이 element의 위치를 조절할 수 있다.
element를 늘임으로써 2.3과 비슷한 레이아웃을 만들 수 있다.