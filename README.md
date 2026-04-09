<!DOCTYPE html>
<html>
<head>
    <title>Meu Chat</title>
    <style>
        body {
            font-family: Arial;
            background: #f0f0f0;
            text-align: center;
        }

        #chat {
            width: 300px;
            margin: 20px auto;
            background: white;
            padding: 10px;
            border-radius: 10px;
        }

        #messages {
            height: 200px;
            overflow-y: auto;
            border: 1px solid #ccc;
            margin-bottom: 10px;
            padding: 5px;
            text-align: left;
        }

        input {
            width: 70%;
            padding: 5px;
        }

        button {
            padding: 5px;
        }
    </style>
</head>
<body>

    <h2>💬 Meu Primeiro Chat</h2>

    <div id="chat">
        <div id="messages"></div>

        <input id="input" placeholder="Digite uma mensagem..." />
        <button onclick="enviar()">Enviar</button>
    </div>

    <script>
        function enviar() {
            const input = document.getElementById("input");
            const msg = input.value;

            if (msg === "") return;

            const div = document.createElement("div");
            div.textContent = "Você: " + msg;

            document.getElementById("messages").appendChild(div);

            input.value = "";
        }
    </script>

</body>
</html>
