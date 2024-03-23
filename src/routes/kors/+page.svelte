<body>
<script>   
    async function handleSubmit(event) {
        event.preventDefault();
        const formData = new FormData(event.target);
        const name = formData.get('name');
        const email = formData.get('email');
        const message = formData.get('message');
        try {
            
            console.log('Имя:', name);
            console.log('Email:', email);
            console.log('Отзыв:', message);
            
            event.target.reset();
        } catch (error) {
            console.error('Ошибка:', error);
        }
    }
</script>

<main>
    <section>
        <h1>Отзывы наших посетителей</h1>
        <p>Мы ценим каждого посетителя и всегда открыты к вашим предложениям и замечаниям!</p>
        
        <form on:submit="{handleSubmit}">
            <label for="name">Ваше имя:</label>
            <input type="text" id="name" name="name" required>
            
            <label for="email">Ваш email:</label>
            <input type="email" id="email" name="email" required>
            
            <label for="message">Ваш отзыв:</label>
            <textarea id="message" name="message" rows="4" required></textarea>
            
            <button type="submit">Отправить</button>
        </form>
    </section>
    
</main>

<style>
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f0f0f0;
    background-image: url('https://top-fon.com/uploads/posts/2023-01/1674815996_top-fon-com-p-kinoteatr-fon-dlya-prezentatsii-85.jpg');
}

main {
    background-color: rgba(0, 0, 0, 0.7); 
    box-shadow: 0 0 20px rgba(255, 255, 255, 0.1);
    color: #fff; 
    padding: 20px;
    max-width: 700px; /* Максимальная ширина блока */
    margin: 20px auto; /* Центрирование блока */
}
p{
    color: #fff;
}
h1 {
    color: #fff; 
}

label {
    color: #fff; 
}

input[type="text"],
input[type="email"],
textarea {
    background-color: #fff; 
    color: #333; 
    border: 1px solid #ccc; 
    padding: 8px;
    margin-bottom: 10px;
    width: 100%;
}

button[type="submit"] {
        background-color: #ff0000; 
        color: #000; 
        padding: 10px 20px;
        border: none;
        cursor: pointer;
        transition: background-color 0.3s ease;
    }

    button[type="submit"]:hover {
        background-color: #a30000; 
    }

</style>
</body>

