# Quotes
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Quote</title>

    <style>

        .widget {
            padding: 5px 5px ;
            color: #000000;
            text-align: center;
                max-width: 95%;
            margin: auto;
            font-variant-caps: petite-caps;
            font-size: 2em;

        }

        div {
             width: 95%;
             min-height: 100px;

            background:
                linear-gradient(to right, black 4px, transparent 4px) 0 0,
                linear-gradient(to right, black 4px, transparent 4px) 0 100%,
                linear-gradient(to left, black 4px, transparent 4px) 100% 0,
                linear-gradient(to left, black 4px, transparent 4px) 100% 100%,
                linear-gradient(to bottom, black 4px, transparent 4px) 0 0,
                linear-gradient(to bottom, black 4px, transparent 4px) 100% 0,
                linear-gradient(to top, black 4px, transparent 4px) 0 100%,
                linear-gradient(to top, black 4px, transparent 4px) 100% 100%;

            background-repeat: no-repeat;
            background-size: 20px 20px;
}

     
    </style>
</head>
<body>

    <div class="widget" id="widget"></div>


<script>

quotes=[
"화이팅",
"당신은 괴짜입니다",
"너에게 키스하고 싶어",
"당신은 예뻐 보인다",
"보고 싶어요",
"Thinking of U",
"I <3 U",
"I miss you.",
"You look good ;) ",
];

const INTERVAL = 86400000;

function dispalyQuote(){

    document.getElementById('widget').innerHTML =quotes[0];
    quotes.forEach((quote, i) => {
        setTimeout(() => {
            document.getElementById('widget').innerHTML =quote;
        }, i * INTERVAL);  
    });
    }

    function dispalyWidget() {
        dispalyQuote();
        setTimeout(dispalyWidget, quotes.length*INTERVAL);
    }
    dispalyWidget()

</script>

</body>
</html>
