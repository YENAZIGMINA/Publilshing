# 오늘 날짜부터 특정일 까지 종료

      <script language="JavaScript">
      		//쿠키저장 함수
      		function setCookie( name, value, expiredays ) {
      			var todayDate = new Date();
      			todayDate.setDate( todayDate.getDate() + expiredays );
      			document.cookie = name + "=" + escape( value ) + "; path=/; expires=" + todayDate.toGMTString() + ";"
      		}
      
      		$(document).ready(function(){
      			$("#promotionBanner .btnClose").click(function(){
      				//오늘만 보기 체크박스의 체크 여부를 확인 해서 체크되어 있으면 쿠키를 생성한다.
      				if($("#chkday").is(':checked')){
      					setCookie( "topPop", "done" , 1 );
      					//alert("쿠키를 생성하였습니다.");
      				}
      				//팝업창을 위로 애니메이트 시킨다. 혹은 slideUp()
      				//$('#promotionBanner').animate({height: 0}, 500);
      				$('#promotionBanner').slideUp(500);
      			});
      		});
      
      	</script>
      
      	<div id="promotionBanner">
      		<div class="popContents">
      			<img src="/upload_data/popup/popup/170383405877008.jpg" alt="2024신년사">
      
      			<div class="popClose">
      				<input type="checkbox" value="checkbox" name="chkbox" id="chkday"/><label for="chkday">오늘 하루 그만보기 </label>
      				<a href="#none" class="btnClose">닫기</a>
      			</div>
      		</div>
      	</div>
      
      	<script language="Javascript">
          // 저장된 해당 쿠키가 있으면 창을 안 띄운다 없으면 뛰운다.
          cookiedata = document.cookie;
          
          // 24년 1월 7일 전 종료 (24년 1월 6일 23:59 까지 게시)
          var currentDate = new Date();
          var endDate = new Date('2024-01-07T00:00:00');
          
          if (cookiedata.indexOf("topPop=done") < 0 && currentDate < endDate) {
              document.getElementById('promotionBanner').style.display = "block";
          } else {
              document.getElementById('promotionBanner').style.display = "none";
          }
      </script>
      	 <!-- e: 레이어 팝업 임시 -->






# 시작일과 종료일 설정

      <style>
        #promotionBanner {position: absolute;z-index: 10;box-shadow: -1px 2px 9px 1px rgba(0, 0, 0, 0.2);overflow: hidden;border-radius: 15px;transform: translate(15px, 19px);}
        #promotionBanner .popContents {background-color: #000;width: 500px;}
        #promotionBanner .popContents img {width: 620px;}
        #promotionBanner .popContents .popClose {padding: 15px 20px;font-size: 17px;}
        #promotionBanner .popContents .popClose label {margin-left: 7px;color: #fff;}
        #promotionBanner .popContents .popClose a.btnClose {position: absolute;right: 20px;color: #fff;}
      </style>

     <script language="JavaScript">
        //쿠키저장 함수
        function setCookie(name, value, expiredays) {
            var todayDate = new Date();
            todayDate.setDate(todayDate.getDate() + expiredays);
            document.cookie = name + "=" + escape(value) + "; path=/; expires=" + todayDate.toGMTString() + ";"
        }

        $(document).ready(function () {
            $("#promotionBanner .btnClose").click(function () {
                //오늘만 보기 체크박스의 체크 여부를 확인 해서 체크되어 있으면 쿠키를 생성한다.
                if ($("#chkday").is(':checked')) {
                    setCookie("topPop", "done", 1);
                    //alert("쿠키를 생성하였습니다.");
                }
                //팝업창을 위로 애니메이트 시킨다. 혹은 slideUp()
                //$('#promotionBanner').animate({height: 0}, 500);
                $('#promotionBanner').slideUp(500);
            });
        });
    </script>

    <div id="promotionBanner">
        <div class="popContents">
            <img src="/upload_data/board_data/BBS_0000843/171037646716836.png" alt="교권침해 직통번호 1395">

            <div class="popClose">
                <input type="checkbox" value="checkbox" name="chkbox" id="chkday" /><label for="chkday">오늘 하루 그만보기
                </label>
                <a href="#none" class="btnClose">닫기</a>
            </div>
        </div>
    </div>

    <script language="Javascript">
        // 저장된 해당 쿠키가 있으면 창을 안 띄운다 없으면 뛰운다.
        cookiedata = document.cookie;

        // 24년 3월 15일 09:00 시작 ~ 25년 2월 28일 18:00 종료
        var startDate = new Date('2024-03-14T09:00:00');
        var currentDate = new Date();
        var endDate = new Date('2024-03-14T12:00:00');


        if (cookiedata.indexOf("topPop=done") < 0 && currentDate < endDate && currentDate >= startDate) {
            document.getElementById('promotionBanner').style.display = "block";
        } else {
            document.getElementById('promotionBanner').style.display = "none";
        }
    </script>
