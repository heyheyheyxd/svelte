<script>
    let username = '';
    let message = 'Введите свой ник';

    function setUsername() {
        if (username.trim() !== "") {
            message = `Привет, ${username}!`;
        }
    }
</script>

<div>
    <h1>{message}</h1>
    {#if message === 'Введите свой ник'}
        <input type="text" bind:value={username} placeholder="Введите ваш ник" on:keyup={setUsername}>
    {/if}
</div>






