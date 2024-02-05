
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


  
