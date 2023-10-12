![image](https://github.com/YENAZIGMINA/Publilshing/assets/129706758/0148f2e1-0332-440f-bac4-1876ec01ef82)

    function openButton(button,element) {
            let tabcontnet;
            tabcontnet = document.getElementsByClassName('tabcontent')

            for (let i = 0; i < tabcontnet.length; i++) {
                tabcontnet[i].style.display = "none";
            }

            let tablinks = document.getElementsByClassName('tablinks');
            for(let i=0; i<tablinks.length; i++){
                tablinks[i].style.backgroundColor="";
                tablinks[i].style.color = "";
                //빈 문자열 할당시 bgc 속성은 기본값으로 초기화
            }

            element.style.backgroundColor="rgb(82, 82, 82)";
            element.style.color="rgb(255, 255, 255)";
            document.getElementById(button).style.display = "block";
            
        }

        document.getElementById('defaultOpen').click();



