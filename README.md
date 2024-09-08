<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Wähle eine Tür</title>
    <style>
        body {
            text-align: center;
            font-family: Arial, sans-serif;
        }
        .door {
            display: inline-block;
            margin: 20px;
            padding: 20px;
            width: 150px;
            height: 150px;
            background-color: #4CAF50;
            color: white;
            font-size: 20px;
            cursor: pointer;
            border-radius: 10px;
        }
        .door:hover {
            background-color: #45a049;
        }
        .amount {
            display: none;
            margin-top: 20px;
            font-size: 24px;
            font-weight: bold;
        }
    </style>
</head>
<body>

    <h1>Wähle eine Tür und finde deinen Sparbetrag!</h1>

    <div id="door1" class="door" onclick="revealAmount(1)">Tür 1</div>
    <div id="door2" class="door" onclick="revealAmount(2)">Tür 2</div>
    <div id="door3" class="door" onclick="revealAmount(3)">Tür 3</div>

    <div id="amount" class="amount"></div>

    <script>
        function revealAmount(door) {
            let amounts = {
                1: "5€ gespart!",
                2: "10€ gespart!",
                3: "15€ gespart!"
            };
            document.getElementById("amount").textContent = amounts[door];
            document.getElementById("amount").style.display = 'block';
        }
    </script>

</body>
</html>
