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

2.5
grid-column : x / y로 grid-column-start와 grid-column-end를 축약할 수 있다.
-1은 끝을 뜻함
-2는 끝의 전을 뜻하며, -n은 끝의 n - 1 전을 뜻함
span n은 n칸을 차지함을 의미함
span n / y 등으로 시작점 등을 표시해줄 수 있다.

2.6
라인 이름 붙이기
grid-template-columns등에서 px값 앞에 [이름]을 붙이는 것으로 라인의 이름을 정할 수 있다.
repeat에서도 2번째 parameter 값 뒤에 [이름]을 붙이는 것으로 라인들의 이름을 정해줄 수 있다.
note: 뒤에 붙이면 끝부터 이름이 붙어서 repeat 시작 line은 이름이 없다! 앞에 붙여야 시작 line부터 이름이 다 붙음

※flex는 1차원, grid는 2차원

2.7
fr은 fraction, fraction은 사용 가능한 공간을 뜻함
공간을 가질 수 있을 만큼 가진다.
navigatior가 아닌 grid container에서 fr을 얻는게 굉장히 중요하다고 한다.
상대좌표의 느낌(px보다 훨씬 유연하다)
row와 colum을 동시에 fr을 하면 왜 사라질까?
수직 방향은 height를 지정해주어야한다.
vh는 내 화면의 n% 정도를 의미한다.
즉 vh도 상대좌표이다!!
grid-template로 많은 것들을 통합할 수 있다.
grid-template에서 repeat은 작동하지 않는다.

2.8
justify-items는 default값이 stretch이며 콘테이너가 모든 grid자식을 가지고 그것들을 늘여 콘테이너 자신을 채움을 뜻함(가로축)
start는 grid의 처음부터 채움. center는 중앙부터 채움. 나머지는 응용
align-items는 세로축 담당
child의 크기가 지정된 상태에서는 stretch가 적용되지 않는다.
place-items: y x로 justify-items와 align-items를 함께 할 수 있다.
첫번째가 수직방향임에 주의

2.9
place-items는 개별 아이템에 적용
place-content는 전체 grid(틀)에 적용
justify-content, align-content, place-content가 모두 존재함

2.10
align-self와 justify-self가 존재! child에게 개별 적용되는 것을 제외하면 똑같다.
.item*20>{$}
.은 div class name을 뜻함 여기서 name은 item
*20은 20개 생성
>{$}는 숫자를 표시해줌을 뜻함
만약 그리드 내에서 지정해준 cell보다 데이터의 cell이 많을 수도 있다.
그럴 때는 grid-auto-rows, grid-auto-columns이 해결책이 될 수 있다.
grid-auto-flow는 특수한 케이스로, item들이 추가되었을 때 어떤 방향으로 grid가 확장될지를 결정한다.
적용방식이 flexbox-direction과 유사하다.

2.11
minmax의 사용 이유: 어떤 element가 가능한한 엄청 크길 바라면서, 어느 정도 이하로 작아지는 것을 바라지는 않을 때
minmax(min,max)로 사용할 수 있다.
min 이하로 작아지지 않고, max 이상으로 커지지 않는다.

2.12 auto-fit과 auto-fill을 이용해 쉽게 반응형 디자인을 할 수 있고 이는 repeat에서 사용된다.
auto-fill은 column이 비어있더라도 column들이 들어갈 수 있는 자리에 최대한 많은 공간을 제공한다(빈 column 발생)
auto-fit은 element들을 stretch하여 공간에 딱 맞게 해준다.
모두 화면이 작을 때는 같이 동작하나, 화면이 늘어날 때 달리 작동한다.