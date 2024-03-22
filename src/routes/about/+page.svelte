<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>О кинотеатре - Heyheyhey Cinema</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #990000; /* Красный цвет фона */
            background-image: url('https://top-fon.com/uploads/posts/2023-01/1674815996_top-fon-com-p-kinoteatr-fon-dlya-prezentatsii-85.jpg');
        }

        .container {
            max-width: 800px;
            margin: 50px auto;
            padding: 20px;
            border-radius: 8px;
            background-color: rgba(0, 0, 0, 0.7); /* Черный цвет с полупрозрачностью */
            box-shadow: 0 0 20px rgba(255, 255, 255, 0.1); /* Тень белого цвета */
        }

        .content {
            padding: 20px;
            text-align: center;
        }

        .content h2 {
            font-size: 2.5rem;
            color: #ffffff; /* Белый цвет текста */
            margin-bottom: 20px;
            text-transform: uppercase;
            letter-spacing: 2px;
            border-bottom: 2px solid #ff0000; /* Красная граница снизу */
            display: inline-block;
            padding-bottom: 10px;
        }

        .content p {
            font-size: 1.2rem;
            color: #ffffff; /* Белый цвет текста */
            line-height: 1.6;
            margin-bottom: 20px;
        }

        .underline {
            text-decoration: none;
            color: #ffffff; /* Белый цвет текста */
        }

        .underline:hover {
            text-decoration: underline;
        }

        .btn {
            display: inline-block;
            padding: 12px 24px;
            background-color: #ff0000; /* Красный цвет кнопки */
            color: #ffffff; /* Белый цвет текста кнопки */
            border: none;
            border-radius: 5px;
            font-size: 1.2rem;
            text-transform: uppercase;
            cursor: pointer;
            transition: background-color 0.3s ease;
            text-decoration: none; /* Убираем подчеркивание для ссылки */
        }

        .btn:hover {
            background-color: #660000; /* Темно-красный цвет при наведении */
        }

        .arrow {
            border: solid #ffffff; /* Белая граница стрелки */
            border-width: 0 3px 3px 0;
            display: inline-block;
            padding: 3px;
            transform: rotate(-45deg);
            -webkit-transform: rotate(-45deg);
            margin-left: 5px;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="content">
            <h2>О кинотеатре</h2>
            <p>Добро пожаловать в кинотеатр "Heyheyhey Cinema"! Мы рады предложить вам самые лучшие фильмы и захватывающие сеансы для всей семьи.</p>
            <p>Наши залы оснащены передовым оборудованием и созданы для того, чтобы вы могли насладиться каждым кадром великолепных кинолент.</p>
            <p>Присоединяйтесь к нам и окунитесь в мир кинофантазий!</p>
            <a href='/blog' class="btn">Расписание сеансов <span class="arrow"></span></a>
        </div>
    </div>
</body>
</html>




