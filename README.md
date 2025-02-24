<!DOCTYPE html>
<html lang="uk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Віртуальний Монітор Трактора</title>
    <style>
        body {
            text-align: center;
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
        }
        .monitor {
            position: relative;
            width: 600px;
            height: 400px;
            margin: 50px auto;
            background: url('monitor-placeholder.jpg') no-repeat center;
            background-size: cover;
            border: 10px solid black;
            border-radius: 20px;
        }
        .button {
            position: absolute;
            width: 80px;
            height: 40px;
            background: red;
            color: white;
            border: none;
            cursor: pointer;
            font-weight: bold;
            border-radius: 5px;
        }
        .button:hover {
            background: darkred;
        }
        #screen {
            position: absolute;
            top: 50px;
            left: 50px;
            width: 500px;
            height: 300px;
            background: white;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
            font-weight: bold;
            color: black;
            border-radius: 10px;
        }
    </style>
</head>
<body>
    <h1>Віртуальний Монітор Трактора</h1>
    <div class="monitor">
        <div id="screen">Головний екран</div>
        <button class="button" style="top: 350px; left: 100px;" onclick="changeScreen('Карта полів')">Карта</button>
        <button class="button" style="top: 350px; left: 200px;" onclick="changeScreen('Густота посіву')">Посів</button>
        <button class="button" style="top: 350px; left: 300px;" onclick="changeScreen('Спостереження')">Обладнання</button>
    </div>
    <script>
        function changeScreen(text) {
            document.getElementById('screen').innerText = text;
        }
    </script>
</body>
</html>
