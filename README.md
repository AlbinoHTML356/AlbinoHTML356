<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bad Words Detector</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 50px;
        }
        textarea {
            width: 100%;
            height: 100px;
        }
        .warning {
            color: red;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <h1>Bad Words Detector</h1>
    <textarea id="textInput" placeholder="Type your text here..."></textarea>
    <p id="warningMessage" class="warning" style="display: none;">Warning: Bad words detected!</p>

    <script>
        const badWords = ["yawa", "pisti", "gi atay"]; // Add your list of bad words here

        document.getElementById('textInput').addEventListener('input', function() {
            const text = this.value.toLowerCase();
            const warningMessage = document.getElementById('warningMessage');
            const containsBadWords = badWords.some(word => text.includes(word));

            warningMessage.style.display = containsBadWords ? 'block' : 'none';
        });
    </script>
</body>
</html>


