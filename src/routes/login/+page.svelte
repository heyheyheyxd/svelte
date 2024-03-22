<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Анонсы фильмов</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-image: url('https://top-fon.com/uploads/posts/2023-01/1674815996_top-fon-com-p-kinoteatr-fon-dlya-prezentatsii-85.jpg');
            background-size: cover;
            background-position: center;
            color: #ffffff; /* белый цвет текста */
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
            width: 48%; /* Ширина блока фильма, чтобы два фильма помещались на одной строке */
            margin-bottom: 30px;
            background-color: #000000; /* черный цвет фона */
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(255, 0, 0, 0.3); /* красная тень */
        }

        .movie img {
            width: 100%;
            height: 200px; /* Фиксированная высота изображения */
            object-fit: cover; /* Растягиваем изображение, чтобы оно полностью заполнило свой контейнер */
            border-radius: 8px 8px 0 0; /* Закругление верхних углов изображения */
        }

        .movie-content {
            padding: 20px;
        }

        .movie h2 {
            font-size: 1.8rem;
            color: #ff0000; /* красный цвет заголовка фильма */
            margin-bottom: 10px;
        }

        .movie p {
            font-size: 1.2rem;
            color: #aaaaaa; /* серый цвет текста */
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
    </style>
</head>
<body>
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
        // Анимация появления элементов
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















