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
            overflow: hidden;
        }
        iframe {
            position: fixed;
            top: 50%;
            left: 50%;
            width: 250%;
            height: 250%;
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
            border: none; /* Rimuove il bordo */
            border-radius: 10px;
            margin-top: 20px;
            color: white !important; 
        }        
        #loveMessageModal {
            font-size: 1.5em;
            margin-top: 10px;
            color: white !important; 
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
        }
    </style>
</head>
<body>
    <iframe src="https://player.vimeo.com/video/898542498?autoplay=1&loop=1&background=1" width="640" height="360" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>
    <div id="overlay">
        <img id="modal" src="https://i.ibb.co/hc4m71J/gatto-malessere.png" alt="Immagine">
        <div id="loveMessageModal">CE FACI SANDULE, FUMEZI SUB PLOAIE?:))</div>
    </div>
    <div id="loveMessage" onclick="mostraFoto()">
        ᴀᴘʀɪ ɪʟ ᴍɪᴏ ᴄᴜᴏʀɪᴄɪɴᴏ 
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




