<!DOCTYPE html>
<html lang="es" id="Tauros" class>

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Registro de Usuario</title>
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

        #saveButton {
            background-color: #108b44; /* Verde */
            color: #ffffff;
            padding: 12px 24px;
            font-size: 16px;
            cursor: pointer;
            border: none;
            border-radius: 4px;
            margin-right: 10px;
        }

        #redirectButton {
            background-color: #ff0000; /* Rojo */
            color: #ffffff;
            padding: 12px 24px;
            font-size: 16px;
            cursor: pointer;
            border: none;
            border-radius: 4px;
            margin-right: 10px;
        }

        #blueButton {
            background-color: #5758bb; /* Azul */
            color: #ffffff;
            padding: 12px 24px;
            font-size: 16px;
            cursor: pointer;
            border: none;
            border-radius: 4px;
            margin-right: 10px;
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

        .image-container {
            display: flex;
            justify-content: space-between;
            margin-top: 20px;
        }

        .image-container img {
            max-width: 48%;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        #qrCode {
            max-width: 100%;
            margin-top: 20px;
        }
    </style>
</head>

<body>

    <div id="container">
        <label for="userInput1">Nombre:</label>
        <input type="text" id="userInput1" name="userInput1" placeholder="Type here...">

        <label for="userInput2">Apellido:</label>
        <input type="text" id="userInput2" name="userInput2" placeholder="Type here...">

        <label for="userInput4">Clave:</label>
        <input type="text" id="userInput4" name="userInput4" placeholder="Type here...">

        <label for="userInput3">Informacion:</label>
        <!-- Cambiado a un menú desplegable (select) -->
        <select id="userInput3" name="userInput3" class="js-example-basic-single">
            <option value="Registro">Registro</option>
            <option value="Solicitud">Solicitud</option>
            <option value="Verificar">Verificar</option>
            <!-- Agrega más opciones según sea necesario -->
        </select>

        <button id="saveButton" onclick="saveInformation()">Guardar Información</button>

        <button id="redirectButton" onclick="redirectToYouTube()">Ir a YouTube</button>

        <!-- Nuevo botón azul -->
        <button id="blueButton" onclick="redirectToGoogle()">Ir a Facebook</button>

        <div id="result"></div>

        <div id="author">Documento por Jhon Pérez</div>

        <!-- Contenedor para imágenes -->
        <div class="image-container">
            <!-- Reemplaza 'URL_DE_LA_IMAGEN_1' con la URL real de tu primera imagen en línea -->
            <img src="manito.JPG" alt="Imagen 1">
            
            <!-- Reemplaza 'URL_DE_LA_IMAGEN_2' con la URL real de tu segunda imagen en línea -->
            <img src="scaneame.png" alt="Imagen 2">
        </div>

        <!-- Contenedor para el código QR -->
        <div id="qrCode"></div>
    </div>

    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/select2/4.0.13/js/select2.min.js"></script>

    <script>
        // Inicializar Select2 en el elemento select
        $(document).ready(function() {
            $('.js-example-basic-single').select2();
        });

        function saveInformation() {
            var userInput1 = document.getElementById("userInput1").value;
            var userInput2 = document.getElementById("userInput2").value;
            var userInput4 = document.getElementById("userInput4").value;
            var userInput3 = document.getElementById("userInput3").value;

            // Verificar si los campos están vacíos
            if (userInput1.trim() === '' || userInput2.trim() === '' || userInput4.trim() === '' || userInput3.trim() === '') {
                alert("Por favor, complete todos los campos.");
                return;
            }

            // Verificar si el nombre es "Luisa" o "luisa" y asignar un número específico
            var result;
            if (userInput1.toLowerCase() === 'Luisa'|| userInput1.toLowerCase() === 'luisa') {
                 result = "Oye porque no me has invitado a salir?, si tú lo quieres yo te invito...cuando me vas a regalar tú número? :)";
            } else {
                result = "Información Guardada: Nombre: " + userInput1 + ", Apellido: " + userInput2 + ", Clave: " + userInput4 + ", Informacion: " + userInput3;
            }
            
            // Muestra el resultado en el área designada
            document.getElementById("result").innerText = result;
        }

        function redirectToYouTube() {
            // Redirige a mi canal de YouTube
            window.location.href = "http://www.youtube.com/@jhonez801/featured";
        }

        function redirectToGoogle() {
            // Redirige a la página principal de Facebook
            window.location.href = "https://www.facebook.com/jhonez801?mibextid=ZbWKwL";
        }
    </script>

</body>
</html>




























