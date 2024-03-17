<!-- LoginPage.svelte -->
<script>
    let username = '';
    let isLoggedIn = false;

    function login() {
        if (username.trim() !== "") {
            isLoggedIn = true;
        }
    }
</script>

{#if isLoggedIn}
    <div>
        <h1>Добро пожаловать, {username}!</h1>
    </div>
{:else}
    <div>
        <h1>Войдите, чтобы продолжить</h1>
        <input type="text" bind:value={username} placeholder="Введите ваше имя">
        <button on:click={login}>Войти</button>
    </div>
{/if}





