<div class="container">
    <a href="/blog" class="xd">Вернуться в каталог фильмов</a>
    <slot />
</div>

<style>
    .container {
        margin: 50px auto;
        max-width: 800px;
        padding: 0 20px;
        text-align: center; 
    }
    .xd {
        display: inline-block;
        padding: 25px 270px; 
        margin-bottom:-60px; 
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


        @keyframes fadeIn {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }
</style>


