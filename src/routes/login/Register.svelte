<!-- Register.svelte -->
<script>
    let username = "";

    function handleUsernameChange(event) {
        username = event.target.value;
    }

    function handleRegister() {
        // Здесь вы можете отправить данные пользователя на сервер для регистрации
        alert(`Пользователь с ником ${username} успешно зарегистрирован!`);
    }
</script>

<h1>Регистрация</h1>

<label>
    Ник:
    <input type="text" bind:value={username} on:input={handleUsernameChange} required>
</label>

<button on:click={handleRegister}>Зарегистрироваться</button>


