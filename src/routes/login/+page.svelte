<!-- Page.svelte -->
<script>
    import Register from './Register.svelte';
    let username = "";

    function setUsername(value) {
        username = value;
    }
</script>

<nav>
    <h3>{username ? `Привет, ${username}!` : "Введите свой ник"}</h3>
</nav>

<Register setUsername={setUsername} />

<style>
    nav {
        margin-bottom: 20px;
    }
</style>










