<!-- Page.svelte -->
<script>
    let username = "";

    function setUsername(value) {
        username = value;
    }
</script>

<nav>
    <h3>{username || "Регистрация"}</h3>
</nav>

<style>
    nav {
        margin-bottom: 20px;
    }
</style>









