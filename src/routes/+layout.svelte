<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Heyheyhey Cinema</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
        }
        nav {
            background-color: rgba(0, 0, 0, 0.7);
            color: #fff;
            padding: 10px 0;
        }
        .nav-container {
            max-width: 1400px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 20px;
        }
        .nav-logo {
            text-decoration: none;
            font-size: 24px;
            font-weight: bold;
            color: #ff0000;
        }
        .nav-links {
            display: flex;
        }
        .nav-links .link {
            text-decoration: none;
            color: #ff0000;
            margin-left: 20px;
        }
        .container {
            max-width: 1400px;
            margin: 50px auto;
            padding: 0 20px;
        }
    </style>
</head>
<body>
    <nav>
        <div class="nav-container">
            <a href="/" class="nav-logo" title="Back to home">Heyheyhey Cinema</a>
            <div class="nav-links">
                <a href="/about" class="link">О кинотеатре</a>
                <a href="/blog" class="link">Каталог</a>
                <a href="/login" class="link">Анонс</a>
                <a href="/contact" class="link">Контакты</a>
                <a href="/kors" class="link">Отзывы</a>
            </div>
        </div>
    </nav>

    <div class="container">
        <!-- Pages will be injected below -->
        <slot></slot>
    </div>
</body>
</html>
