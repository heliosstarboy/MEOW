<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Do You Love Me?</title>
    <style>
        body {
            font-family: 'Comic Sans MS', cursive, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #ffebf0;
        }
        .container {
            text-align: center;
            background-color: white;
            padding: 20px;
            border-radius: 15px;
            box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.2);
        }
        .question {
            font-size: 28px;
            font-weight: bold;
            color: #ff4081;
            margin-bottom: 20px;
        }
        .button {
            padding: 12px 24px;
            margin: 5px;
            font-size: 18px;
            cursor: pointer;
            border: none;
            border-radius: 8px;
            transition: 0.3s;
        }
        .yes-button {
            background-color: #4CAF50;
            color: white;
        }
        .no-button {
            background-color: #f44336;
            color: white;
            position: absolute;
        }
        .button:hover {
            opacity: 0.8;
        }
        .response {
            font-size: 22px;
            margin-top: 20px;
            color: #ff4081;
        }
    </style>
</head>
<body>

<div class="container">
    <div class="question">
        DO YOU LOVE ME? 💖🥺
    </div>
    <button class="button yes-button" onclick="showResponse('YAY! LOVE YOU TOO! 💕🥰')">Yes</button>
    <button class="button no-button" onclick="askAgain(this)">No</button>
    
    <div id="response" class="response"></div>
</div>

<script>
    function showResponse(answer) {
        document.getElementById('response').innerText = answer;
    }

    function askAgain(button) {
        let response = document.getElementById('response');
        if (response.innerText === "Are you really sure? :<") {
            response.innerText = "Really, really sure? 😢";
        } else if (response.innerText === "Really, really sure? 😢") {
            response.innerText = "Okay... 💔";
        } else {
            response.innerText = "Are you really sure? :<";
        }
    }
</script>

</body>
</html>
