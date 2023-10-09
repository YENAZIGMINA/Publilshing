<h2>중앙정렬</h2>


✔️자기자신이 중앙정렬
position, flex, grid, place-items (grid 일 때 사용), margin

✔️수평 중앙정렬
- 블록요소 : 자기자신에게 margin:auto;
- 인라인 (+ 인라인블록) : 부모요소 or 상위요소에 text-align:center;
- float로 배치하는 것은 블록,인라인, 인라인블록 모두 해당

✔️자기자신과 인접해있는 요소와 수직 중앙을 맞출경우
- vertical-align: 값;
- transform : translateY(값);

--------------------------------------------------------------------------------
✔️flex
flex-wrap 은 한 줄로 구성할지, 여러줄로 구성할지 설정
flex-wrap(줄바꿈) : nowrap / wrap (부모 폭을 기준으로 줄바꿈) / wrap-reverse (부모 폭 기준으로 줄바꿈되지만, 순서가 아래 왼쪽부터 정렬)

align-content : stretch (item의 높이값이 교차축을 중심으로 균등하게 늘어나고)
              : flex-start (부모 컨테이너의 상단기준으로) / flex-end는 하단 기준으로 / center는 부모요소 컨테이너의 중앙기준으로 정렬
              : space-between (아이템 교차축 방향으로 첫줄과 마지막줄은 양끝으로 정렬되고 ~)

align-self : 컨텐트와 동일한 값이 있지만 각각 개별로 정렬


flex-grow : 증가너비 비율을 설정 / 부모 너비보다 커지면 각 아이템은 flex-grow 비율에 맞게 늘어남 (기본값 0)
flex-shrink : 감소너비 비율 설정 (스크롤 생기지 않음) (기본값 1)
flex-basis : 아이템 기본너비값 지정 (기본값 auto) (px, em, %값으로 설정)

--------------------------------------------------------------------------------
[ place-items 설명 ]
display:grid; 일 때 사용
https://www.w3schools.com/cssref//playdemo.php?filename=playcss_place-items
