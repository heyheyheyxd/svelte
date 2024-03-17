<div class="container">
    <a href="/about" class="xd">Обо мне</a>
    <slot />
</div>

<style>
    .container {
        margin: 50px auto;
        max-width: 800px;
        padding: 0 20px;
    }
    .xd {
        display: inline-block;
        padding: 10px 20px;
        background-color: #007bff;
        color: #fff;
        text-decoration: none;
        border-radius: 5px;
        transition: background-color 0.3s ease;
    }

    .xd:hover {
        background-color: #0056b3;
    }
</style>