<div class="container">
    <a href="/blog" class="xd">Вернуться в каталог фильмов</a>
    <slot />
</div>

<style>
    .container {
        margin: 50px auto;
        max-width: 800px;
        padding: 0 20px;
        text-align: center; /* Центрирование контента внутри контейнера */
    }
    .xd {
        display: inline-block;
        padding: 25px 270px; /* Увеличенные отступы по горизонтали */
        margin-bottom:-60px; /* Увеличенный отступ снизу */
        margin-left: 17px;
        white-space: nowrap;
        background-color: #ff0000;
        color: #fff;
        text-decoration: none;
        border-radius: 5px;
        transition: background-color 0.3s ease;
    }

    .xd:hover {
        background-color: #8b0000;
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
        max-height: 300px; /* Максимальная высота изображения */
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
</style>


