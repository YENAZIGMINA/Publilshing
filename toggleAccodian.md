
![image](https://github.com/YENAZIGMINA/Publilshing/assets/129706758/a25cc329-71e1-492a-aa73-4345ac40eea5)




◼클릭(토글)하면 나와야하는 pannel 영역 (* max-height: 0; overflow: hidden;)

![image](https://github.com/YENAZIGMINA/Publilshing/assets/129706758/bbfd0d6e-916a-42f2-a28c-e82776bb1e6c)

◼active 붙으면 아이콘 변경 (accordions)

![image](https://github.com/YENAZIGMINA/Publilshing/assets/129706758/de8e3f57-d5f5-4516-96cb-75999cc4e297)




    let accordions = document.getElementsByClassName('detail_btn');

        function toggleAccordion() {
            let panel = this.nextElementSibling;
            this.classList.toggle('active'); //active 붙으면 아이콘 변경

            if (panel.style.maxHeight) {
                panel.style.maxHeight = null;
            } else {
                panel.style.maxHeight = panel.scrollHeight + "px"; //원래가지고 있는 높이값
            }
        }

        for (let i = 0; i < accordions.length; i++) {
            let accordion = accordions[i];
            accordion.addEventListener('click', toggleAccordion);
        }




---------------------------------------------------------------------


        <ul>
            <li class="accodion_list">
                <div class="acco_tit" tabindex="0">title01</div>
                <p class="acco_desc">desc01</p>
            </li>
            <li class="accodion_list">
                <div class="acco_tit" tabindex="0">title02</div>
                <p class="acco_desc">desc02</p>
            </li>
        </ul>




        * {margin: 0; padding: 0;}
        .accodion_list {width: 100%; cursor: pointer; border-bottom: 1px solid #eee;}
        .acco_tit {background-color: pink; padding: 20px; font-size: 20px;}
        .acco_desc {height: 0; overflow: hidden; background-color: #fff;}
        .accodion_list.active .acco_desc {padding: 20px; height: auto;}




       <script>

            let accodionList = document.querySelectorAll('.accodion_list');

            for(let i = 0; i < accodionList.length; i++){
              accodionList[i].addEventListener("click", () => {
              accodionList[i].classList.toggle("active");
             });

            accodionList[i].addEventListener("keyup", (e) => {
                if(e.keyCode === 13) {
                  accodionList[i].classList.toggle("active");
                }
              })
            }

         </script>

