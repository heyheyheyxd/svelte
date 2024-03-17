<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Heyheyhey Shop</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f9f9f9;
        }

        .container {
            max-width: 1400px;
            margin: 50px auto;
            padding: 20px;
            background-color: #fff;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        .info {
            text-align: center;
            padding: 50px 0;
        }

        .info h1 {
            font-size: 3rem;
            margin: 20px 0;
            color: #333;
        }

        .info h2 {
            font-size: 1.5rem;
            font-weight: 400;
            color: #666;
            margin-bottom: 20px;
        }

        .background-div {
            background-color: #333;
            height: 300px;
            margin: 0 -20px;
            border-bottom-left-radius: 10px;
            border-bottom-right-radius: 10px;
        }

        .scroll-button {
            margin-top: 20px;
        }

        .scroll-button a {
            background-color: #333;
            color: #fff;
            padding: 10px 20px;
            border-radius: 5px;
            text-decoration: none;
            transition: background-color 0.3s ease;
        }

        .scroll-button a:hover {
            background-color: #555;
        }

        .arrow {
            width: 0;
            height: 0;
            border-left: 10px solid transparent;
            border-right: 10px solid transparent;
            border-top: 10px solid #333;
            margin-left: 5px;
            display: inline-block;
            vertical-align: middle;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="info">
            <h1>Добро пожаловать в Heyheyhey Shop</h1>
            <h2>Магазин стильной одежды и кроссовок для вашего активного образа жизни.</h2>
            <div class='scroll-button animate-scroll'>
                <a href='/about'>Узнать больше <span class="arrow"></span></a>
            </div>
        </div>
    </div>

    <div class="background-div"></div>
</body>
</html>
