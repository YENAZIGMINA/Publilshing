![image](https://github.com/YENAZIGMINA/Publilshing/assets/129706758/76afb239-789e-4108-8f21-2c6f3316b5dd)


    ▪ 배경 어둡게 고정
     .pannel_inner3_wrapper {display: none; z-index: 1; position: fixed; left: 0; top: 0; width: 100%; height: 100%; background-color: rgba(0,0,0,0.5);}

 
    ▪ 컨텐츠 올리기
     .pannel_inner3_popup {color: #000; position: absolute; top: 50%; left: 50%; transform: translate(-50%,-50%); width: 600px; background-color: #fff; z-index: 2; text-align: center;}







    $('.pannel_inner3 .search_wrap').click(function (e) {
        e.preventDefault();
        $('.pannel_inner3_wrapper').fadeIn();
        });
        $('.pannel_inner3_popup .close').click(function (e) {
            e.preventDefault();
            $('.pannel_inner3_wrapper').fadeOut();
        });




        ---------------------------------------------------------------------


# 팝업 여러개 js 간략하게 작성

		<div class="infos">
			<a href="" class="tag share" data-popup="pop01">공유하기</a>
			<a href="" class="tag favor" data-popup="pop02">즐겨찾기</a>
			<a href="" class="tag decla" data-popup="pop03">신고하기</a>
		</div>

		<div class="info-pop pop01">
			<div class="overlay-bg">
				<div class="popWrap type01">
					<h4 class="cont-title tit">공유하기</h4>
					<div class="in-con">
						<a href="#n" class="link icon">
							<span>링크 복사</span>
						</a>
						<a href="#n" class="kakao icon">
							<span>카카오톡</span>
						</a>
						<a href="#n" class="facebook icon">
							<span>페이스북</span>
						</a>
						<a href="#n" class="naver icon">
							<span>네이버</span>
						</a>
					</div>
					<a href="#n" class="close-btn"><span class="blind">닫기</span></a>
				</div>
			</div>
		</div>
  

  		<script>
			$(document).ready(function() {
				function togglePopup(popupClass) {
					$('.' + popupClass).fadeIn();
					$('.close-btn').click(function(e) {
						e.preventDefault();
						$('.' + popupClass).fadeOut();
					});
				}

				$('.share, .favor, .decla').click(function (e) {
					e.preventDefault();
					var popupClass = $(this).data('popup');
					togglePopup('info-pop.' + popupClass);
				});
			});
		</script>



	

 


# 오늘하루안보기 - 레이어팝업

        <!doctype html>
        <html lang="ko">
        <head>

        <!-- Layer popup start -->
        <script language="JavaScript">
		    function setCookie( name, value, expiredays ) {
			    var todayDate = new Date();
				    todayDate.setDate( todayDate.getDate() + expiredays );
				    document.cookie = name + "=" + escape( value ) + "; path=/; expires=" + todayDate.toGMTString() + ";"
			    }

		    function closeWin() {
			    if ( document.notice_form.chkbox.checked ){
				    setCookie( "maindiv", "done" , 1 );
			    }
			    document.all['divpop'].style.visibility = "hidden";
		    }
	    </script>
        <!-- Layer popup end -->

        </head>

        
        <body>
   
        <!-- POPUP start -->
        <div id="divpop" style="position:absolute;left:100px;top:150px;z-index:200;visibility:hidden;">
         <table width=490px height=340px cellpadding=0 cellspacing=0>
	        <tr>
	        	<td style="border:1px #666666 solid" height=340px align=center bgcolor=white> 
	        		<a href="http://www.naver.com"><img src="이미지링크" width=490px height=340px alt="설명설명"></a>
	        	</td>
	        </tr>
	        <tr>
	        	<td height=10 bgcolor="#000000">
	        	</td>
	        </tr>
	        <tr>
		        <form name="notice_form">
		        	<td height=25 align=right bgcolor="#000000" valign=middle>
		        		<input type="checkbox" name="chkbox" value="checkbox"> <font color=#eeeeee>오늘 하루 이 창을 열지 않음 </font>
		        		<a href="javascript:closeWin();"> <font color=#eeeeee> <B>[닫기]</B> </font></a>
	        		</td> 
	        	</form>
        	</tr>
        </table>

        <script language="Javascript">
	        cookiedata = document.cookie;   
        	if ( cookiedata.indexOf("maindiv=done") < 0 ){ document.all['divpop'].style.visibility = "visible"; }
        		else { document.all['divpop'].style.visibility = "hidden"; }
        </script>
        <!-- POPUP end -->

        </body>
        </html>





 # 특정날짜까지만 보이기 레이어팝업


		<div class="popBox" id="popBox"  tabindex="0">
    			<div class="popCntBox">
				<div class="in-cont" style="height:auto">
					<video src = "/upload_data/popup/popup/170382586436189.mp4" controls width="100%" height="auto"></video>
				</div>
        			<div class="popCloseBox">
            				<a href="#" class="noLink popToday">오늘하루안보기</a>
            				<a href="#" class="noLink popClose">닫기</a>
        			</div>
    			</div>
		</div>



		<script>
   			const date1 = new Date;
    			const date2 = new Date(2024, 0, 1, 6, 0, 0); // 시작날짜 (년,월,일,시,분,초)
    			const date3 = new Date(2024, 0, 5, 17, 59, 0); // 종료날짜
    			const popEl = document.getElementById("popBox");

    			// Check "오늘하루안보기" 
    			const isTodayHidden = localStorage.getItem("popBoxHidden") === date1.toDateString();

    			if (date1 < date2 || date1 > date3 || isTodayHidden) {
        			popEl.style.display = 'none';
    			}

    			// Add click event listener "오늘하루안보기"
    			const popTodayLink = document.querySelector('.popToday');
    			popTodayLink.addEventListener('click', function (event) {
        			event.preventDefault();

        			// Set a flag in local storage to remember that the user has clicked the link today
       				 localStorage.setItem("popBoxHidden", date1.toDateString());

        			popEl.style.display = 'none';
    			});
		</script> 





# 특정날짜 + 오늘하루 안보기
 
		<!-- s : 레이어 팝업 임시 -->
	<div>
	<style>
		#promotionBanner {
		position: fixed;
		top: 80px;
		left: 80px;
		z-index: 9999999;
		width: 500px;
		overflow: hidden;
		border: 5px solid #000;
		box-shadow: 1px 2px 8px 5px rgba(0, 0, 0, 0.2);
	}

	#promotionBanner .img {
		display: block;
	}

	#promotionBanner .img img {
		width: 100%;
	}

	#promotionBanner .popClose {
		background: #000;
		padding: 10px;
		overflow: hidden;
	}

	#promotionBanner .popClose label {
		float: left;
		font-size: 15px;
		color: #fff;
		padding-right: 10px;
	}

	#promotionBanner .popClose .btnClose {
		float: right;
		font-size: 15px;
		color: #fff;
	}

	@media all and (max-width:1000px) {
		#promotionBanner {
			top: 90px;
			left: 20px;
			width: 400px;
		}

		#promotionBanner .img {
			width: 100%;
		}
	}

	@media all and (max-width:680px) {
		#promotionBanner {
			top: 70px;
			left: 0px;
			width: 100%;
		}

		#promotionBanner .img {
			width: 100%;
		}
	}
</style>

	<script language="JavaScript">
		// 쿠키 저장 함수
		function setCookie(name, value, expiredays) {
			var todayDate = new Date();
			todayDate.setDate(todayDate.getDate() + expiredays);
			document.cookie = name + "=" + encodeURIComponent(value) + "; path=/; expires=" + todayDate.toUTCString() + ";";
		}

		// 쿠키 읽기 함수
		function getCookie(name) {
			var value = "; " + document.cookie;
			var parts = value.split("; " + name + "=");
			if (parts.length === 2) return decodeURIComponent(parts.pop().split(";").shift());
			return null;
		}

		$(document).ready(function () {
			// 현재 날짜
			var now = new Date();
			console.log("Current Date:", now);

			// 기한 날짜 설정: 2025년 1월 13일 오전 9시부터 2025년 1월 22일 오후 6시까지
			var deadlineStart = new Date("2025-01-15T09:00:00"); // 시작 날짜
			var deadlineEnd = new Date("2025-01-22T18:00:00"); // 종료 날짜
			console.log("Deadline Start Date:", deadlineStart);
			console.log("Deadline End Date:", deadlineEnd);

			// 쿠키 확인
			var topPopCookie = getCookie("topPop");
			console.log("TopPop Cookie:", topPopCookie);

			// 쿠키가 없거나, 현재 날짜가 설정된 기간 안에 있으면 팝업을 표시
			if (!topPopCookie && now >= deadlineStart && now <= deadlineEnd) {
				$('#promotionBanner').show();
				console.log("Popup shown");
			} else {
				$('#promotionBanner').hide();
				console.log("Popup not shown");
			}

			// 닫기 버튼 클릭 이벤트
			$("#promotionBanner .btnClose").click(function () {
				// 오늘만 보기 체크박스의 체크 여부를 확인해서 체크되어 있으면 쿠키를 생성한다.
				if ($("#chkday").is(':checked')) {
					setCookie("topPop", "done", 1);
					console.log("Cookie set for topPop");
				}
				// 팝업창을 위로 애니메이트 시킨다. 혹은 slideUp()
				$('#promotionBanner').slideUp(500);
				console.log("Popup closed and sliding up");
			});
		});
		</script>

		<div id="promotionBanner" style="display:none;">
			<div class="popContents">
				<a href="#n" class="img"><img src="/portal/upload_data/board_data/BBS_0000130/173672678702303.jpg"
					alt="2025년 태화강 철새아카데미 5기 모집"></a>
				<div class="popClose">
					<input type="checkbox" value="checkbox" name="chkbox" id="chkday" /><label for="chkday">오늘 하루 그만보기
					</label>
					<a href="#none" class="btnClose">닫기</a>
				</div>
			</div>
		</div>

		<script language="Javascript">
		//저장된 해당 쿠키가 있으면 창을 안 띄운다 없으면 뛰운다.
		cookiedata = document.cookie;
		if (cookiedata.indexOf("topPop=done") < 0) {
			document.all['promotionBanner'].style.display = "block";
		} else {
			document.all['promotionBanner'].style.display = "none";
		}
		</script>
		<!-- e: 레이어 팝업 임시 -->
