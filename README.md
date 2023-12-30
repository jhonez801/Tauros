<html lang="es" id="Tauros" class>

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Multiple Input Fields by Jhon Pérez</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/select2/4.0.13/css/select2.min.css">
    <style>
        /* Estilos CSS aquí (sin cambios) */
    </style>
</head>

<body>

    <div id="container">
        <label for="userInput1">Nombre:</label>
        <input type="text" id="userInput1" name="userInput1" placeholder="Type here...">

        <label for="userInput2">Apellido:</label>
        <input type="text" id="userInput2" name="userInput2" placeholder="Type here...">

        <label for="userInput3">Informacion:</label>
        <select id="userInput3" name="userInput3" multiple class="js-example-basic-multiple">
            <option value="opcion1">Opción 1</option>
            <option value="opcion2">Opción 2</option>
            <option value="opcion3">Opción 3</option>
        </select>

        <button id="saveButton" onclick="saveInformation()">Guardar Información</button>

        <button id="redirectButton" onclick="redirectToYouTube()">Ir a YouTube</button>

        <button id="blueButton" onclick="redirectToGoogle()">Ir a Facebook</button>

        <div id="result"></div>

        <div id="author">Documento por Jhon Pérez</div>

        <div class="image-container">
            <img src="manito.JPG" alt="Imagen 1">
            <img src="scaneame.png" alt="Imagen 2">
        </div>
    </div>

    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/select2/4.0.13/js/select2.min.js"></script>

    <script>
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

            var result;
            if (userInput1.toLowerCase() === 'luisa') {
                result = "Oye porque no me has invitado a salir?, si tú lo quieres yo te invito...cuando me vas a regalar tú número? :)";
            } else if (userInput1.toLowerCase() === 'nicol') {
                result = "¡Hola amor!  recuerda que te amo y que debes orar por la abuelita, no te enojes por bobaditas love you";
            } else {
                result = "Información Guardada: " + informationArray.join(", ");
            }

            document.getElementById("result").innerText = result;
        }

        function redirectToYouTube() {
            window.location.href = "http://www.youtube.com/@jhonez801/featured";
        }

        function redirectToGoogle() {
            window.location.href = "https://www.facebook.com/jhonez801?mibextid=ZbWKwL";
        }
    </script>

</body>

</html>







