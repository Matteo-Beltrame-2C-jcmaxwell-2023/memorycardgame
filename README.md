<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>

    <style>
        img {
            width: 300px;
        }
    </style>
</head>

<body>

    <div id="tavoloDaGioco"></div>

    <div class="container">
        <span class="counter">Punti =</span><span id="counter" class="counter">0</span>
    </div>

    <script>
        carte = ["front.jpg, front.jpg, 2front.jpg, 2front.jpg, 3front.jpg, 3front.jpg,4front.jpg,4front.jpg,5front.jpg,5front.jpg,6front.jpg,6front.jpg,7front.jpg,7front.jpg,8front.jpg,8front.jpg,9front.jpg,9front.jpg,"]
        let NcarteGirate = 0;
        let primaCartaGirata = null
        tavolo = document.querySelector('#tavoloDaGioco')

        carte.forEach(element => {
            tavolo.innerHTML += '<img id="' + element + '" src="retro.jpg" onclick="gira(this)" />'
            console.log('<img id="' + element + '" src="retro.jpg" />')
            
            var counter = document.getElementById("counter");
        var count = 0;
        });

        function gira(carta) {
            NcarteGirate++
            console.log(NcarteGirate)
            carta.src = carta.id
            if (NcarteGirate == 1)
                primaCartaGirata = carta
            else {
                NcarteGirate = 0
                if (carta.src == primaCartaGirata.src) {
                    count++;
                    counter.textContent = count;
                } else {
                    setTimeout(function() {
                        carta.src = "retro.jpg";
                        primaCartaGirata.src = "retro.jpg";
                    }, 1000);
                }
            }
        }


    </script>
</body>

</html>
