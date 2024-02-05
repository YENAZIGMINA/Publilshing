## title로 전환텍스트 넣기


    <a href="#n" class="dkmode-btn" onclick="toggleDarkMode()" title="다크모드로 전환합니다">
      <span id="dark">다크모드</span>
    </a>

    <script>
        function toggleDarkMode() {
          var demoElement = document.getElementById("dark");
          var isDarkMode = demoElement.innerText === "다크모드";

          demoElement.innerText = isDarkMode ? "일반모드" : "다크모드";
          document.querySelector('.dkmode-btn').title = (isDarkMode ? "일반모드" : "다크모드") + "로 전환합니다";
        }
    </script>



## 태그추가로 전환텍스트 넣기

        <style>
            .hideTitle {
                width: 1px;
                height: 1px;
                overflow: hidden;
                position: absolute;
                top: -9999px;
                left: -9999px;
                display: block;
                text-indent: -9999px;
                font-size: 0px;
                line-height: 0;
            }
        </style>



         <a href="#n" class="dkmode-btn" onclick="toggleDarkMode()">
            <span id="dark">다크모드</span>
            <p class="hideTitle">다크모드로 전환합니다</p>
        </a>

        <script>
            function toggleDarkMode() {
                var demoElement = document.getElementById("dark");
                var isDarkMode = demoElement.innerText === "다크모드";
        
                demoElement.innerText = isDarkMode ? "일반모드" : "다크모드";
                document.querySelector('.hideTitle').innerText = (isDarkMode ? "일반모드" : "다크모드") + "로 전환합니다";
            }
        </script>
