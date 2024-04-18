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



# input 영문만 입력가능하도록
        <input type="text" oninput="handleOnInput(this)" />

        function handleOnInput(e)  {
              e.value = e.value.replace(/[^A-Za-z]/ig, '')
        }



# input - radio 클릭한 값 출력하기

        <input type="radio" name="gender" value="female" onclick="getGender(event)">여성
        <input type="radio" name="gender" value="male" onclick="getGender(event)">남성
        <div id="result"></div>


        function getGender(event) {
            document.getElementById('result').innerText = event.target.value;
        }



# chekbox 전체선택

        <input type="checkbox" name="animal" value="selectall" onclick="selectAll(this)">전체
        <br>
        <input type="checkbox" name="animal" value="dog">개
        <br>
        <input type="checkbox" name="animal" value="cat">고양이
        <br>
        <input type="checkbox" name="animal" value="rabbit">토끼

        <script>
        
            function selectAll(selectAll) {
                const checkboxs = document.getElementsByName('animal');

                    checkboxs.forEach((checkbox) => {
                        checkbox.checked = selectAll.checked;
                    });
                }

        </script>        
