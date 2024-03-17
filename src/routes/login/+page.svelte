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
        Добро пожаловать на страницу "Дополнительная информация"! В нашем магазине мы предлагаем широкий выбор игровых товаров:
    </p>

    <!-- Остальной контент -->

    <p class={isVisible ? 'fade-in' : ''}>
        Не упустите возможность приобрести игры и аксессуары по выгодным ценам! Для получения дополнительной информации свяжитесь с нами по телефону или по электронной почте.
    </p>

    <p>Последнее обновление страницы: {formatTime(Date.now())}</p>
</div>

<style>
    .background {
    background-color: #e0f3ff; /* Цвет фона, который вы хотите использовать */
}

    .container {
        max-width: 800px;
        margin: 0 auto;
        padding: 20px;
        background-color: #f4f4f4; /* Устанавливаем фоновый цвет */
        border-radius: 10px;
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.1); /* Добавляем тень */
    }

</style>
</body>












