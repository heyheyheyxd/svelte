<!-- Login.svelte -->
<script>
    let username = "";
    let password = "";

    async function login() {
        // Здесь можно написать код для отправки запроса на сервер для аутентификации
        alert(`Вы вошли как ${username}`);
    }
</script>

<style>
    /* Здесь можно написать стили для формы входа */
</style>

<h1>Вход</h1>

<form on:submit|preventDefault={login}>
    <label>
        Имя пользователя:
        <input type="text" bind:value={username} required>
    </label>
    <label>
        Пароль:
        <input type="password" bind:value={password} required>
    </label>
    <button type="submit">Войти</button>
</form>

<p>Еще нет аккаунта? <a href="/register">Зарегистрироваться</a></p>
