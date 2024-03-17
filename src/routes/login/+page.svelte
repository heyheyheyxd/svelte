<script>
    import { onMount } from 'svelte';

    let username = '';
    let isLoggedIn = false;

    // Проверяем, сохранено ли имя пользователя при загрузке страницы
    onMount(() => {
        const savedUsername = localStorage.getItem('username');
        if (savedUsername) {
            username = savedUsername;
            isLoggedIn = true;
        }
    });

    function login() {
        if (username.trim() !== "") {
            isLoggedIn = true;
            localStorage.setItem('username', username); // Сохраняем имя пользователя в локальное хранилище
        }
    }

    function logout() {
        isLoggedIn = false;
        username = '';
        localStorage.removeItem('username'); // Удаляем имя пользователя из локального хранилища
    }
</script>

{#if isLoggedIn}
    <div>
        <h1>Добро пожаловать, {username}!</h1>
        <button on:click={logout}>Выйти</button>
    </div>
{:else}
    <div>
        <h1>Войдите, чтобы продолжить</h1>
        <input type="text" bind:value={username} placeholder="Введите ваше имя">
        <button on:click={login}>Войти</button>
    </div>
{/if}




