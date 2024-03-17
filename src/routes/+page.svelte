<nav>
    <div class="nav-container">
        <a href="/" class="nav-logo" title="Back to home">Heyheyhey shop</a>
    <div class="nav-links">
      <a href="/about" class="link">Обо мне</a>
      <a href="/blog" class="link">Каталог</a>
      <a href="/contact" class="link">Контакты</a>
    </div>
    </div>
</nav>

<div class="container">
    <!--Pages will be injected below-->
    <slot></slot>
</div>

<style>
    .container{
        max-width: 1400px;
        margin: 50px auto;
    }
</style>