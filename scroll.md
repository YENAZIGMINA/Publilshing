# scroll up, down 확인

    ▪ 삼항연산자로 확인

    <script>

      let lastScrollY=0; //이전 스크롤 위치를 변수에 담기

      window.addEventListener("scroll", (e)=>{
        let currentScrollY = window.scrollY; //현재 스크롤 위치(스크롤했을 경우 위치)를 변수에 담음

        lastScrollY < currentScrollY ? console.log("scroll down") : console.log("scroll up");
        //이전 스크롤위치(Y)가 현재 스크롤 위치(Y)보다 작을 경우 scroll down
        //이전 스크롤위치가 현재 스크롤 위치보다 클 경우 scroll up
        
        lastScrollY = currentScrollY; 
        // 이전 스크롤 위치에 현재 스크롤 위치 저장
        //(이 이벤트 다음에 스크롤 했을 때 현재있는 위치에서 위에 있는지 아래에 있는지 알기 위해)
      })

    </script>



    ▪if 조건으로 확인

      <script>

        let lastScrollY=0;

        window.addEventListener("scroll", (e)=>{
          let currentScrollY = window.scrollY;

          if(lastScrollY < currentScrollY){
            console.log("scroll down");
          };

          if(currentScrollY < lastScrollY) {
            console.log("scroll up")
          }

          lastScrollY = currentScrollY;
        })

      </script>
