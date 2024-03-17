<script>
    let username = '';
    
    function displayUsername() {
        if (username.trim() !== "") {
            alert(`Привет, ${username}!`);
        }
    }
</script>

<h1>{username ? `Привет, ${username}!` : 'Войти или зарегистрироваться'}</h1>
<input type="text" bind:value={username} placeholder="Введите ваш ник">
<button on:click={displayUsername}>Войти</button>
