![image](https://github.com/YENAZIGMINA/Publilshing/assets/129706758/4576a286-3de6-4b0a-b3fd-0be75f2a4b1b)

    
    
    <ul>
        <li>Item One</li>
        <li>Item Two</li>
        <li>Item Three</li>
        <li class="slider"></li>
    </ul>


    <style>
        @import url(https://fonts.googleapis.com/css?family=Lato:100,300,400,700);

        * {box-sizing: border-box;}
        body {font-family: 'Lato', sans-serif; background: #222; }
        ul {font-size: 0; position: relative; padding: 0; width: 480px;  margin: 40px auto; user-select: none;}
        li {display: inline-block; width: 160px; height: 60px; background: #39CCCC; font-size: 16px;
            text-align: center; line-height: 60px; color: #fff; text-transform: uppercase; position: relative;
            overflow: hidden; cursor: pointer;}
        .slider {display: block;position: absolute;bottom: 0;left: 0;height: 4px;background: yellow;transition: all 0.5s;}

        /*  Ripple */
        .ripple {width: 0;height: 0;border-radius: 50%;background: rgba(255, 255, 255, 0.4);transform: scale(0);
                  position: absolute;opacity: 1;}
        .rippleEffect {animation: rippleDrop .6s linear;}

        @keyframes rippleDrop {
            100% {
                transform: scale(2);
                opacity: 0;
            }
        }
    </style>



    <script>
        $("ul li").click(function (e) {
            if ($(this).hasClass('slider')) {
                return;
            }

            /* Add the slider movement */
            var whatTab = $(this).index();

            // Work out how far the slider needs to go (=li 넓이값)
            var howFar = 160 * whatTab;
            $(".slider").css({left: howFar + "px"});

            /* Add the ripple */
            // Remove olds ones
            $(".ripple").remove();
            // Setup
            var posX = $(this).offset().left,
                posY = $(this).offset().top,
                buttonWidth = $(this).width(),
                buttonHeight = $(this).height();

            // Add the element
            $(this).prepend("<span class='ripple'></span>"); //prepend : 선택한요소의 자식요소 앞에 내용삽입

            // Make it round!
            if (buttonWidth >= buttonHeight) {
                buttonHeight = buttonWidth;
            } else {
                buttonWidth = buttonHeight;
            }

            // Get the center of the element
            var x = e.pageX - posX - buttonWidth / 2;
            var y = e.pageY - posY - buttonHeight / 2;

            // Add the ripples CSS and start the animation
            $(".ripple").css({
                width: buttonWidth,
                height: buttonHeight,
                top: y + 'px',
                left: x + 'px'
            }).addClass("rippleEffect");
        });
    </script>
    
    
