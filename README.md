<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pagina Interattiva</title>
    <style>
        body {
            display: flex;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
            background-image: url('https://i.pinimg.com/564x/60/43/50/60435052d20652348142bd9b5acc0aee.jpg');
            background-size: cover;
            background-position: center;
            color: white;
            font-family: Arial, sans-serif;
        }
        #initialMessage {
            font-size: 2em;
            cursor: pointer;
            text-decoration:
        }
        #hiddenMessage {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            justify-content: center;
            align-items: center;
            flex-direction: column;
            text-align: center;
        }
        #hiddenMessage img {
            width: 80%;
            max-width: 400px; /* Limita la larghezza dell'immagine su dispositivi più piccoli */
            border-radius: 10px;
            margin-bottom: 20px;
        }
        #closeButton {
            cursor: pointer;
            color: #ffffff;
            font-size: 1.5em;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div id="initialMessage" onclick="mostraMessaggio()">🐷𝔱𝔬𝔠𝔠𝔞𝔪𝔦🐷</div>

    <div id="hiddenMessage">
        <img src=https://media1.tenor.com/m/B0hY0xt5NUgAAAAC/bust-kurtangle.gif alt="Immagine Grande">
        <p>Dafne davanti al Papi che fa l'elicottero💦</p>
        <div id="closeButton" onclick="chiudiMessaggio()"></div>
    </div>

    <script>
        function mostraMessaggio() {
            document.getElementById('hiddenMessage').style.display = 'flex';
        }

        function chiudiMessaggio() {
            document.getElementById('hiddenMessage').style.display = 'none';
        }
    </script>
</body>
</html>

