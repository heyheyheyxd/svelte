<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Heyheyhey Cinema</title>
    <style>
        
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            overflow-x: hidden; 
            background-image: url('https://top-fon.com/uploads/posts/2023-01/1674815996_top-fon-com-p-kinoteatr-fon-dlya-prezentatsii-85.jpg');
        }

        
        .container {
    max-width: 1200px;
    margin: 50px auto;
    padding: 20px;
    background-color: rgba(204, 204, 255, 0); 
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}


        /* Стили для информационного блока */
        .info {
            text-align: center;
            padding: 50px 0;
            background-color: rgba(204, 204, 255, 0);
        }

        .info h1 {
            font-size: 3rem;
            margin: 20px 0;
            color: #ff0000;
        }

        .info h2 {
            font-size: 1.5rem;
            font-weight: 400;
            color: #ff0000;
            margin-bottom: 20px;
        }
        .scroll-button {
            margin-top: 20px;
        }

        .scroll-button a {
            background-color: #ff0000;
            color: #fff;
            padding: 10px 20px;
            border-radius: 5px;
            text-decoration: none;
            transition: background-color 0.3s ease;
        }

        .scroll-button a:hover {
            background-color: #8b0000;
        }
        .arrow {
            width: 0;
            height: 0;
            border-left: 10px solid transparent;
            border-right: 10px solid transparent;
            border-top: 10px solid #ffffff;
            margin-left: 5px;
            display: inline-block;
            vertical-align: middle;
        }
    </style>
</head>
<body class="background">
    <div class="container">
        <div class="info">
            <h1>Добро пожаловать в Heyheyhey Cinema</h1>
            <h2>Кинотеатр: выбирайте лучшие фильмы для вашего удовольствия.</h2>
            <div class='scroll-button animate-scroll'>
                <a href='/blog'>Узнать больше <span class="arrow"></span></a>
            </div>
        </div>
    </div>

    <div class="background-div"></div>
</body>
</html>



