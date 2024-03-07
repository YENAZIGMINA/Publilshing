![image](https://github.com/YENAZIGMINA/Publilshing/assets/129706758/c5742108-4279-480b-ab68-bba32cc99364)


    
    <div class="subWrap">
        <div class="box">
            <button type="button" class="btn">open</button>
            <div class="menubox">menu</div>
        </div>
        <div class="modal2"></div> <!-- slide 오픈되었을 때 배경  -->
    </div>



    <style>
        * {margin: 0; padding: 0;}
        body.off {height:100%; /* overflow: hidden; 웹페이지 스크롤 생겨야해서 주석처리 */ position: relative;}
        .subWrap {height: 200vh;} /* 스크롤 내려가도 슬라이드 box가 보이도록 하기위해 높이 설정 한것, 실제 적용시에는 없어도 됨 */
        .box {/* position: relative; */ position: fixed;}
        .box .btn {position: fixed; top: 50px; left: 0;}
        .box .menubox {position: absolute; top: 0; left: -200px; width: 200px; height: 200px; background-color: aqua;}
        .modal2 {display: none; position: fixed; top:0; left: 0; width: 100%; height: 100%; background: rgba(0,0,0,0.5); z-index: -1;} 
    </style>



    <script>
        $(function(){
            var countAni = 1;
            $('.btn').click(function(){
                if(countAni == 1) { //메뉴 오픈시
                $('.menubox').animate({left:'0px'},300);
                $('.btn').text('close').animate({left:'200px'},300);
                $('.modal2').show();
                //$('body').addClass('off'); 웹페이지 스크롤 생겨야해서 주석처리
                $('body').on('scroll touchmove mousewheel', function(event){
                event.preventDefault();
                event.stopPropagation();
                return false;
            });
                countAni = 0;
            } else { //메뉴 닫을시
                $('.menubox').animate({left:'-300px'},300);
                $('.btn').text('open').animate({left:'0px'},300);
                $('.modal2').hide();
                $('body').removeClass('off');
                $('body').off('scroll touchmove mousewheel');
                countAni = 1;
                }
            });
        });
    </script>
