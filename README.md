<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Be My Valentine?</title>
    <style>
        body { text-align: center; font-family: Arial, sans-serif; }
        #letterBox { display: none; }
    </style>
</head>
<body>
    <h1>Can I be your Valentine? 💖</h1>
    <button onclick="askValentine('yes')">Yes</button>
    <button onclick="askValentine('no')">No</button>
    
    <div id="letterBox">
        <h2>Yay! Write or edit your sweet letter:</h2>
        <textarea id="letter" rows="5" cols="30">My dearest Valentine,
From the moment I met you, my world has been brighter.
Every smile, every laugh, every moment with you is a treasure.
You make my days sweeter, my nights warmer, and my heart fuller.
💖</textarea><br>
        <button onclick="submitLetter()">Send</button>
    </div>
    
    <script>
        function askValentine(answer) {
            if (answer === 'yes') {
                document.getElementById('letterBox').style.display = 'block';
            } else {
                let messages = ["Please? 🥺", "Try again? 🙏", "Think about it... 😘", "Are you sure? 😢", "Just one more chance? 💕"];
                alert(messages[Math.floor(Math.random() * messages.length)]);
            }
        }

        function submitLetter() {
            let letter = document.getElementById('letter').value;
            alert("Your letter: \n" + letter + "\nYou can edit it anytime before she says yes!");
        }
    </script>
</body>
</html>
