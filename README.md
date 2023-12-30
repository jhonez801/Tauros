
<html lang="es" id="Tauros" class>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Multiple Input Fields by Jhon Pérez</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/select2/4.0.13/css/select2.min.css">
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

        input, select {
            width: 100%;
            padding: 10px;
            font-size: 16px;
            margin-bottom: 16px;
            box-sizing: border-box;
        }

        #saveButton, #redirectButton {
            background-color: #5758bb;
            color: #ffffff;
            padding: 12px 24px;
            font-size: 16px;
            cursor: pointer;
            border: none;
            border-radius: 4px;
            margin-right: 10px;
        }

        #redirectButton {
            background-color: #4caf50; /* Color verde */
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
        <label for="userInput1">Nombre:</label>
        <input type="text" id="userInput1" name="userInput1" placeholder="Type here...">

        <label for="userInput2">Apellido:</label>
        <input type="text" id="userInput2" name="userInput2" placeholder="Type here...">

        <label for="userInput3">Informacion:</label>
        <!-- Cambiado a un multiselector (select con atributo multiple) -->
        <select id="userInput3" name="userInput3" multiple class="js-example-basic-multiple">
            <option value="opcion1">Opción 1</option>
            <option value="opcion2">Opción 2</option>
            <option value="opcion3">Opción 3</option>
            <!-- Agrega más opciones según sea necesario -->
        </select>

        <button id="saveButton" onclick="saveInformation()">Save Information</button>

        <button id="redirectButton" onclick="redirectToURL()">Ir a URL</button>

        <div id="result"></div>

        <div id="author">Document by Jhon Pérez</div>

        <!-- Reemplaza 'URL_DE_LA_IMAGEN' con la URL real de tu imagen en línea -->
        <img src="manito.JPG" alt="Placeholder Image">
    </div>

    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/select2/4.0.13/js/select2.min.js"></script>

    <script>
        // Inicializar Select2 en el elemento select
        $(document).ready(function() {
            $('.js-example-basic-multiple').select2();
        });

        function saveInformation() {
            var userInput1 = document.getElementById("userInput1").value;
            var userInput2 = document.getElementById("userInput2").value;
            var userInput3 = document.getElementById("userInput3").selectedOptions;

            var informationArray = [userInput1, userInput2];
            for (var i = 0; i < userInput3.length; i++) {
                informationArray.push(userInput3[i].value);
            }

            // Verificar si el nombre es "Luisa" o "luisa" y asignar un número específico
            var result;
            if (userInput1.toLowerCase() === 'Luisa'|| userInput1.toLowerCase() === 'luisa') {
                 result = "Oye porque no me has invitado a salir?, si tú lo quieres yo te invito...cuando me vas a regalar tú número? :)";
            } else {
                result = "Information Saved: " + informationArray.join(", ");
            }
            
            // Muestra el resultado en el área designada
            document.getElementById("result").innerText = result;
        }

        function redirectToURL() {
            // Reemplaza 'URL_DE_DESTINO' con la URL real a la que deseas redirigir
            var destinationURL = "http://www.youtube.com/@jhonez801/featured";
            window.location.href = destinationURL;
        }
    </script>

</body>
</html>


</body>
</html>


