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
            background-image: url('https://i.pinimg.com/564x/30/d7/b6/30d7b605c376472aa07d4af33a40afb2.jpg');
            background-size: cover;
            background-position: center;
            color: #fff; /* Testo bianco */
            font-family: 'Parisienne', cursive; /* Font più stilizzato */
            text-align: center;
        }
        #overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.7); /* Sovrimpressione nera con opacità */
            display: none;
            flex-direction: column; /* Allineamento dei figli in colonna */
            justify-content: center;
            align-items: center;
            z-index: 2;
            overflow: hidden; /* Nasconde i cuori che esplodono oltre i bordi dell'overlay */
        }
        #modal {
            max-width: 80%;
            max-height: 80%;
            animation: hearts 1.5s ease-out; /* Aggiunta animazione cuori */
        }
        #loveMessage {
            font-size: 2em;
            cursor: pointer;
            text-decoration: none; /* Rimuovi l'underline */
            -webkit-tap-highlight-color: transparent; /* Impedisce il colore di evidenziazione durante il tocco su iOS */
            position: relative;
            z-index: 1;
            padding: 20px;
            border: none; /* Rimuove il bordo */
            border-radius: 10px;
            background: rgba(0, 0, 0, 0.7); /* Sfondo nero traslucido */
            box-shadow: 0 0 10px rgba(255, 255, 255, 0.3); /* Ombra */
            margin-top: 20px; /* Aggiunto margine sopra il messaggio */
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

        /* Stile aggiunto per dispositivi mobili */
        @media only screen and (max-width: 600px) {
            #loveMessage {
                font-size: 1.5em;
            }
        }
    </style>
</head>
<body>
    <div id="overlay">
        <img id="modal" src="https://i.ibb.co/hc4m71J/gatto-malessere.png" alt="Immagine">
        <div id="loveMessageModal">𝓠𝓾𝓲 𝓬𝓲 𝓼𝓮𝓲 𝓼𝓸𝓵𝓸 𝓽𝓾 𝓓𝓪𝓯𝓷𝓮 ❤️</div>
    </div>
    <div id="loveMessage" onclick="mostraFoto()">
        ᴀᴘʀɪ ɪʟ ᴍɪᴏ ᴄᴜᴏʀɪᴄɪɴᴏ ❤️
    </div>

    <script>
        function mostraFoto() {
            document.getElementById('overlay').style.display = 'flex';
        }

        // Chiudi la finestra modale cliccando al di fuori dell'immagine
        document.getElementById('overlay').addEventListener('click', function(event) {
            if (event.target === this) {
                this.style.display = 'none';
            }
        });
    </script>
</body>
</html>

