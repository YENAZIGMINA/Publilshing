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
