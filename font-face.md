▪ TTF(True Type Font)는 용량이 큼 / EOT(Embedding Open Type) / WOFF(Web Open Font Format) 사용

▪ IE6~8 브라우저는 EOT를 지원. 불필요하게 WOFF파일까지 요청 할 필요가 없음 ->  local(※)이라는 구문을 넣어서 WOFF의 요청을 막음

format('woff') 포맷 타입은 이 형식을 지원하는 브라우저만 글꼴을 내려받게 되어 있다.


    @font-face{
      font-family:ng;
      src:url(NanumGothic.eot);
      src:local(※), url(NanumGothic.woff) format('woff')
      }



※ 기호는 사용자 시스템에 존재하지 않을만한 글꼴을 임의로 지정한 것. 

굳이 2byte짜리 특수문자를 사용한 이유는 Mac OS에서 2byte짜리 문자열로 된 시스템 글꼴 이름은 아예 처리하지 않기 때문.

(IE6~8 브라우저가 두번째 src속성을 해석하지 못하도록 하기 위함. local값의 용도는 사용자 로컬 시스템 글꼴이 있는 경우 참조하는 것인데

Mac 컴퓨터는 시스템 글꼴 이름이 모두 1바이트로 되어 있기 때문에 2바이트 이름을 사용해서 아예 제외.

local값은 비워두면 안되기 때문에 반드시 넣어야 하고 여기에 로컬에 전혀 없을만한 글꼴이름을 넣는다.)






    @font-face {
    font-family: 'GmarketSans';
    font-style: normal;
    font-weight: 100;
    src:url('/font/GmarketSansLight.woff') format('woff'), 
      url('/font/GmarketSansTTFLight.ttf') format('truetype');
    }
