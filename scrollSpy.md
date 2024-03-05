    <nav class="gnb">
        <ul class="gnb-list">
            <li class="gnb-item active"><a href="#sectionOne">Section01</a></li>
            <li class="gnb-item"><a href="#sectionTwo">Section02</a></li>
            <li class="gnb-item"><a href="#sectionThree">Section03</a></li>
        </ul>
    </nav>


    <div>
        <section id="sectionOne" class="section">Section01</section>
        <section id="sectionTwo" class="section">Section02</section>
        <section id="sectionThree" class="section">Section03</section>
    </div>


    ---------------------------------------------


        *{margin: 0; padding: 0;}
        nav.gnb {position: fixed; top: 0; left: 0; right: 0; background-color: rgb(32, 32, 32);}
        ul.gnb-list {display: flex; justify-content: space-between;}
        ul.gnb-list li.gnb-item {list-style: none; border-right: 1px solid #ccc; width: 33.33%; text-align: center;}
        ul.gnb-list li.gnb-item.active {background-color: pink;}
        ul.gnb-list li.gnb-item a {text-decoration: none; color: #fff; padding: 15px; width: 100%; display: inline-block;}
        ul.gnb-list li.gnb-item.active a {color: #252525; font-weight: bold;}

        section {width: 100%; height: 100vh; color: #252525; font-size: 35px; display: flex; justify-content: center; align-items: center;}
        section:nth-child(1) {background: coral; margin-top: 40px;}
        section:nth-child(2) {background: cornflowerblue;}
        section:nth-child(3) {background: rgb(255, 151, 172);}


      ---------------------------------------------


      window.addEventListener("scroll", () => {
        const sections = document.querySelectorAll("section");
        const gnbItems = document.querySelectorAll(".gnb-item");

        sections.forEach((section, index) => {
          const top = window.scrollY; //현재 Y값
          const sectionTop = section.offsetTop - 40; // 섹션 상단의 Y값 - Gnb메뉴 높이 값
          const sectionHeight = section.offsetHeight; // 섹션 높이

          gnbItems.forEach((gnbItem) => {
          // 5. 스크롤 위치가 섹션 상단 스크롤 위치보다 크고 && 섹션높이값보다 작을 경우
          if (top >= sectionTop && top < sectionTop + sectionHeight) {
            gnbItem.classList.remove("active");
            gnbItems[index].classList.add("active");
          }
        });
      });
    });

      
