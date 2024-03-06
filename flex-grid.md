# flex-basis

    <div class="wrap">
      <div class="item">가가가</div>
      <div class="item">나나나</div>
      <div class="item">다다다</div>
      <div class="item">라라라</div>
      <div class="item">마마마</div>
    </div>

    .wrap {display: flex; width: 60%; background-color: aliceblue;}
    .item {border: 1px solid #000; text-align: center; line-height: 100px; width: 100px; height: 100px; 
          margin-right: 20px; background-color: antiquewhite; }
    .item:nth-child(1) {flex-basis: 200px;}
    .item:nth-child(2) {flex-basis: auto;}
    .item:nth-child(3) {flex-basis: 30vw;}
    .item:nth-child(4) {flex-basis: 50%;}
    .item:nth-child(5) {flex-basis: 5rem;}

    
-------------------------------------------------------


# flex-grow

    <div class="wrap02">
      <div class="item02">가가가</div>
      <div class="item02">나나나</div>
      <div class="item02">다다다</div>
      <div class="item02">라라라</div>
      <div class="item02">마마마</div>
    </div>


    .wrap02 {display: flex; background-color: rgb(247, 250, 236);}
    .item02 {border: 1px solid #000; text-align: center; line-height: 100px; width: 100px; height: 100px;
            margin-right: 20px; background-color: rgb(189, 218, 219); flex-grow: 1;}
    .item02:nth-child(1) {flex-grow: 3;}
    .item02:nth-child(2) {flex-grow: 0;}
    .item02:nth-child(3) {flex-grow: 4;}
    .item02:nth-child(4) {flex-grow: 0;}
    .item02:nth-child(5) {}

    
-----------------------------------------------------------


# flex-shrink

    <div class="wrap03">
      <div class="item03">가가가</div>
      <div class="item03">나나나</div>
      <div class="item03">다다다</div>
      <div class="item03">라라라</div>
      <div class="item03">마마마</div>
    </div>
  </div>


     .wrap03 {display: flex; background-color: rgb(250, 238, 236);}
    .item03 {border: 1px solid #000; text-align: center; line-height: 100px; width: 100px; height: 100px;
             margin-right: 20px; background-color: rgb(255, 223, 236);}
    .item03:nth-child(1) {flex-basis: 300px; flex-shrink: 0;}
    .item03:nth-child(2) {flex-shrink: 2;}
    .item03:nth-child(3) {}
    .item03:nth-child(4) {}
    .item03:nth-child(5) {flex-shrink: 3; min-width: 0; min-height: 0; overflow: hidden;} /* 최소한으로 줄어들도록 */



-----------------------------------------------------------

# grid-template-columns, grid-template-rows, grid-auto-rows, grid-gap (부모)

# grid-column, grid-row (자식)

    <div class="container">
      <div class="box color1">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eos minus nemo aliquid consequuntur nulla sequi sapiente alias, animi magni ea quod aut dignissimos repellat earum consectetur est nostrum aspernatur obcaecati. Lorem ipsum, dolor sit amet consectetur adipisicing elit. Eaque eum eveniet tempore, laboriosam ad corrupti enim rem, odit maiores iure cumque labore error quaerat accusantium libero hic repellendus minima numquam.</div>
      <div class="box color2">Item1</div>
      <div class="box color2">Item2</div>
      <div class="box color3">Item3</div>
      <div class="box color4">Item4</div>
      <div class="box color5">Item5</div>
      <div class="box color1">Item6</div>
      <div class="box color2">Item7</div>
      <div class="box color3">Item8</div>
      <div class="box color4">Item9</div>
      <div class="box color5">Item10</div>
      <div class="box color5">Item11</div>
    </div>


     .container {display: grid; grid-template-columns: repeat(5,1fr); grid-template-rows: 220px 220px 220px; /* grid-auto-rows: minmax(200,auto); */ grid-gap: 10px;}
    .box {text-align: center;}
    .box:nth-child(1) {background-color: #f5f5f5;}
    .box:nth-child(2) {background-color: #e7e7e7;}
    .box:nth-child(3) {background-color: #dadada; grid-column: 3/5; grid-row: 1/3;}
    .box:nth-child(4) {background-color: #cccccc;}
    .box:nth-child(5) {background-color: #bebebe;}
    .box:nth-child(6) {background-color: #afafaf;}
    .box:nth-child(7) {background-color: #a5a5a5;}
    .box:nth-child(8) {background-color: #999999;}
    .box:nth-child(9) {background-color: #8d8d8d;}
    .box:nth-child(10) {background-color: #7e7e7e;}
    .box:nth-child(11) {background-color: #6b6b6b;}
    .box:nth-child(12) {background-color: #555555;}


-----------------------------------------------------------


    <section class="img-wrap">
      <img src="" alt="img" class="image image1">
      <img src="" alt="img" class="image image2">
      <img src="" alt="img" class="image image3">
      <img src="" alt="img" class="image image4">
      <img src="" alt="img" class="image image5">
      <img src="" alt="img" class="image image6">
      <img src="" alt="img" class="image image7">
    </section>


    .img-wrap {display: grid; grid-template-columns: repeat(3,1fr); grid-auto-rows: 300px; gap: 40px;
               grid-template-areas: 'a a a'
                                    'b c c'
                                    'b d g'
                                    'e f g';}
    img {width: 100%; height: 100%; object-fit: cover;}
    .image1 {grid-area: a;}
    .image2 {grid-area: b;}
    .image3 {grid-area: c;}
    .image4 {grid-area: d;}
    .image5 {grid-area: e;}
    .image6 {grid-area: f;}
    .image7 {grid-area: g;}
