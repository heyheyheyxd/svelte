<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Каталог - Heyheyhey Digital Store</title>
    <style>
    .background {
    background-color: #e0f3ff; /* Цвет фона, который вы хотите использовать */
}
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f0f0f0;
        }

        .container {
            max-width: 1200px;
            margin: 50px auto;
            padding: 20px;
            background-color: #fff;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        h1 {
            text-align: center;
            color: #333;
        }

        .catalog {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            margin-top: 30px;
        }

        .product {
            width: 250px;
            margin: 20px;
            padding: 20px;
            background-color: #f9f9f9;
            border-radius: 8px;
            box-shadow: 0 0 5px rgba(0, 0, 0, 0.1);
            text-align: center;
        }

        .product h2 {
            color: #007bff;
            margin-bottom: 10px;
        }

        .product img {
            max-width: 100%;
            border-radius: 8px;
        }

        .product p {
            color: #666;
            margin-bottom: 10px;
        }

        .product select {
            margin-top: 10px;
            padding: 8px;
            border-radius: 5px;
            border: 1px solid #ccc;
            width: 100%;
            box-sizing: border-box;
        }

        .product .price {
            margin-top: 10px;
            color: #007bff;
            font-weight: bold;
        }

        .product button {
            margin-top: 10px;
            padding: 10px 20px;
            background-color: #007bff;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }

        .product button:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body class="background">
    <div class="container">
        <h1>Каталог</h1>

        <div class="catalog">
            <div class="product">
                <h2>Roblox</h2>
                <p>Количество:</p>
                <select id="robloxSelect">
                    <option value="40" data-price="10">40</option>
                    <option value="80" data-price="15">80</option>
                    <option value="200" data-price="25">200</option>
                    <option value="400" data-price="40">400</option>
                </select>
                <div class="price" id="robloxPrice"></div>
                <button onclick="addToCart('Roblox', document.getElementById('robloxSelect').value)">Добавить в корзину</button>
            </div>

            <div class="product">
                <h2>Fortnite</h2>
                <p>Количество:</p>
                <select id="fortniteSelect">
                    <option value="1000" data-price="30">1000</option>
                    <option value="2800" data-price="50">2800</option>
                    <option value="5000" data-price="80">5000</option>
                    <option value="13500" data-price="120">13500</option>
                </select>
                <div class="price" id="fortnitePrice"></div>
                <button onclick="addToCart('Fortnite', document.getElementById('fortniteSelect').value)">Добавить в корзину</button>
            </div>

            <div class="product">
                <h2>Rocket League</h2>
                <p>Количество:</p>
                <select id="rocketLeagueSelect">
                    <option value="500" data-price="20">500</option>
                    <option value="1100" data-price="35">1100</option>
                    <option value="300" data-price="15">300</option>
                    <option value="6500" data-price="50">6500</option>
                </select>
                <div class="price" id="rocketLeaguePrice"></div>
                <button onclick="addToCart('Rocket League', document.getElementById('rocketLeagueSelect').value)">Добавить в корзину</button>
            </div>

            <div class="product">
                <h2>Brawl Stars</h2>
                <p>Количество:</p>
                <select id="brawlStarsSelect">
                    <option value="30" data-price="5">30</option>
                    <option value="80" data-price="10">80</option>
                    <option value="170" data-price="15">170</option>
                    <option value="360" data-price="25">360</option>
                    <option value="720" data-price="40">720</option>
                </select>
                <div class="price" id="brawlStarsPrice"></div>
                <button onclick="addToCart('Brawl Stars', document.getElementById('brawlStarsSelect').value)">Добавить в корзину</button>
            </div>
        </div>
    </div>

    <script>
        function updatePrice(selectId, priceId) {
            const select = document.getElementById(selectId);
            const price = document.getElementById(priceId);
            const selectedOption = select.options[select.selectedIndex];
            const selectedPrice = selectedOption.getAttribute('data-price');
            price.textContent = `Цена: $${selectedPrice}`;
        }

        const products = [
            { name: 'Roblox', image: 'roblox.jpg', options: [40, 80, 200, 400], prices: [10, 15, 25, 40] },
            { name: 'Fortnite', image: 'fortnite.jpg', options: [1000, 2800, 5000, 13500], prices: [30, 50, 80, 120] },
            { name: 'Rocket League', image: 'rocket-league.jpg', options: [500, 1100, 300, 6500], prices: [20, 35, 15, 50] },
            { name: 'Brawl Stars', image: 'brawl-stars.jpg', options: [30, 80, 170, 360, 720], prices: [5, 10, 15, 25, 40] }
        ];

        function addToCart(productName, quantity) {
            const product = products.find(p => p.name === productName);
            const priceIndex = product.options.indexOf(parseInt(quantity));
            const totalPrice = product.prices[priceIndex];
            alert(`Товар "${productName}" в количестве ${quantity} добавлен в корзину. Общая сумма: $${totalPrice}`);
        }

        window.onload = function () {
            updatePrice('robloxSelect', 'robloxPrice');
            updatePrice('fortniteSelect', 'fortnitePrice');
            updatePrice('rocketLeagueSelect', 'rocketLeaguePrice');
            updatePrice('brawlStarsSelect', 'brawlStarsPrice');
        };
    </script>
</body>
</html>


