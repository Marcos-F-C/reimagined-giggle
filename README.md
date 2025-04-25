# TE AMO MI VIDA
Carta para el amor de mi vida
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Carta de Amor Animada</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #fff5f5;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
            padding: 20px;
            overflow: hidden;
            perspective: 1000px;
        }
        
        .envelope-container {
            position: relative;
            width: 400px;
            height: 300px;
            cursor: pointer;
            transition: all 0.5s ease;
            transform-style: preserve-3d;
        }
        
        .envelope {
            position: absolute;
            width: 100%;
            height: 100%;
            background-color: #ff6b81;
            border-radius: 5px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            transform-origin: bottom;
            transition: all 0.5s ease;
            z-index: 2;
        }
        
        .envelope:before {
            content: '';
            position: absolute;
            top: 0;
            width: 0;
            height: 0;
            border-left: 200px solid transparent;
            border-right: 200px solid transparent;
            border-top: 150px solid #e84393;
            transform-origin: top;
            transform: rotateX(0deg);
            transition: all 0.5s ease 0.3s;
        }
        
        .envelope:after {
            content: '';
            position: absolute;
            bottom: 0;
            width: 0;
            height: 0;
            border-left: 200px solid #e84393;
            border-right: 200px solid #e84393;
            border-bottom: 150px solid transparent;
        }
        
        .letter {
            position: absolute;
            width: 90%;
            height: 90%;
            background-color: white;
            left: 5%;
            top: 5%;
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
            padding: 20px;
            box-sizing: border-box;
            transform: translateY(0) scale(0.9);
            opacity: 0;
            transition: all 0.5s ease;
            z-index: 1;
            overflow-y: auto;
        }
        
        .envelope-container.open .envelope {
            transform: rotateX(180deg);
            z-index: 0;
        }
        
        .envelope-container.open .envelope:before {
            transform: rotateX(180deg);
        }
        
        .envelope-container.open .letter {
            transform: translateY(-200px) scale(1);
            opacity: 1;
            transition: all 0.5s ease 0.5s;
            z-index: 3;
        }
        
        .heart {
            color: #ff6b81;
            font-size: 24px;
            position: absolute;
        }
        
        .heart-1 { top: 10px; left: 10px; }
        .heart-2 { top: 10px; right: 10px; }
        .heart-3 { bottom: 10px; left: 10px; }
        .heart-4 { bottom: 10px; right: 10px; }
        
        h1 {
            color: #ff6b81;
            text-align: center;
            margin-bottom: 30px;
            font-size: 28px;
        }
        
        p {
            color: #555;
            line-height: 1.6;
            margin-bottom: 20px;
            font-size: 16px;
        }
        
        .signature {
            font-family: 'Brush Script MT', cursive;
            font-size: 24px;
            color: #ff6b81;
            text-align: right;
            margin-top: 30px;
        }
        
        .date {
            text-align: right;
            color: #888;
            font-style: italic;
            margin-top: 5px;
        }
        
        .instructions {
            position: absolute;
            bottom: 20px;
            width: 100%;
            text-align: center;
            color: #ff6b81;
            font-style: italic;
            opacity: 0;
            transition: opacity 0.5s ease;
        }
        
        .envelope-container:hover .instructions {
            opacity: 1;
        }
        
        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
            100% { transform: translateY(0px); }
        }
        
        .envelope-container {
            animation: float 3s ease-in-out infinite;
        }
    </style>
</head>
<body>
    <div class="envelope-container" id="envelope">
        <div class="envelope"></div>
        <div class="letter">
            <div class="heart heart-1">♥</div>
            <div class="heart heart-2">♥</div>
            <div class="heart heart-3">♥</div>
            <div class="heart heart-4">♥</div>
            
            <h1>Mi Amor</h1>
            
            <p>Querida Dayra López</p>
            
            <p>Desde el momento en que entraste en mi vida, todo cobró un nuevo significado. Tu sonrisa ilumina mis días más oscuros y tu amor llena mi corazón de una felicidad que nunca antes había conocido.</p>
            
            <p>Cada día a tu lado es un regalo que me maravilla profundamente. En tus ojos encuentro un hogar del cual no tengo duda alguna que es en el cual, quiero pasar el resto de mis días y en tus abrazos, mi paz y el calor de un cariño sincero. No hay palabras suficientes para expresar lo mucho que significas para mí, lo tanto que te amo y lo que deseo ser parte de tu vida el resto de la mía.</p>
            
            <p>Prometo amarte en cada momento, en las risas y en las lágrimas, en la calma y en la tormenta, en nuestras peleas y discusiones, en los momentos de amor y en los de disgusto, pero jamás dejar de amarte. Eres lo mejor que me ha pasado y haré todo lo posible para que cada día sientas lo especial que eres.</p>

	 <p> Feliz primer mes a tu lado y los que nos faltan amor de mi vida.</p>
            
            <p>Con todo mi amor y cariño, te amo y amaré siempre.</p>
            
            <div class="signature">Marcos Fuentes</div>
            <div class="date">24 de abril del 2025</div>
        </div>
        <div class="instructions">Haz clic para abrir el sobre</div>
    </div>

    <script>
        const envelope = document.getElementById('envelope');
        envelope.addEventListener('click', function() {
            this.classList.toggle('open');
            
            // Cambiar el texto de instrucción después de abrir
            const instructions = document.querySelector('.instructions');
            if (this.classList.contains('open')) {
                setTimeout(() => {
                    instructions.textContent = "Haz clic para cerrar el sobre";
                }, 500);
            } else {
                setTimeout(() => {
                    instructions.textContent = "Haz clic para abrir el sobre";
                }, 500);
            }
        });
    </script>
</body>
</html>
