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


# 스크롤 원하는 위치에 놓기 (js)
      
      
      <nav class="gnb">
        <ul class="gnb-list">
            <li class="gnb-item"><a href="#sectionOne">Section01</a></li>
            <li class="gnb-item"><a href="#sectionTwo">Section02</a></li>
            <li class="gnb-item"><a href="#sectionThree">Section03</a></li>
        </ul>
       </nav>


       <div>
           <section id="sectionOne" class="section">Section01</section>
           <section id="sectionTwo" class="section">Section02</section>
           <section id="sectionThree" class="section">Section03</section>
       </div>


       ----------------------------------------------------------

      *{margin: 0; padding: 0;}
        nav.gnb {position: fixed; top: 0; left: 0; right: 0; background-color: rgb(32, 32, 32);}
        ul.gnb-list {display: flex; justify-content: space-between;}
        ul.gnb-list li {border-right: 1px solid #ccc; width: 33.33%; text-align: center;}
        ul.gnb-list li a {text-decoration: none; color: #fff; padding: 15px; width: 100%; display: inline-block;}

        section {height: 60vh; color: #252525; font-size: 35px; display: flex; justify-content: center; align-items: center;}
        section:nth-child(1) {background: coral;}
        section:nth-child(2) {background: cornflowerblue;}
        section:nth-child(3) {background: rgb(255, 151, 172);}

        ------------------------------------------------------------


        <script>

        let gnbItem = document.querySelector('.gnb-item');
        let sections = document.querySelector('section')

        gnbItem.forEach((gnbItem, index) => {
            gnbItem.addEventListner("click", (e) => {
                e.preventDefault();

                let sectionTop = sections[index].offsetTop - 500;

                window.scroll({top:sectionTop});
            })
        })

       </script>
       

      






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


# 스크롤 부드럽게

      window.scroll({
         top:0,
         left:100,
         behavior:'smooth'
      });



      function makeLinksSmooth() { 
        const navLinks = document.querySelectorAll("nav a"); 

        navLinks.forEach((link) => {
        link.addEventListener("click", smoothScroll);
           });
      }


