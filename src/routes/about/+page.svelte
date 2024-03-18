<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Обо мне - Heyheyhey Digital Store</title>
    <style>
        .background {
            background-color: #CCEEFF;
        }

        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f0f0f0;
        }

        .container {
            max-width: 800px;
            margin: 50px auto;
            padding: 20px;
            background-color: #CCCCFF;
            border-radius: 8px;
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.1);
        }

        .content {
            padding: 20px;
            text-align: center;
        }

        .content h2 {
            font-size: 2.5rem;
            color: #333;
            margin-bottom: 20px;
            text-transform: uppercase;
            letter-spacing: 2px;
            border-bottom: 2px solid #007bff; /* Добавляем подчеркивание */
            display: inline-block;
            padding-bottom: 10px;
        }

        .content p {
            font-size: 1.2rem;
            color: #666;
            line-height: 1.6;
            margin-bottom: 20px;
        }

        .underline {
            text-decoration: none;
            color: #007bff;
        }

        .underline:hover {
            text-decoration: underline;
        }

        .btn {
            display: inline-block;
            padding: 12px 24px;
            background-color: #007bff;
            color: #fff;
            border: none;
            border-radius: 5px;
            font-size: 1.2rem;
            text-transform: uppercase;
            cursor: pointer;
            transition: background-color 0.3s ease;
            text-decoration: none; /* Убираем подчеркивание для ссылки */
        }

        .btn:hover {
            background-color: #0056b3;
        }

        .arrow {
            border: solid #fff;
            border-width: 0 3px 3px 0;
            display: inline-block;
            padding: 3px;
            transform: rotate(-45deg);
            -webkit-transform: rotate(-45deg);
            margin-left: 5px;
        }
    </style>
</head>
<body class="background">
    <div class="container">
        <div class="content">
            <h2>Обо мне</h2>
            <p>Привет! Меня зовут Усимов Дмитрий и я основатель <span class="underline">Heyheyhey Digital Store</span>. Наш магазин предлагает широкий выбор цифровых товаров, включая программное обеспечение, музыку, книги, видеоигры и многое другое.</p>
            <p>Мы стремимся предоставить нашим клиентам лучший опыт покупок, обеспечивая качественный сервис и быструю доставку цифровых товаров. Наша команда гордится тем, что мы можем помочь вам найти именно то, что вам нужно.</p>
            <p>Спасибо, что выбрали наш магазин!</p>
            <a href='/login' class="btn">Узнать больше <span class="arrow"></span></a>
        </div>
    </div>
</body>
</html>


