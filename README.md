
<html>
<head>
    <title>Contador de Beijos</title>
    <style>
        h1 {
            font-size: 36px;
            font-weight: bold;
            text-align: center;
        }

        p {
            font-size: 24px;
            text-align: center;
        }

        button {
            display: block;
            margin: 0 auto;
            padding: 10px 20px;
            font-size: 18px;
            font-weight: bold;
            background-color: #ff69b4;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <h1>Contador de Beijos</h1>
    <p>Você já deu <span id="contador">0</span> beijos.</p>
    <button onclick="aumentarContador()">Dê um beijo!</button>

    <script>
        function aumentarContador() {
            var contadorAtual = parseInt(document.getElementById("contador").innerHTML);
            contadorAtual++;
            document.getElementById("contador").innerHTML = contadorAtual;
            destacarContador();
        }

        function destacarContador() {
            var contadorElemento = document.getElementById("contador");
            contadorElemento.classList.add("destaque");
            setTimeout(function() {
                contadorElemento.classList.remove("destaque");
            }, 500);
        }
    </script>
</body>
</html>
