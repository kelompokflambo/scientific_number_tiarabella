<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Scientific Number Input</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">
    <style>
        body {
            font-family: 'Roboto', sans-serif;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #878f87;
        }
        .container {
            text-align: center;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
            background-color: #fefcfc;
            max-width: 400px;
            width: 90%;
        }
        input[type="text"] {
            width: calc(100% - 22px);
            padding: 10px;
            font-size: 16px;
            border: 1px solid #c7c9cb;
            border-radius: 5px;
            margin-bottom: 10px;
            margin-right: 5px;
            display: inline-block;
            box-sizing: border-box;
        }
        button {
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
            background-color: #007bff;
            color: #ffffff;
            border: none;
            border-radius: 5px;
            transition: background-color 0.3s;
        }
        button:hover {
            background-color: #0056b3;
        }
        #result {
            margin-top: 20px;
            font-size: 18px;
        }
        #name-container {
            position: absolute;
            top: 20px;
            left: 20px;
            background-color: #faf9f9;
            padding: 10px;
            border-radius: 5px;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
        }
        #name-container h3 {
            margin: 5px 0;
        }
        h1 {
            color: #0e0e0e;
        }
    </style>
</head>
<body>
    <div id="name-container">
        <h3>Major : Information Systems</h3>
        <h3>Name : Tiarabella Kalaena </h3>
        <h3>NIM : 221011060023</h3>
    </div>
    <div class="container">
        <h1 style="font-weight: 700;">Scientific Number Input</h1>
        <h2>Input Scientific Number</h2>
        <input type="text" id="scientificNumber" placeholder="Enter scientific number...">
        <button onclick="acceptNumber()"><i class="fas fa-check"></i> Accept</button>
        <div id="result"></div>
    </div>

    <script>
        function acceptNumber() {
            var scientificNumberInput = document.getElementById("scientificNumber").value;
            var parsedNumber = parseFloat(scientificNumberInput);
            if (!isNaN(parsedNumber)) {
                document.getElementById("result").innerHTML = `<span style="color: #28a745;"><i class="fas fa-check-circle"></i> Accepted Number: ${parsedNumber}</span>`;
            } else {
                document.getElementById("result").innerHTML = `<span style="color: #dc3545;"><i class="fas fa-times-circle"></i> Invalid input. Please enter a valid scientific number.</span>`;
            }
        }
    </script>
</body>
</html>
