<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Regalo para mi pancito</title>
    <style>
        body {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #f0e4d7;
            font-family: 'Arial', sans-serif;
        }
        h1 {
            font-size: 2.5em;
            color: #ff69b4;
            text-align: center;
            padding: 0 20px;
        }
        #tulipanes {
            display: none;
            margin: 20px 0;
            flex-wrap: wrap;
            justify-content: center;
        }
        .tulipan {
            width: 70px;
            height: 100px;
            background-color: pink;
            clip-path: polygon(50% 0%, 0% 100%, 100% 100%);
            margin: 10px;
            display: inline-block;
        }
        button {
            background-color: #ff69b4;
            color: white;
            border: none;
            padding: 10px 20px;
            font-size: 1.2em;
            cursor: pointer;
            border-radius: 10px;
        }
        #mensaje {
            font-size: 1.8em;
            color: #ff69b4;
            margin-top: 20px;
            display: none;
        }
        @media (max-width: 768px) {
            h1 {
                font-size: 2em;
            }
            button {
                font-size: 1em;
                padding: 10px 20px;
            }
            .tulipan {
                width: 60px;
                height: 90px;
            }
            #mensaje {
                font-size: 1.5em;
            }
        }
        @media (max-width: 480px) {
            h1 {
                font-size: 1.8em;
            }
            button {
                font-size: 0.9em;
                padding: 8px 15px;
            }
            .tulipan {
                width: 50px;
                height: 80px;
            }
            #mensaje {
                font-size: 1.2em;
            }
        }
    </style>
</head>
<body>

    <h1>Regalo para mi pancito</h1>
    <button onclick="mostrarTulipanes()">Mirar el regalo de tu pancito</button>

    <div id="tulipanes"></div>
    <div id="mensaje">Te amo</div>

    <script>
        function mostrarTulipanes() {
            const tulipanesDiv = document.getElementById("tulipanes");
            tulipanesDiv.style.display = "flex";
            tulipanesDiv.innerHTML = '';
            for (let i = 0; i < 10; i++) {
                const tulipan = document.createElement("div");
                tulipan.classList.add("tulipan");
                tulipanesDiv.appendChild(tulipan);
            }

            setTimeout(() => {
                document.getElementById("mensaje").style.display = "block";
            }, 2000);
        }
    </script>

</body>
</html# Regalo-pancito
