<!DOCTYPE html><html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Open Me</title>
    <style>
        body {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            background-color: #ffefef;
            font-family: Arial, sans-serif;
        }
        .letter {
            width: 300px;
            height: 200px;
            background: white;
            border: 2px solid #ff4d6d;
            border-radius: 10px;
            text-align: center;
            padding: 20px;
            position: relative;
            overflow: hidden;
            transition: transform 0.5s ease-in-out;
        }
        .closed .content {
            display: none;
        }
        .open .content {
            display: block;
        }
        .heart {
            cursor: pointer;
            font-size: 24px;
            color: red;
        }
        .hidden {
            display: none;
        }
        .buttons button {
            margin: 10px;
            padding: 10px 20px;
            border: none;
            background: #ff4d6d;
            color: white;
            font-size: 16px;
            cursor: pointer;
            border-radius: 5px;
        }
    </style>
</head>
<body>
    <audio id="bg-music" loop>
        <source src="palagi-instrumental.mp3" type="audio/mp3">
    </audio><div class="letter closed" id="letter">
    <p>Open Me! Just click the little <span class="heart" onclick="openLetter()">❤</span></p>
    <div class="content hidden">
        <p>Hi love!</p>
        <p>I miss you so much and I love you.</p>
        <p>from nea</p>
        <p>Do you want to reply?</p>
        <div class="buttons">
            <button onclick="reply()">Yes</button>
            <button onclick="reply()">Yes</button>
        </div>
    </div>
</div>

<script>
    function openLetter() {
        document.getElementById("letter").classList.remove("closed");
        document.getElementById("letter").classList.add("open");
        document.querySelector(".content").classList.remove("hidden");
        document.getElementById("bg-music").play();
    }
    
    function reply() {
        alert("Your reply has been sent to the creator!");
    }
</script>

</body>
</html>
