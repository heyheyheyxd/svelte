<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Кинотеатр Heyheyhey</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f0f0f0;
            background-image: url('https://top-fon.com/uploads/posts/2023-01/1674815996_top-fon-com-p-kinoteatr-fon-dlya-prezentatsii-85.jpg');
        }
        .container {
            max-width: 1200px;
            margin: 20px auto;
            padding: 0; 
        }
        h1 {
            text-align: center;
            color: #ff0000;
        }
        .catalog {
            display: grid; /* Используем grid layout */
            grid-template-columns: repeat(2, 1fr); /* Два блока в одну строку */
            gap: 20px; /* Расстояние между блоками */
            justify-content: center;
            margin-top: 30px;
        }
        .product {
            width: 100%;
            padding: 20px;
            background-color: #000000;
            color: #ffffff;
            border-radius: 8px;
            box-shadow: 0 0 5px rgba(0, 0, 0, 0.1);
            text-align: center;
            position: relative;
            opacity: 0; /* Исходно скрываем блоки */
            animation: fadeIn 1s ease-in-out forwards; /* Анимация появления */
        }
        .product img {
            width: 100%;
            height: auto;
            max-width: 500px;
            max-height: 300px;
            border-radius: 8px;
            margin-bottom: 10px;
        }
        .product h2 {
            color: #ff0000;
            margin-bottom: 10px;
        }
        .product p {
            margin-bottom: 10px;
        }
        .product select {
            margin-top: 10px;
            padding: 8px;
            border-radius: 5px;
            border: 1px solid #ffffff;
            width: 100%;
            box-sizing: border-box;
            color: #000000;
            background-color: #ffffff;
        }
        .product .price {
            margin-top: 10px;
            color: #ff0000;
            font-weight: bold;
        }
        .product button {
            margin-top: 10px;
            padding: 10px 20px;
            background-color: #ff0000;
            color: #ffffff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }
        .product button:hover {
            background-color: #8b0000;
        }

        @keyframes fadeIn {
            from {
                opacity: 0; /* Начальная непрозрачность */
            }
            to {
                opacity: 1; /* Конечная непрозрачность */
            }
        }
    </style>
</head>
<body class="background">
    <div class="container">
        <h1>Каталог фильмов</h1>
        <div id="cart-items-count">Товаров в корзине: 0</div>
        <div class="catalog" id="catalog"></div>
    </div>

    <script>
        const products = [
            { name: 'Пила', image: 'https://www.proficinema.com/upload/iblock/cf0/cf0a6ea1e13c0c42a2bc2f0cb053ce94.jpg', options: [1, 2, 3, 4], parts: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10], prices: [10, 20, 30, 40] },
            { name: 'Бегущий в лабиринте', image: 'https://klubkrik.ru/wp-content/uploads/2015/04/575613.jpg', options: [1, 2, 3, 4], parts: [1, 2, 3], prices: [7, 15, 22, 29] },
            { name: 'Такси', image: 'https://wallpapercosmos.com/w/full/c/b/a/352680-1920x1080-desktop-full-hd-taxi-movie-wallpaper.jpg', options: [1, 2, 3, 4], parts: [1, 2, 3,4], prices: [8, 16, 24, 32] },
            { name: 'Форсаж', image: 'https://sun9-35.userapi.com/hCWfxGwcuIRvmfKQXwr9OZNN4mu4ERi538DsZg/QlzDt8Eazmk.jpg', options: [1, 2, 3, 4], parts: [1, 2, 3,4,5,6,7,8,9,10], prices: [9, 18, 27, 36] }
        ];

        function createProductCard(product) {
            const card = document.createElement('div');
            card.className = 'product';

            const image = document.createElement('img');
            image.src = product.image;
            image.alt = product.name;
            card.appendChild(image);

            const title = document.createElement('h2');
            title.textContent = product.name;
            card.appendChild(title);

            const paragraph = document.createElement('p');
            paragraph.textContent = 'Количество билетов:';
            card.appendChild(paragraph);

            const select = document.createElement('select');
            product.options.forEach((option, index) => {
                const optionElement = document.createElement('option');
                optionElement.value = option;
                optionElement.textContent = option;
                optionElement.setAttribute('data-price', product.prices[index]);
                select.appendChild(optionElement);
            });
            card.appendChild(select);

            const partParagraph = document.createElement('p');
            partParagraph.textContent = 'Выберите часть фильма:';
            card.appendChild(partParagraph);

            const partSelect = document.createElement('select');
            product.parts.forEach(part => {
                const partOption = document.createElement('option');
                partOption.value = part;
                partOption.textContent = `Часть ${part}`;
                partSelect.appendChild(partOption);
            });
            card.appendChild(partSelect);

const timeParagraph = document.createElement('p');
timeParagraph.textContent = 'Выберите время сеанса:';
card.appendChild(timeParagraph);

const timeSelect = document.createElement('select');
const times = ['10:00', '13:00', '16:00', '19:00'];
times.forEach(time => {
    const timeOption = document.createElement('option');
    timeOption.value = time;
    timeOption.textContent = time;
    timeSelect.appendChild(timeOption);
});
card.appendChild(timeSelect);
const price = document.createElement('div');
price.className = 'price';
card.appendChild(price);

select.addEventListener('change', function () {
    const selectedOption = this.options[this.selectedIndex];
    const selectedPrice = selectedOption.getAttribute('data-price');
    price.textContent = `Цена: $${selectedPrice}`;
});
const button = document.createElement('button');
button.textContent = 'Забронировать';
button.addEventListener('click', function () {
    const selectedQuantity = select.value;
    const selectedPart = partSelect.value; // Получаем выбранную часть фильма
    const selectedTime = timeSelect.value;
    const selectedPrice = select.options[select.selectedIndex].getAttribute('data-price');
    let message = `Фильм "${product.name}". Часть ${selectedPart}.`;

    message += ` Количество билетов: ${selectedQuantity}. Время сеанса ${selectedTime}. Общая сумма: $${selectedPrice}.`;
    alert(message);
});
card.appendChild(button);

return card;
}

const catalog = document.getElementById('catalog');
products.forEach(product => {
catalog.appendChild(createProductCard(product));
});


</script>
</body>
</html>




           












           

