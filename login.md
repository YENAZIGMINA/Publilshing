

    <body>
    <div class="login-wrapper">
        <h2>Login</h2>
        <form method="post" action="서버의url" id="login-form">
            <input type="text" name="userName" placeholder="Email">
            <input type="password" name="userPassword" placeholder="Password">
            <label for="remember-check">
                <input type="checkbox" id="remember-check">아이디 저장하기
            </label>
            <input type="submit" value="Login">
        </form>
    </div>
    </body>


# 체크박스 커스텀 (이미지 넣기)
        <div>
          <input type="checkbox" id="remember-check">
          <label for="remember-check" class="ck01"></label> //체크박스
          <label for="remember-check" class="ck02">아이디 저장하기</label>
        </div>


        div {display: flex; align-items: center;}
        input[type="checkbox"] {display: none;} //기존체크박스 숨기기
        input[type="checkbox"] + label {
            display: inline-block;
            width: 24px;
            height: 24px;
            background: url(./img/check-line-w.png) no-repeat center rgb(110, 110, 228);  //베이직 체크
            border-radius: 50%;
            padding: 2px;
            position: relative;
        }
        input[type="checkbox"]:checked + label::after {
            content: '';
            position: absolute;
            top: 2px;
            left: 2px;
            background: url(./img/check-line.png) no-repeat center;   //색상변화 체크
            width: 24px;
            height: 24px;
            font-size: 25px;
            text-align: center;
        }
        label.ck02 {margin-left: 8px;}
