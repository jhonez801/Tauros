<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Multiple Input Fields by Jhon Pérez</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            font-size: 16px;
            margin: 20px;
            background-color: #f4f4f4;
        }

        #container {
            max-width: 600px;
            margin: 0 auto;
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        label {
            display: block;
            margin-bottom: 8px;
            color: #333;
        }

        input {
            width: 100%;
            padding: 10px;
            font-size: 16px;
            margin-bottom: 16px;
            box-sizing: border-box;
        }

        #saveButton {
            background-color: #4caf50;
            color: #fff;
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
            border: none;
            border-radius: 4px;
        }

        #result {
            margin-top: 20px;
            font-weight: bold;
            color: #333;
        }

        #author {
            text-align: center;
            margin-top: 20px;
            font-style: italic;
            color: #666;
        }
    </style>
</head>
<body>

    <div id="container">
        <label for="userInput1">Enter Information 1:</label>
        <input type="text" id="userInput1" name="userInput1" placeholder="Type here...">

        <label for="userInput2">Enter Information 2:</label>
        <input type="text" id="userInput2" name="userInput2" placeholder="Type here...">

        <label for="userInput3">Enter Information 3:</label>
        <input type="text" id="userInput3" name="userInput3" placeholder="Type here...">

        <button id="saveButton" onclick="saveInformation()">Save Information</button>

        <div id="result"></div>

        <div id="author">Document by Jhon Pérez</div>

        <!-- Replace the placeholder URL with the actual URL of your image -->
        <img src="C:\Users\jhone\pagina web\manito.JPG" alt="Placeholder Image">
    </div>

    <script>
        function saveInformation() {
            var userInput1 = document.getElementById("userInput1").value;
            var userInput2 = document.getElementById("userInput2").value;
            var userInput3 = document.getElementById("userInput3").value;

            var informationArray = [userInput1, userInput2, userInput3];
            var result = "Information Saved: " + informationArray.join(", ");
            
            // Muestra el resultado en el área designada
            document.getElementById("result").innerText = result;
        }
    </script>

</body>
</html>

