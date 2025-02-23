<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>⚪️が動くサイト</title>
    <style>
        body {
            margin: 0;
            overflow: hidden;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background-color: #f0f0f0;
        }

        #circle {
            width: 50px;
            height: 50px;
            background-color: #3498db;
            border-radius: 50%;
            position: absolute;
            transition: transform 0.1s;
        }
    </style>
</head>
<body>

<div id="circle"></div>

<script>
    let circle = document.getElementById('circle');
    let positionX = window.innerWidth / 2 - 25;
    let positionY = window.innerHeight / 2 - 25;

    circle.style.left = positionX + 'px';
    circle.style.top = positionY + 'px';

    document.addEventListener('keydown', function(event) {
        if (event.key === ' ') {  // スペースキーを押したとき
            positionX = Math.random() * (window.innerWidth - 50); // 画面幅内でランダム
            positionY = Math.random() * (window.innerHeight - 50); // 画面高さ内でランダム

            // 新しい位置に円を移動
            circle.style.left = positionX + 'px';
            circle.style.top = positionY + 'px';
        }
    });
</script>

</body>
</html>
