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
