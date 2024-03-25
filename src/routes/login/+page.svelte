<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Анонсы фильмов</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-image: url('https://zakon.ru/Content/entriesattachments/7f1c9f22-5ff4-49bb-b597-70223d6014de.jpg');
            background-size: cover;
            background-position: center;
            color: #ffffff; 
        }

        .container {
            max-width: 1200px;
            margin: 50px auto;
            padding: 20px;
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
        }

        .movie {
            width: 48%; 
            margin-bottom: 30px;
            background-color: #000000; 
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(255, 0, 0, 0.3); 
        }

        .movie img {
            width: 100%;
            height: 300px; 
            object-fit: cover; 
            border-radius: 8px 8px 0 0; 
        }

        .movie-content {
            padding: 20px;
        }

        .movie h2 {
            font-size: 1.8rem;
            color: #ff0000; 
            margin-bottom: 10px;
        }

        .movie p {
            font-size: 1.2rem;
            color: #aaaaaa; 
            margin-bottom: 10px;
        }

        .fade-in {
            animation: fadeIn 1s ease-in-out;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }
        .back-to-catalog {
    background-color: red;
    color: white;
    padding: 20px 470px; /* Увеличиваем отступы для создания более длинной кнопки */
    text-decoration: none;
    border-radius: 5px;
    margin-top: 10px;
    display: block;
    width: fit-content;
    margin-left: auto;
    margin-right: auto;
}


        .back-to-catalog:hover {
            background-color: #ff3333;
        }
    </style>
</head>
<body>
    <a href="/blog" class="back-to-catalog">Вернуться в каталог фильмов</a>
    <div class="container">
        <div class="movie fade-in">
            <img src="https://www.proficinema.com/upload/iblock/cf0/cf0a6ea1e13c0c42a2bc2f0cb053ce94.jpg" alt="Пила">
            <div class="movie-content">
                <h2>Пила </h2>
                <p>Жанр: ужасы, триллер</p>
                <p>Режиссер: Джеймс Ван</p>
                <p>Дата выхода: 2003</p>
            </div>
        </div>

        <div class="movie fade-in">
            <img src="https://wallpapercosmos.com/w/full/c/b/a/352680-1920x1080-desktop-full-hd-taxi-movie-wallpaper.jpg" alt="Такси">
            <div class="movie-content">
                <h2>Такси </h2>
                <p>Жанр: комедия, боевик</p>
                <p>Режиссер: Жерар Пирес</p>
                <p>Дата выхода: 1998</p>
            </div>
        </div>

        <div class="movie fade-in">
            <img src="https://sun9-35.userapi.com/hCWfxGwcuIRvmfKQXwr9OZNN4mu4ERi538DsZg/QlzDt8Eazmk.jpg" alt="Форсаж">
            <div class="movie-content">
                <h2>Форсаж</h2>
                <p>Жанр: боевик, триллер</p>
                <p>Режиссер: Роб Коэн</p>
                <p>Дата выхода: 2001</p>
            </div>
        </div>

        <div class="movie fade-in">
            <img src="https://animezavod.ru/wp-content/uploads/2023/10/1647340681_31-kartinkin-net-p-begushchii-v-labirinte-kartinki-35.jpg" alt="Бегущий в лабиринте">
            <div class="movie-content">
                <h2>Бегущий в лабиринте</h2>
                <p>Жанр: фантастика, триллер</p>
                <p>Режиссер: Уэс Болл</p>
                <p>Дата выхода: 2014</p>
            </div>
        </div>
    </div>

    <script>
        
        window.onload = function () {
            const elements = document.querySelectorAll('.fade-in');
            elements.forEach(element => {
                element.style.opacity = 0;
                element.style.animation = 'fadeIn 1s ease-in-out forwards';
            });
        };
    </script>
</body>
</html>














