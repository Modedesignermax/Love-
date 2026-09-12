<!DOCTYPE html>
<html lang="de">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
body {
    margin: 0;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    background: #050005;
    overflow: hidden;
}

.heart {
    font-size: 160px;
    opacity: 0;
    transform: scale(0.1);
    animation: erscheinen 5s ease-out forwards;
    filter: drop-shadow(0 0 30px #ff1744);
}

@keyframes erscheinen {
    0% {
        opacity: 0;
        transform: scale(0.1);
    }

    30% {
        opacity: 0.2;
        transform: scale(0.4);
    }

    60% {
        opacity: 0.6;
        transform: scale(0.8);
    }

    85% {
        opacity: 0.9;
        transform: scale(1.05);
    }

    100% {
        opacity: 1;
        transform: scale(1);
    }
}
</style>
</head>

<body>

<div class="heart">❤️</div>

</body>
</html>
