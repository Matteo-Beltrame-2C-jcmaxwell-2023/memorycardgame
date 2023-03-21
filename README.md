
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>

    <style>
        img {
            width: 100px;
        }
    </style>
</head>

<body>

    <div id="tavolo"></div>

    <script>
        let ncartegirate = 0
        carte = ["front.jpg","front.jpg","2front.jpg" ,"2front.jpg","3front.jpg","3front.jpg","4front.jpg","4front.jpg","5front.jpg","5front.jpg","6front.jpg","6front.jpg","7front.jpg","7front.jpg","8front.jpg","8front.jpg","9front.jpg","9front.jpg"]

        tavolo = document.querySelector('#tavolo')

        carte.forEach(element => {
            tavolo.innerHTML += '<img id="'+element+'" src="retro.jpg" onclick="gira(this)" />'
            console.log('<img id="'+element+'" src="retro.jpg" />')
        });

        function gira(carta) {
            ncartegirate++
            carta.src = carta.id
            console.log(carta.src)
            if (ncartegirate == 1)
                primacartagirata = carta
            else {
                ncartegirate = 0
                if (carta.src == primacartagirata.src)
                    console.log('BRAVO+1 punto')
                else {
                    console.log('RIPROVACI')
                    carta.src = "retro.jpg"
                    primacartagirata.src = "retro.jpg"


                }


            }
             }
    </script>
</body>
