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

            
