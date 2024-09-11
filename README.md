<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Feliz Cumpleaños Amor</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #f7d1e2;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            overflow: hidden;
        }

        .container {
            background-color: #ffffff;
            border-radius: 20px;
            box-shadow: 0px 4px 15px rgba(0, 0, 0, 0.1);
            text-align: center;
            padding: 40px;
            max-width: 600px;
        }

        h1 {
            color: #e91e63;
            font-size: 3rem;
        }

        h2 {
            color: #3f51b5;
            font-size: 2rem;
        }

        p {
            font-size: 1.2rem;
            color: #440c46;
        }

        .message {
            background-color: #f1f1f1;
            padding: 15px;
            border-radius: 10px;
            margin: 20px 0;
        }

        .button {
            background-color: #e91e63;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            font-size: 1.1rem;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }

        .button:hover {
            background-color: #d81b60;
        }

        /* Estilos para los botones de la ventana emergente */
        #popup {
            display: none;
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background-color: white;
            border: 2px solid #e91e63;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0px 4px 15px rgba(0, 0, 0, 0.1);
            z-index: 10;
        }

        #popup p {
            font-size: 1.2rem;
        }

        #yesBtn, #noBtn {
            background-color: #e91e63;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1rem;
            margin: 10px;
        }

        #yesBtn:hover, #noBtn:hover {
            background-color: #d81b60;
        }

        /* Estilo del globo */
        .balloon {
            position: fixed;
            top: 20px;
            right: 20px;
            width: 60px;
            height: 100px;
            background-color: #f06292;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            box-shadow: 0px 4px 15px rgba(0, 0, 0, 0.1);
            cursor: pointer;
            transition: transform 0.3s ease;
        }

        .balloon:hover {
            transform: scale(1.1);
        }

        .balloon-btn {
            background-color: #fff;
            border: none;
            padding: 10px;
            border-radius: 5px;
            font-size: 0.8rem;
            cursor: pointer;
        }

        .balloon-btn:hover {
            background-color: #ffebee;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>¡Feliz Cumpleaños, Carita de Cereal!</h1>
        <h2>Sandi 🍓</h2>
        <div class="message">
            <p>Niña hermosa, FELIZ CUMPLE, sabes que te amo mi amor y de todas las personas que conozco, eres la unica que me hace parar, el corazón obvio <3</p>
            <p>Por eso, TE AMO MUCHO </p>
        </div>
        <button class="button" onclick="showPopup()">Presiona aquí si me amas</button>
    </div>

    <!-- Globo interactivo -->
    <div class="balloon" onclick="burstBalloon()">
        <button class="balloon-btn">Presiona aquí</button>
    </div>

    <!-- Popup con los botones Sí y No -->
    <div id="popup">
        <p>PRECIONA 'SI' SI ME AMAS</p>
        <button id="yesBtn" onclick="loveConfirmed()">Sí</button>
        <button id="noBtn" onmouseover="moveNoButton()">No</button>
    </div>

    <!-- Script para confeti -->
    <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.5.1/dist/confetti.browser.min.js"></script>

    <script>
        // Función para mostrar la ventana emergente
        function showPopup() {
            document.getElementById('popup').style.display = 'block';
        }

        // Función para mover el botón "No"
        function moveNoButton() {
            const noBtn = document.getElementById('noBtn');
            const randomX = Math.floor(Math.random() * (window.innerWidth - noBtn.clientWidth));
            const randomY = Math.floor(Math.random() * (window.innerHeight - noBtn.clientHeight));
            noBtn.style.position = "absolute";
            noBtn.style.left = randomX + "px";
            noBtn.style.top = randomY + "px";
        }

        // Función cuando se presiona "Sí"
        function loveConfirmed() {
            alert("Sabía que me amabas ❤️");
            alert("By: Alex <3");
            document.getElementById('popup').style.display = 'none';
        }

        // Función para reventar el globo y lanzar confeti
        function burstBalloon() {
            confetti({
                particleCount: 100,
                spread: 70,
                origin: { y: 0.6 }
            });
            alert("¡Sorpresa! 🎉");
        }
    </script>
</body>
</html>
