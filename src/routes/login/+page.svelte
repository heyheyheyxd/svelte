<!-- src/routes/login/index.svelte -->
<script>
    let message = 'Введите свой ник';

    function setUsername() {
        const username = prompt("Введите свой ник:");
        if (username !== null && username.trim() !== "") {
            message = `Привет, ${username}!`;
        }
    }
</script>

<div>
    <h1>{message}</h1>
    <button on:click={setUsername}>Войти или зарегистрироваться</button>
</div>








