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


----------------------------------------------------------------------

*탭 클릭시 클래스명 active 추가(텍스트 색상변경위해)
        function openMap(button, element) {
        let tabcontent = document.getElementsByClassName('mapImg');
    
        for (let i = 0; i < tabcontent.length; i++) {
            tabcontent[i].style.display = "none";
        }
    
        let tablinks = document.getElementsByClassName('tablinks');
        for (let i = 0; i < tablinks.length; i++) {
            tablinks[i].classList.remove('active');
        }
    
        document.getElementById(button).style.display = "block";
        element.classList.add('active');
    }
    
    document.getElementById('defaultOpen').click();


----------------------------------------------------------------------




        <div class="tap-box">
                <ul class="taps depth5">
                    <li><a href="#mainTabBtn" class="active mainTabBtn" title="선택됨"><span>지하 1층</span></a>
                    </li>
        
                    <li><a href="#mainTabBtn" class="mainTabBtn"><span>본관 1층</span></a>
                    </li>
        
                    <li>
                        <a href="#mainTabBtn" class="mainTabBtn"><span>본관 2층</span></a>
                    </li>
        
                    <li>
                        <a href="#mainTabBtn" class="mainTabBtn"><span>본관 3층</span></a>
                    </li>
                </ul>
            </div>



            <div class="tab_content" id="mainTab4" style="display: none;">
                <div class="img-preview txt-box mg20t tc">
                    <a class="preview-btn" href="http://210.206.69.186/Jangsu/Potal/images/content/02/map-3f.png" target="_blank" title="새창으로열림">
                        <span>+원본보기</span></a>
                    <img src="http://210.206.69.186/Jangsu/Potal/images/content/02/map-3f.png" alt="">
                </div>
            </div>




            <script>
            //<![CDATA[
            $(document).ready(function(){
                $(".mainTabBtn").bind("click",function(){
                        var curLength = $(this).parent().index();
                        $(".tab_content").css("display","none");
                        $("#TabUl > li").removeClass("active");
                        $("#mainTab"+(curLength+1)).css("display","block");
                        $(this).parent().addClass("active");
                });
            });
            //]]>
            </script>



----------------------------------------------------------------------------

# 탭메뉴 부드럽게 나타나기

        <!--탭메뉴-->
        <ul class="commonTab">
            <li class="t1">
                <a href="#listtype1"> 탭1</a>
            </li>
            <li class="t2">
                <a href="#listtype2">탭2</a>
            </li>
            <li class="t3">
                <a href="#listtype3">탭3</a>
            </li>
        </ul>
        <!--//탭메뉴-->

        <!--내용-->
        <div class="prolist" id="listtype1">
            탭1 내용
        </div>
        <div class="prolist" id="listtype2">
            탭2 내용
        </div>
        <div class="prolist" id="listtype3">
            탭3 내용
        </div>
        <!--//내용-->



        $('.prolist').hide();
        $('.commonTab a').bind('click', function(e){
            $('.commonTab a.on').removeClass('on');
            $('.prolist:visible').hide();
            $(this.hash).fadeIn(300);
            $(this).addClass('on')
            e.preventDefault();
        })
        .filter(':eq(1)').click();
            
