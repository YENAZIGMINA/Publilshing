# display:table로 반응형

    <div class="tc">
      <div>가나다</div>
      <div>가나다</div>
      <div>가나다</div>
    </div>


    .tc {display: table; table-layout: fixed; width: 100%;}
    .tc div {display: table-cell; vertical-align: middle;}


    ----------------------------------------------------------------


# table 스크롤 (scroll)
감싸는 태그에 oveflow:auto 적용

    <div class="scroll-table">
      <table>
      </table>
    </div>
    
    .table-wrap .scroll-table {overflow-x: auto;}


    ---------------------------------------------------------------


    
