<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jumpscare Website</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: black;
            color: white;
            overflow: hidden;
        }
        #message {
            font-size: 24px;
            text-align: center;
        }
        #jumpscare {
            display: none;
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: black url('https://your-scary-image-link.com/image.jpg') no-repeat center center;
            background-size: cover;
            z-index: 9999;
        }
    </style>
</head>
<body>

<div id="message">Klik di sini untuk melihat sesuatu yang mengejutkan!</div>
<div id="jumpscare"></div>

<audio id="scream" src="https://your-scream-sound-link.com/scream.mp3"></audio>

<script>
    const message = document.getElementById("message");
    const jumpscare = document.getElementById("jumpscare");
    const scream = document.getElementById("scream");

    message.addEventListener("click", () => {
        jumpscare.style.display = "block";
        scream.play();
        setTimeout(() => {
            jumpscare.style.display = "none";
        }, 2000);
    });
</script>

</body>
</html>
