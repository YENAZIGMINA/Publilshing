# offset : 선택한 요소의 좌표를 가져오거나 특정 좌표로 이동

   
    ■ var abc = $( 'h1' ).offset();
    
    ---> h1 요소의 좌표를 변수 abc에 저장

    ■ $( 'h1' ).offset( { left: 100, top: 50 } );

    ---> h1 요소를 왼쪽 100ox, 위 50px 만큼 위치이동


# scrollTop : 요소의 수직 스크롤 바 위치

element.scrollTop;

element.scrollTop = 200; 



------------------------------------------------------------------------------------------------------


# 스크롤 원하는 위치에 놓기 (여러개)

![image](https://github.com/YENAZIGMINA/Publilshing/assets/129706758/42788a1d-2c08-466e-8535-0570cd6bcff9)

![image](https://github.com/YENAZIGMINA/Publilshing/assets/129706758/c9f547cb-6dd1-4908-a78a-e489f00be5e4)

![image](https://github.com/YENAZIGMINA/Publilshing/assets/129706758/d36778f8-4b13-4418-b914-a82aab981561)


# 스크롤 원하는 위치에 놓기 (개별)

      $('.abc').animate( { scrollTop : $(selector).offset().top }, 500 );

      ---> abc의 스크롤이 selector요소의 위치로 500ms 동안 이동






# 최대수평 스크롤값

![image](https://github.com/YENAZIGMINA/Publilshing/assets/129706758/3e5027e5-3bba-4c4a-b39d-01e754b1e541)

const maxScrollLeft = el.scrollWidth - el.clientWidth;

# 최대수직 스크롤값
![image](https://github.com/YENAZIGMINA/Publilshing/assets/129706758/406a48a1-cf83-48c9-95d8-8dffbf6076c5)

const maxScrollHeight = el.scrollHeight - el.clientHeight;




------------------------------------------------------------------------------------------------------



# 윈도우 스크롤 맨위로 이동

      제이쿼리
      $(window).scrollTop(0);

      애니메이션 주면서 이동
      $('html, body').animate({scrollTop:0},1000);

      자바스크립트
      window.scrollTop(0,300);


# 애니메이션

줄임표현 속성들을 완벽히 지원하지 않는다. (border x -> border-width o)

$(selector).animate({style}, speed, easing, callback)



