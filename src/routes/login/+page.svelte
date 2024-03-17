<!-- Page.svelte -->
<script>
    import { Route } from 'svelte-routing';
    import Login from './Login.svelte';
    import Register from './Register.svelte';
</script>

<div>
    <Route path="/login" component={Login} />
    <Route path="/register" component={Register} />
</div>
