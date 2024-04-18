# input:placeholder-shown 글자입력시 하단 텍스트 나오게
    
    
    <input type="text" class="input-txt" placeholder="글자를 입력하세요">
    <p class="input-msg">입력완료!</p>


    <style>
    .input-txt:placeholder-shown {border-color: rgb(219, 219, 147);}
    .input-txt:placeholder-shown + .input-msg {display: none;}
    </style>




# input 숫자만 작성가능 하도록1

        <input type="text" size="40" onkeyup="setNum(this);">
        <textarea onkeyup="setNum(this);"></textarea>


        <script type="text/javascript">
            function setNum (obj){
                val = obj.value;
                re=/[^0-9]/gi;
                obj.value=val.replace(re,"");
            }
        </script>


# input 숫자만 작성가능 하도록2
        <input type="text" oninput="this.value = this.value.replace(/[^0-9.]/g, '').replace(/(\..*)\./g, '$1');" />


# input CapsLock 문구넣기
        <input type="text" id="name" onkeyup="checkCapsLock(event)">
        <div id="message"></div>

        <script>
        
            function checkCapsLock(event) {
                if(event.getModifierState("CapsLock")){
                    document.getElementById("message").innerText = "CapsLock이 켜져 있습니다."
                } else {
                    document.getElementById("message").innerText = ""
                }
            }
    </script>
