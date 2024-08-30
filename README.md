<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>I'm_caca</title>
    <style>
        @font-face {
            font-family: 'Pixel Operator';
            src: url('PixelOperator.ttf') format('truetype'); /* Ensure PixelOperator.ttf is in the same directory */
        }
        body {
            font-family: 'Pixel Operator', monospace;
            color: #fff;
            background-color: #000;
            margin: 0;
            padding: 0;
        }
        .container {
            padding: 20px;
        }
        h1 {
            font-size: 18px;
            white-space: pre;
        }
        .links {
            margin-top: 20px;
        }
        .links a {
            display: block;
            color: #0f0;
            text-decoration: none;
            font-size: 16px;
            margin-bottom: 10px;
        }
        .console {
            margin-top: 20px;
            padding: 10px;
            background-color: #222;
            border: 1px solid #0f0;
            height: 150px;
            overflow-y: scroll;
            color: #0f0;
            white-space: pre-wrap;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>
            .___/\\ <br>
            |   )/_____<br>
            |   |/     \\    _/ ___\\ \\__  \\ _/ ___\\ \\__  \\ <br>
            |   |  Y Y  \\   \\  \\___ / __ \\ \\  \\___ / __ \\_<br>
            |___|__|_|  /____\\___  >____  /\\___  >____  /<br>
                      \\/_____/   \\/     \\/     \\/     \\/<br>
        </h1>
        <div class="links">
            <a href="https://discord.com/users/1025675124457873459" target="_blank">My Discord</a>
            <a href="https://discord.gg/TZRFQ9FKFd" target="_blank">Patrosxf Server</a>
            <a href="https://www.roblox.com/users/4853433053/profile" target="_blank">My Roblox Account</a>
            <a href="https://www.roblox.com/groups/17342458/patrosxf#!/about" target="_blank">My Roblox Group</a>
        </div>
        <div class="console" id="console">
            Type here...
        </div>
    </div>
    <script>
        const consoleElement = document.getElementById('console');

        const easterEggs = {
            "innovation's": "https://www.roblox.com/users/799258/profile/",
            "cc": "https://discord.gg/5pqeumQrY9"
        };

        function handleCommand(command) {
            if (easterEggs[command]) {
                window.location.href = easterEggs[command];
            } else {
                consoleElement.textContent += `\nUnknown command: ${command}`;
            }
        }

        function processInput(event) {
            if (event.key === "Enter") {
                event.preventDefault();
                const command = event.target.value.trim();
                handleCommand(command);
                event.target.value = "";
            }
        }

        function initConsole() {
            consoleElement.addEventListener('click', function() {
                const input = document.createElement('input');
                input.type = 'text';
                input.style.width = '100%';
                input.style.background = '#222';
                input.style.color = '#0f0';
                input.style.border = 'none';
                input.style.outline = 'none';
                input.style.fontFamily = 'Pixel Operator';
                consoleElement.textContent = '';
                consoleElement.appendChild(input);
                input.focus();
                input.addEventListener('keydown', processInput);
            });
        }

        initConsole();
    </script>
</body>
</html>
