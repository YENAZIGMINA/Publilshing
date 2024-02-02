    // tabindex 속성 추가
    $('.popup-layer').css('display','block' ).attr('tabindex','0').focus();

    // tabindex 속성 삭제
    $('.popup-layer').css('display', 'none').removeAttr('tabindex');
