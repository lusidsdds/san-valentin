<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>San Valentín</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            height: 100vh;
            background-color: white;
            font-family: Arial, sans-serif;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            background-image: url('https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRC3KnXmyrNeYcCX1pdHBTZ6PameveMe8EZe56QJqazCTo5d-fHedGex4JBCDLI7iYJUoE&usqp=CAU');
            background-size: cover;
            background-position: center;
            position: relative;
            color: white;
            text-align: center;
            height: 100vh;
        }

        h1 {
            font-size: 3em;
            font-weight: bold;
            color: red;
        }

        h2 {
            font-size: 2em;
            font-weight: bold;
            color: white;
            margin-top: -20px;
        }

        .buttons {
            margin-top: 20px;
            display: flex;
            justify-content: center;
            gap: 20px;
        }

        .button {
            padding: 15px 30px;
            font-size: 1.2em;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        .button-yes {
            background-color: navy;
            color: white;
        }

        .button-no {
            background-color: red;
            color: white;
        }

        .button-large {
            padding: 25px 50px;
            font-size: 1.5em;
            background-color: darkorange;
            color: white;
            border: none;
            border-radius: 10px;
            margin-top: 30px;
        }

        .small-text {
            font-size: 0.8em;
            margin-top: 10px;
        }

        /* Video Background */
        video {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
            z-index: -1;
        }
    </style>
</head>
<body>
    <!-- Video background -->
    <video autoplay muted loop>
        <source src="https://www.youtube.com/watch?v=VzmtIUmjkTo" type="video/mp4">
    </video>

    <h1>¿Quieres ser mi San Valentín?</h1>
    <h2>Nahomy</h2>

    <div class="buttons">
        <button class="button button-yes" onclick="window.location.href='https://wa.me/34XXXXXXX'">Sí</button>
        <button class="button button-no" onclick="showLargeButton()">No</button>
    </div>

    <!-- Large Button when "No" is pressed -->
    <button class="button-large" id="largeButton" style="display: none;" onclick="scheduleAppointment()">Es sí o sí, no hay más</button>

    <div class="small-text">
        <p>Pulsa el botón nuevamente para agendar cita</p>
    </div>

    <script>
        function showLargeButton() {
            document.getElementById("largeButton").style.display = "block";
        }

        function scheduleAppointment() {
            alert("Agendando cita...");
            window.location.href = "https://wa.me/34XXXXXXX"; // Reemplaza con tu número de WhatsApp
        }
    </script>
</body>
</html>
