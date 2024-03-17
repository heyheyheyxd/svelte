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
        }
        nav {
            background-color: #333;
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
            color: #fff;
        }
        .nav-links {
            display: flex;
        }
        .nav-links .link {
            text-decoration: none;
            color: #fff;
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
            <a href="/" class="nav-logo" title="Back to home">Heyheyhey shop</a>
            <div class="nav-links">
                <a href="/about" class="link">Обо мне</a>
                <a href="/blog" class="link">Каталог</a>
                <a href="/contact" class="link">Контакты</a>
            </div>
        </div>
    </nav>

    <div class="container">
        <!-- Pages will be injected below -->
        <slot></slot>
    </div>
</body>
</html>
