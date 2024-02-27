

    <article id="area" data-board-section="board_notice">


    (JavaScript)
    var article = document.getElementById('area');
    article.getAttribute('data-board-section');	// "board_notice"
    article.dataset.boardSection;

    (jQuery)
    $("[data-board-section]").data("board-section");

    (css)
    article::before {content: attr(data-board-section);}
    article[data-board-section='board_notice'] {width: 600px;}
