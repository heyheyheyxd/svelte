<!-- MoreInfo.svelte -->
<script>
    import { onMount } from 'svelte';

    let isVisible = false;

    // Функция для форматирования времени
    function formatTime(time) {
        return new Date(time).toLocaleString();
    }

    onMount(() => {
        isVisible = true;
    });
</script>

<body class="background">
    <div class="container">
        <h1>Дополнительная информация</h1>
        <p class={isVisible ? 'fade-in' : ''}>
            Добро пожаловать на страницу "Дополнительная информация"! Здесь вы найдете всю необходимую информацию о наших продуктах и услугах.
        </p>

        <!-- Остальной контент -->

        <p class={isVisible ? 'fade-in' : ''}>
            Не упустите возможность окунуться в захватывающий мир развлечений! В нашем магазине вы найдете широкий выбор игровых товаров по самым привлекательным ценам.
        </p>

        <p class={isVisible ? 'fade-in' : ''}>
            Не забудьте принять участие в наших акциях и специальных предложениях, чтобы получить дополнительные бонусы и скидки!
        </p>

        <p class={isVisible ? 'fade-in' : ''}>
            Для получения дополнительной информации и консультаций свяжитесь с нашей дружелюбной командой поддержки по телефону или электронной почте.
        </p>

        <p>Последнее обновление страницы: {formatTime(Date.now())}</p>
    </div>

    <style>
                h1 {
            font-size: 2rem; /* Уменьшенный размер шрифта */
            color: #333;
            margin-bottom: 20px;
            text-align: center;
        }
        .background {
            background-color: #CCEEFF; 
        }

        .container {
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
            background-color: #CCCCFF; 
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        .container h1 {
            font-size: 2.5rem;
            color: #333;
            margin-bottom: 20px;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .container p {
            font-size: 1.2rem;
            color: #666;
            line-height: 1.6;
            margin-bottom: 20px;
        }
    </style>
</body>













