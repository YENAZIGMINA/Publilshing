# :not()  전체중 특정 요소 빼고 적용할 때
    .minu p:not(.except) {background-color: blanchedalmond;}

# ::selection   드래그시 색상변경
    .desc::selection {color: greenyellow; background-color: brown;}

# 첫글자만 대문자로 변경
    1) .txt::first-letter {text-transform: uppercase;}
    2) .txt {text-transform: capitalize;}

# input 첨부파일 확장자 지정
    <input type="file" accept="image/jpeg,.txt" />
