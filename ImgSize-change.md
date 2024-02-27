# Img 사이즈 반응형


    ✔️반응형 max-width / 백그라운드 이미지로 넣을 때 조절 (패딩에 백그라운드 이미지 들어갈 수 있음)
![image](https://github.com/YENAZIGMINA/Publilshing/assets/129706758/8f7d143c-a135-4a4d-880f-adb6b84ff7f7)


    ✔️반응형 가변적으로 div 넓이, 높이 비율 유지 (position 있을 경우)
![image](https://github.com/YENAZIGMINA/Publilshing/assets/129706758/6fe50ae1-ac8c-4bd7-be83-824ec4707bed)


    ✔️미디어쿼리를 활용하여 이미지 변환

    <picture>
        <source srcset="images/f.png" media="(max-width: 400px)">
        <source srcset="images/e.png" media="(max-width: 576px)">
        <source srcset="images/d.png" media="(max-width: 768px)">
        <source srcset="images/c.png" media="(max-width: 992px)">   
        <source srcset="images/b.png" media="(max-width: 1140px)">
        <img src="images/a.png">
    </picture>
