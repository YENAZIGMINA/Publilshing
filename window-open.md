

    ■ 기본
    
    var win = window.open("/popup.html", "PopupWin", "width=500,height=600");


    ■ 창 컨트롤을 모두 활성화
    
    var win = window.open("/popup.html", "_blank", "toolbar=yes,scrollbars=yes,resizable=yes,top=500,left=500,width=400,height=400");


    
    var win = window.open("", "PopupWin", "width=500,height=600");
    win.document.write("<p>새창에 표시될 내용 입니다.</p>");





# js - window.open


    <button onclick="popup()">popup naver</button>

    function popup(){
        let options = "toolbar=no,scrollbars=no,resizable=yes,status=no,menubar=no,width=1200, height=800, top=0,left=0";
          window.open("http://www.naver.com","_blank", options);
    };




# a태그 - window.open

    <a href="https://www.naver.com/" onclick="window.open(this.href, '_blank', 'width=800, height=600'); return false;">
        클릭 시 팝업 창으로 이동합니다
    </a>
