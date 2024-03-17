<!-- +Page.svelte -->
<script>
    let username = "";

    import Register from './Register.svelte';
</script>

<nav>
    <h3>{username || "Регистрация"}</h3>
</nav>

<Register />






