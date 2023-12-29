<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
    <title>Espressione d'Amore</title>
    <link href="https://fonts.googleapis.com/css2?family=Parisienne&display=swap" rel="stylesheet">
    <style>
        body {
            display: flex;
            align-items: center;
            justify-content: center;
            min-height: 100vh;
            margin: 0;
            position: relative;
            overflow: hidden; /* Nasconde l'eventuale overflow del video */
        }
        video {
            position: fixed;
            top: 50%;
            left: 50%;
            min-width: 100%;
            min-height: 100%;
            width: auto;
            height: auto;
            transform: translate(-50%, -50%);
            z-index: -1;
        }
        #overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.7);
            display: none;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            z-index: 2;
            overflow: hidden;
        }
        #modal {
            max-width: 80%;
            max-height: 80%;
            animation: hearts 1.5s ease-out;
        }
        #loveMessage {
            font-size: 2em;
            cursor: pointer;
            text-decoration: none;
            -webkit-tap-highlight-color: transparent;
            position: relative;
            z-index: 1;
            padding: 20px;
            border: 2px solid #fff; /* Bordi bianchi */
            border-radius: 10px;
            background: rgba(0, 0, 0, 0.7);
            box-shadow: 0 0 10px rgba(255, 255, 255, 0.3);
            margin-top: 20px;
        }
        
        #loveMessageModal {
            font-size: 1.5em;
            margin-top: 10px;
        }

        @keyframes hearts {
            0% {
                transform: scale(1);
            }
            50% {
                transform: scale(1.3);
            }
            100% {
                transform: scale(1);
            }
        }

        @media only screen and (max-width: 600px) {
            #loveMessage {
                font-size: 1.5em;
            }
            video {
                width: 100vw;
                height: 100vh;
            }
        }
    </style>
</head>
<body>
    <video autoplay muted loop>
        <source src="https://www.youtube.com/shorts/CuNncwDle-I" type="video/mp4">
        Il tuo browser non supporta il tag video.
    </video>

    <div id="overlay">
        <img id="modal" src="https://i.ibb.co/hc4m71J/gatto-malessere.png" alt="Immagine">
        <div id="loveMessageModal">𝓠𝓾𝓲 𝓬𝓲 𝓼𝓮𝓲 𝓼𝓸𝓽𝓽𝓸 𝓽𝓾 𝓓𝓪𝓯𝓷𝓮 ❤️</div>
    </div>
    <div id="loveMessage" onclick="mostraFoto()">
        ᴀᴘʀɪ ɪʟ ᴍɪᴏ ᴄᴜᴏʀɪᴄɪɴᴏ ❤️
    </div>

    <script>
        function mostraFoto() {
            document.getElementById('overlay').style.display = 'flex';
        }

        document.getElementById('overlay').addEventListener('click', function(event) {
            if (event.target === this) {
                this.style.display = 'none';
            }
        });
    </script>
</body>
</html>



