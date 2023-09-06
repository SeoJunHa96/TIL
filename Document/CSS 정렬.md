- Flex레이아웃 만들기

  ```html
  <div class="container">
      <div class="item">helloflex</div>
  </div>
  ```

  

- display: flex;

  ```html
  .container{
  	display: flex;
  }
  ```

  (block을 자기 콘텐츠 영역만큼만 범위를 가지도록 변경)



- 배치 방향 설정

  ```html
  .container{
  	flex-direction: row;(column, row-reverse, column-reverse)
  }
  <!-- 왼쪽에서 오른쪽, 위에서 아래, 오른쪽 끝에서부터 왼쪽으로 쌓음, 아래(바닥)에서 위로 쌓음)
  ```

  

- 줄넘김 처리 flex-wrap

  ```html
  .container{
  	flex-wrap: warp;
  }
  ```

  줄바꿈. wrap-reverse하면 줄바뀜이 생길때 위로 올라감



- flex-flow

  ```html
  .container{
  	flex-flow: row wrap
  }
  <!-- direction, wrap의 순으로 한칸 띄고 쓰기 -->
  ```



- 정렬
  - justify : 메인축
  - align : 수직축



- 메인축 방향 정렬, justify-content

  ```html
  .container{
  		justify-content: flex-start;
  (flex-end, center, space-between, space-around, space-evenly)
  }
  <!-- 기본값, 오른쪽 끝으로 붙임, 가운데 정렬, 양쪽 정렬, 양쪽 정렬인데 끝 부분 여백 있음, 여백과 아이템 사이의 간격도 똑같음 -->
  ```

  

- 수직출 방향 정렬

  ```html
  .container{
  		align-item: stretch;
  (flex-start, flex-end, center, baseline)
  }
  <!-- 기본값(수직축 방향으로 끝까지), 시작점으로 정렬(작 세로 위치 만큼 영역 가짐), 바닥 정렬, 가운데 정렬, 밑줄 맡춤(베이스라인 기준 정렬) -->
  ```

  

- 여러 행 정렬 align-content

  flex-wrap: wrap; 이 설정된 상태에서, 아이템들의 행이 2줄 이상 되었을 때의 수직축 방향 정렬을 결정하는 속성.

  ```html
  .container{
  		flex-wrap: wrap;
  		align-content: stretch;
  (flex-start, flex-end, center, space-between, space-around, space-evenly)
  }
  <!-- 기본값, 위에 몰림, 아래 정렬, 가운데 정렬(행 기준), 양쪽 정렬, 양쪽정렬에 여백, 균일 간격-->
  ```

  

- 유연하게 늘리기 flex-grow

  여백 부분을 flex-golw에 지정된 숫자의 비율로 나누어진다.

  ```html
  .item{
  	flex-grow: 1;
  }
  <!-- 1:2:1 비율 세팅-->
  .item:nth-child(1) {flex-grow: 1; }
  .item:nth-child(2) {flex-grow: 2; }
  .item:nth-child(3) {flex-grow: 1; }
  ```



- 유연하게 줄이기 flex-shrink

  ```html
  .item{
  	flex-basis: 150px;
  	flex-shrink: 1;
  }
  ```

  ```html
  .container{
  		display: flex;
  }
  .item:nth-child(1){
  		flex-shrink: 0;
  		width: 100px;
  }
  .item:nth-child(2){
  		flex-grow: 1;
  }
  ```



-  수직축으로 아이템 정렬 align-self

  align-items가 전체 아이템의 수직축 방향 정렬, align-self는 해당 아이템의 수직축 방향 정렬

  ```html
  .item{
  		align-self: auto
  (stretch, flex-start, flex-end, center, baseline)
  }
  ```

  align-self는 align-items보다 우선권이 있다.

  개별적으로 값을 넣는것.



- 배치 순서 order

  시각적 나열 순서. HTML 자체의 구조를 바꾸는 것은 아니므로 접근성 측면에서 주의해야 한다.

  (스크린 리더로 화면을 읽을 때는 order로 순서를 바꾼 것이 의미가 없다.)

  ```html
  .item:nth-child(1){order: 3;}
  .item:nth-child(2){order: 1;}
  .item:nth-child(3){order: 2;}
  ```

  

- z - index

  z축 정렬 (숫자가 클수록 위로 올라감)

  ```html
  .item:nth-child(2) {
  		z-index : 1;
  		transform: scale(2);
  }
  <!-- z-index를 설정 안하면 0이다. -->
  ```

  