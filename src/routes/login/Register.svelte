<!-- Register.svelte -->
<script>
    export let setUsername;

    let username = "";

    function handleUsernameChange(event) {
        username = event.target.value;
    }

    function handleRegister() {
        setUsername(username);
    }
</script>

<label>
    Ник:
    <input type="text" bind:value={username} on:input={handleUsernameChange} required>
</label>

<button on:click={handleRegister}>Зарегистрироваться</button>




