<!-- Register.svelte -->
<script>
    let username = "";
    let password = "";

    async function register() {
        // Здесь можно написать код для отправки запроса на сервер для регистрации
        alert(`Пользователь ${username} успешно зарегистрирован`);
    }
</script>

<style>
    /* Здесь можно написать стили для формы регистрации */
</style>

<h1>Регистрация</h1>

<form on:submit|preventDefault={register}>
    <label>
        Имя пользователя:
        <input type="text" bind:value={username} required>
    </label>
    <label>
        Пароль:
        <input type="password" bind:value={password} required>
    </label>
    <button type="submit">Зарегистрироваться</button>
</form>

<p>Уже есть аккаунт? <a href="/login">Войти</a></p>
