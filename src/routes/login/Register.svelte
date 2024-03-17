<!-- Register.svelte -->
<script>
    import GoogleLogin from 'svelte-google-login';

    async function handleLogin(user) {
        console.log(user);
        // В этой функции вы можете отправить данные пользователя на сервер для регистрации
    }
</script>

<h1>Регистрация</h1>

<p>Зарегистрируйтесь с помощью Google:</p>
<GoogleLogin
    clientId="YOUR_CLIENT_ID"
    onSuccess={handleLogin}
    onFailure={(error) => console.log(error)}
>
    <button>Войти с Google</button>
</GoogleLogin>

