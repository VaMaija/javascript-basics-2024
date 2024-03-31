<!DOCTYPE html>
<html>

<head>
    <meta charset="UTF-8">
    <title>XX</title>

    <!-- Lomakekenttien laitto vasemmalta tasan -->
    <style>
        label {
            display: block;
            width: 6em;
            float: left;
        }
    </style>

</head>

<body>
    <h3>alennettu hinta</h3>

    <form>
        <p>
        <label>Hinta:</label>
        <input type="text" id="hinta" size="5">
        </p>
        <p>
        <label>Alennus:</label>
        <input type="text" id="alennus" size="4"> %
        </p>
        <input type="button" value="laske" onclick="laskeAlennus()">
    </form>

    <!-- Tänne kirjoitetaan vastaus JavaScriptillä -->
    <div id="vastaus"></div>

    <script>
        // Funktio, jota painike kutsuu
        function laskeAlennus() {

            // Lomakekentän arvon lukeminen
            let hinta = Number(document.getElementById("hinta").value);
            let alennus = Number(document.getElementById("alennus").value);
            // Käsittely
            let alennettuHinta = hinta* (100.0 - alennus) /100;

            // Vastauksen kirjoittaminen html-sivulle
            document.getElementById("vastaus").innerHTML = "<p>Alennettu hinta on: " + alennettuHinta.toFixed(2) + " euroa</p>";
        }
    </script>
</body>

</html>
