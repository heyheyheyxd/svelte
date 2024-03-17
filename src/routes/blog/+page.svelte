<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Каталог - Heyheyhey Digital Store</title>
    <style>
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
        }

        .product p {
            color: #666;
        }

        .product select {
            margin-top: 10px;
            padding: 8px;
            border-radius: 5px;
            border: 1px solid #ccc;
            width: 100%;
            box-sizing: border-box;
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
<body>
    <div class="container">
        <h1>Каталог</h1>

        <div class="catalog">
            <div class="product">
                <h2>Roblox</h2>
                <p>Цена:</p>
                <select id="robloxSelect">
                    <option value="40">40</option>
                    <option value="80">80</option>
                    <option value="200">200</option>
                    <option value="400">400</option>
                </select>
                <button onclick="addToCart('Roblox', document.getElementById('robloxSelect').value)">Добавить в корзину</button>
            </div>

            <div class="product">
                <h2>Fortnite</h2>
                <p>Цена:</p>
                <select id="fortniteSelect">
                    <option value="1000">1000</option>
                    <option value="2800">2800</option>
                    <option value="5000">5000</option>
                    <option value="13500">13500</option>
                </select>
                <button onclick="addToCart('Fortnite', document.getElementById('fortniteSelect').value)">Добавить в корзину</button>
            </div>

            <div class="product">
                <h2>Rocket League</h2>
                <p>Цена:</p>
                <select id="rocketLeagueSelect">
                    <option value="500">500</option>
                    <option value="1100">1100</option>
                    <option value="300">300</option>
                    <option value="6500">6500</option>
                </select>
                <button onclick="addToCart('Rocket League', document.getElementById('rocketLeagueSelect').value)">Добавить в корзину</button>
            </div>

            <div class="product">
                <h2>Brawl Stars</h2>
                <p>Цена:</p>
                <select id="brawlStarsSelect">
                    <option value="30">30</option>
                    <option value="80">80</option>
                    <option value="170">170</option>
                    <option value="360">360</option>
                    <option value="720">720</option>
                </select>
                <button onclick="addToCart('Brawl Stars', document.getElementById('brawlStarsSelect').value)">Добавить в корзину</button>
            </div>
        </div>
    </div>

    <script>
        function addToCart(productName, price) {
            alert('Товар ' + productName + ' ценой ' + price + ' успешно добавлен в корзину!');
        }
    </script>
</body>
</html>
