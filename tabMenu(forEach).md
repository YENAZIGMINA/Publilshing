    <ul>
      <li class="tabMenu"><a href="#">menu1</a></li>
      <li class="tabMenu"><a href="#">menu2</a></li>
      <li class="tabMenu"><a href="#">menu3</a></li>
      <li class="tabMenu"><a href="#">menu4</a></li>
    </ul>

    <div class="tabContent_wrapper">
      <div class="tabDesc active" id="tab1">desc01</div>
      <div class="tabDesc" id="tab2">desc02</div>
      <div class="tabDesc" id="tab3">desc03</div>
      <div class="tabDesc" id="tab4">desc04</div>
    </div>


------------------------------------------------


    * {margin: 0; padding: 0;}
    ul {display: flex; margin: 20px; justify-content: center;}
    ul li {list-style: none; margin-right: 10px;}
    ul li a {text-decoration: none; width: 80px; display: inline-block; padding: 15px; background-color: tomato;
            color: #fff; font-size: 17px; text-align: center;}
    .tabDesc {display: none; text-align: center;}
    .tabDesc.active {display: block;}


------------------------------------------------


    const tabMenu = document.querySelectorAll(".tabMenu");
    const tabDesc = document.querySelectorAll(".tabDesc");

    tabMenu.forEach((item, index) => {
      item.addEventListener("click", (e) => {
      e.preventDefault();
    
      tabDesc.forEach((content) => {
        content.classList.remove("active");
      });

      tabMenu.forEach((content) => {
        content.classList.remove("active");
      });

      tabMenu[index].classList.add("active");
      tabDesc[index].classList.add("active");
    });
  });
    
