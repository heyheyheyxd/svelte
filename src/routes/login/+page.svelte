<!-- +Page.svelte -->
<script>
    import { Router, Route } from 'svelte-routing';
    import Login from './Login.svelte';
    import Register from './Register.svelte';
</script>

<nav>
    <a href="/login">Войти</a>
    <a href="/register">Регистрация</a>
</nav>

<Router>
    <Route path="/login" component={Login} />
    <Route path="/register" component={Register} />
</Router>

<style>
    nav {
        margin-bottom: 20px;
    }

    nav a {
        margin-right: 10px;
        text-decoration: none;
    }
</style>




