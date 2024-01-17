#Web Animation API

    var box = document.querySelector('.box');

        const animation = box.animate(
            [
            {transform:'translateX(50px)', opacity:0},
            {transform:'translateX(0)', offset:0.3}, //30% 지점
            {transform:'translateX(200px)', opacity:1}
        ], {
            duration:1000,
            easing:'linear',
            fill:'both',
            iterations:Infinity,
            direction:'alternate'
        }
        );

        animation.pause();
        console.log(animation.playState);

        window.addEventListener('click',()=>{
            animation.play();
            console.log(animation.playState);
        });
