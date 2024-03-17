<!-- MoreInfo.svelte -->
<script>
    import { onMount } from 'svelte';

    let isVisible = false;

    // Функция для обновления страницы
    function refreshPage() {
        window.location.reload();
    }

    // Функция для форматирования времени
    function formatTime(time) {
        return new Date(time).toLocaleString();
    }

    onMount(() => {
        isVisible = true;
    });
</script>

<div class="container">
    <h1>
        Дополнительная информация
    </h1>

    <p class={isVisible ? 'fade-in' : ''}>
        Добро пожаловать на страницу "Дополнительная информация"! В нашем магазине мы предлагаем широкий выбор игровых товаров:
    </p>

    <!-- Остальной контент -->

    <p class={isVisible ? 'fade-in' : ''}>
        Не упустите возможность приобрести игры и аксессуары по выгодным ценам! Для получения дополнительной информации свяжитесь с нами по телефону или по электронной почте.
    </p>

    <button class="refresh-button" on:click={refreshPage}>Обновить страницу</button>

    <p>Последнее обновление страницы: {formatTime(Date.now())}</p>
</div>

<style>
    h1 {
        font-size: 2rem;
        color: #333;
        margin-bottom: 20px;
        cursor: pointer; /* Добавляем курсор при наведении */
        transition: color 0.3s ease-in-out; /* Добавляем плавный переход цвета */
    }

    h1:hover {
        color: #ff6600; /* Изменяем цвет при наведении */
    }

    .container {
        max-width: 800px;
        margin: 0 auto;
        padding: 20px;
        background-color: #f4f4f4; /* Устанавливаем фоновый цвет */
        border-radius: 10px;
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.1); /* Добавляем тень */
    }

    .refresh-button {
        background-color: #007bff;
        color: white;
        border: none;
        padding: 10px 20px;
        border-radius: 5px;
        cursor: pointer;
        margin-top: 20px;
        transition: background-color 0.3s ease-in-out; /* Плавный переход цвета фона */
    }

    .refresh-button:hover {
        background-color: #0056b3; /* Изменяем цвет при наведении */
    }
</style>











