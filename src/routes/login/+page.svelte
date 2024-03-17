<script>
    let username = '';
    let isLoggedIn = false;
    
    function displayUsername() {
        if (username.trim() !== "") {
            isLoggedIn = true;
        }
    }
</script>

{#if isLoggedIn}
    <h1>Привет, {username}!</h1>
{:else}
    <h1>Войти или зарегистрироваться</h1>
    <input type="text" bind:value={username} placeholder="Введите ваш ник">
    <button on:click={displayUsername}>Войти</button>
{/if}

