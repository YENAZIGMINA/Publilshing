    <head>
      <!-- 제이쿼리 불러오기 -->
      <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
      <!-- slick 불러오기 -->
      <script src="https://cdnjs.cloudflare.com/ajax/libs/slick-carousel/1.9.0/slick.min.js"></script>
      <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/slick-carousel/1.9.0/slick-theme.min.css">
      <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/slick-carousel/1.9.0/slick.min.css">
    </head>




    <div class="outer">
        <div class="buttons">
            <button class="active">1</button>
            <button>2</button>
            <button>3</button>
        </div>
        <div class="tabs">
            <div class="tab active">
                <div class="slider">
                    <div class="item" style="background-color:red;"></div>
                    <div class="item" style="background-color:blue;"></div>
                    <div class="item" style="background-color:green;"></div>
                    <div class="item" style="background-color:gold;"></div>
                    <div class="item" style="background-color:black;"></div>
                </div>
            </div>
            <div class="tab">
                <div class="slider">
                    <div class="item" style="background-color:skyblue;"></div>
                    <div class="item" style="background-color:pink;"></div>
                    <div class="item" style="background-color:darkblue;"></div>
                    <div class="item" style="background-color:darkred;"></div>
                    <div class="item" style="background-color:darkgray;"></div>
                </div>
            </div>
            <div class="tab">
                <div class="slider">
                    <div class="item" style="background-color:darkgreen;"></div>
                    <div class="item" style="background-color:purple;"></div>
                    <div class="item" style="background-color:orange;"></div>
                    <div class="item" style="background-color:red;"></div>
                    <div class="item" style="background-color:blue;"></div>
                </div>
            </div>
        </div>
    </div>





    <style>
        * {margin: 0; padding: 0;}
        .tabs {padding-top:50px;}
        .tab {display:none;}
        .tab.active {display:block;}
        button {width:50px;height:50px;font-size:16px;display:inline-block;color:darkgreen;}
        button.active {background-color:rgba(0,0,0,.5);}
        .slider {width:500px;height:300px;}
        .item {height:300px;}
    </style>




    <script>
        $('button').click(function(){
            var $this = $(this);
            var index = $this.index();

            $this.addClass('active');
            $this.siblings('button.active').removeClass('active');

            var $outer = $this.closest('.outer');
            var $current = $outer.find(' > .tabs > .tab.active');
            var $post = $outer.find(' > .tabs > .tab').eq(index);

            $current.removeClass('active');
            $post.addClass('active');
            // 위의 코드는 탭메뉴 코드입니다.

            $('.slider').slick('setPosition');
            // 탭 페이지 안에서 slick 사용시 – slick이 첫페이지에 있지 않으면 slick의 첫번째 이미지가 보이지 않고 2번째 부터 도는것을 확인할 수 있다. 해당 문제는 탭이 active가 된 후 그 페이지에 slick이 있다면 = slick의 위치를 수동으로 새로 고쳐줘야 한다.
        });

        // 기존 처음의 slick 적용
        $('.slider').slick({
            slidesToShow: 2,
            dots: true,
        });
    </script>
    
