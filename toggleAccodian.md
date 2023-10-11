
![image](https://github.com/YENAZIGMINA/Publilshing/assets/129706758/a25cc329-71e1-492a-aa73-4345ac40eea5)


![image](https://github.com/YENAZIGMINA/Publilshing/assets/129706758/bbfd0d6e-916a-42f2-a28c-e82776bb1e6c)
◼클릭(토글)하면 나와야하는 pannel 영역 (* max-height: 0; overflow: hidden;)

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
