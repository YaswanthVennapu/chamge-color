# chamge-color
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Toggle Button with Animations</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f0f0f0;
            margin: 0;
        }

        .container {
            width: 300px;
            height: 300px;
            background-color: #61dafb;
            display: flex;
            justify-content: center;
            align-items: center;
            border-radius: 12px;
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.1);
            transition: background-color 0.5s ease-in-out;
        }

        .text {
            font-size: 24px;
            color: #fff;
            transition: color 0.5s ease-in-out;
        }

        .button {
            margin-top: 30px;
            padding: 10px 20px;
            font-size: 18px;
            color: #fff;
            background-color: #282c34;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            transition: background-color 0.5s ease-in-out;
        }

        .button:hover {
            background-color: #0c1a24;
        }

        .fade {
            opacity: 0;
            animation: fadeIn 0.5s forwards;
        }

        @keyframes fadeIn {
            to {
                opacity: 1;
            }
        }
    </style>
</head>

<body>

    <div class="container" id="container">
        <div class="text" id="text">Initial State</div>
    </div>

    <button class="button" id="toggleButton">Change</button>

    <script>
        const container = document.getElementById('container');
        const text = document.getElementById('text');
        const button = document.getElementById('toggleButton');
        let isInitialState = true;

        button.addEventListener('click', () => {
            if (isInitialState) {
                container.style.backgroundColor = '#ff6347'; 
                text.textContent = 'Changed State'; 
                text.style.color = 'blue'; 
                button.textContent = 'Revert'; 
            } else {
                container.style.backgroundColor = '#61dafb'; 
                text.textContent = 'Initial State';
                text.style.color = 'green'; 
                button.textContent = 'Change'; 
            }

            isInitialState = !isInitialState; 
        });
    </script>

</body>

</html>
