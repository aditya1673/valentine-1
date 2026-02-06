# valentine-1
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Be My Valentine?</title>
<style>
    body {
        font-family: Arial, sans-serif;
        text-align: center;
        background: #ffe6e6;
        margin-top: 100px;
    }

    h1 {
        font-size: 40px;
    }

    button {
        font-size: 20px;
        padding: 10px 20px;
        margin: 20px;
        border: none;
        border-radius: 8px;
        cursor: pointer;
    }

    #yesBtn {
        background-color: #ff4d6d;
        color: white;
        transition: transform 0.3s ease;
    }

    #noBtn {
        background-color: #666;
        color: white;
        position: absolute;
    }

    #message {
        font-size: 30px;
        color: #ff4d6d;
        margin-top: 30px;
    }
</style>
</head>

<body>

<h1>Will you be my Valentine?</h1>

<button id="yesBtn">Yes</button>
<button id="noBtn">No</button>

<div id="message"></div>

<script>
let yesBtn = document.getElementById("yesBtn");
let noBtn = document.getElementById("noBtn");
let message = document.getElementById("message");

let size = 1;

noBtn.addEventListener("mouseover", function() {
    let x = Math.random() * (window.innerWidth - 100);
    let y = Math.random() * (window.innerHeight - 50);
    noBtn.style.left = x + "px";
    noBtn.style.top = y + "px";

    size += 0.2;
    yesBtn.style.transform = "scale(" + size + ")";
});

yesBtn.addEventListener("click", function() {
    document.body.innerHTML = "<h1>Yay! ❤️</h1><p>See you on Valentine’s Day!</p>";
});
</script>

</body>
</html>
