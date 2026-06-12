<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Blog de Robótica - Unidad III</title>
    <style>
        /* Estilos generales y paleta de colores (tema morado) */
        body { 
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; 
            background-color: #f4f4f9; 
            color: #333; 
            line-height: 1.6; 
            margin: 0; 
            padding: 0; 
        }
        .container { 
            width: 85%; 
            max-width: 900px; 
            margin: 40px auto; 
            overflow: hidden; 
        }
        header { 
            background: #5e2a84; /* Morado principal */
            color: #fff; 
            padding: 30px 20px; 
            border-bottom: #9b59b6 4px solid; 
            border-radius: 10px 10px 0 0; 
            text-align: center; 
        }
        header h1 { 
            margin: 0; 
            font-size: 2.2em;
            letter-spacing: 1px;
        }
        header p {
            margin-top: 10px;
            font-size: 1.1em;
            color: #e0b0ff;
        }
        .post-content { 
            background: #fff; 
            padding: 40px; 
            border-radius: 0 0 10px 10px; 
            box-shadow: 0px 4px 15px rgba(0,0,0,0.05); 
        }
        h2 { 
            color: #5e2a84; 
            border-bottom: 2px solid #f0e6f7; 
            padding-bottom: 10px; 
            margin-top: 30px;
        }
        h3 { 
            color: #732d91; 
            margin-top: 25px;
        }
        p {
            font-size: 1.05em;
            color: #444;
        }
        code {
            background-color: #f0e6f7;
            color: #5e2a84;
            padding: 2px 6px;
            border-radius: 4px;
            font-family: monospace;
            font-weight: bold;
        }
        .img-placeholder { 
            width: 100%; 
            height: auto; 
            max-height: 400px;
            object-fit: cover;
            border-radius: 8px; 
            margin: 20px 0; 
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        .cierre-box { 
            background: #fdfaf6; 
            padding: 20px 25px; 
            border-left: 5px solid #5e2a84; 
            border-radius: 0 8px 8px 0;
            margin-top: 40px; 
            font-style: italic;
        }
    </style>
</head>
<body>

    <div class="container">
        <header>
            <h1>Unidad III: El Cerebro de la Máquina</h1>
            <p>Conceptos Básicos de Programación en Robótica</p>
        </header>

        <div class="post-content">
            <h2>Inicio</h2>
            <p>¡Qué tal, gente! Bienvenidos a esta nueva entrada del blog. Esta semana (la número 14, ya casi cerrando el semestre en la universidad) nos toca meternos de lleno en la Unidad III de nuestro temario. Hoy vamos a hablar de algo bastante interesante: cómo darle "vida" y autonomía a los robots a través del código.</p>
            <p>Si bien mi día a día suele estar más enfocado en el desarrollo web, las bases de datos o estructurando el backend de una aplicación, la lógica que usamos para que un robot se mueva no es tan ajena a nosotros. Al final del día, es pura lógica, pensar en algoritmos y saber darle las instrucciones exactas a la máquina para que haga lo que necesitamos.</p>

            <h2>Desarrollo</h2>
            
            <h3>Lenguajes de Programación para Robots</h3>
            <p>No existe un único "idioma" para hablar con un robot; todo depende del hardware y del objetivo. Los reyes indiscutibles aquí suelen ser C++ y Python. Si ya le metes al código con Python (algo que a mí en lo personal me encanta por lo rápido que te deja levantar la lógica de un proyecto), te vas a sentir súper cómodo usando frameworks estandarizados como ROS (Robot Operating System). Mientras C++ se usa cuando necesitas que el microcontrolador reaccione en milisegundos, Python es la herramienta perfecta para la lógica de alto nivel, visión artificial y machine learning.</p>
            <img src="https://images.unsplash.com/photo-1518770660439-4636190af475?ixlib=rb-4.0.3&auto=format&fit=crop&w=1000&q=80" alt="Placa de circuitos y robótica" class="img-placeholder">

            <h3>Algoritmos y Estructuras de Control</h3>
            <p>Un algoritmo no es más que una serie de pasos secuenciales para resolver un problema. En robótica, las estructuras de control son el pan de cada día. Imagínense que están en una partida de Counter-Strike o farmeando en Minecraft: toman decisiones en tiempo real basadas en su entorno. En el código del robot, hacemos exactamente lo mismo usando condicionales (los clásicos <code>if</code> y <code>else</code>) y bucles (<code>while</code> o <code>for</code>).</p>
            <p>La lógica es: <em>"Si el sensor ultrasónico detecta un obstáculo a menos de 10 cm, entonces detén los motores y gira a la derecha; de lo contrario, sigue avanzando"</em>. Es así como un robot logra mapear y navegar su entorno sin chocar con todo.</p>

            <h3>Programación de Movimientos y Tareas Simples</h3>
            <p>Para que un robot agarre un objeto o avance en línea recta, tenemos que traducir valores numéricos en energía para los motores (actuadores). Empezamos programando tareas muy simples a través de la cinemática. Por ejemplo, calcular a qué ángulo exacto debe rotar un servomotor para que un brazo robótico alcance una coordenada específica en el espacio. Se trata de tomar la data cruda que recogen los sensores, procesarla en nuestra placa, y convertirla en una acción física que interactúe con el mundo real.</p>
            <img src="https://images.unsplash.com/photo-1485827404703-89b55fcc595e?ixlib=rb-4.0.3&auto=format&fit=crop&w=1000&q=80" alt="Brazo robótico en funcionamiento" class="img-placeholder">

            <h2>Cierre</h2>
            <div class="cierre-box">
                <p><strong>En conclusión:</strong> Programar un robot es el arte de conectar el software con el mundo físico. Ya sea que estemos estructurando un sistema web administrativo, masterizando el audio de un podcast para que suene perfecto, o programando un carrito evasor de obstáculos para la universidad, todo se resume a la misma filosofía: entender el problema, dividirlo en tareas más pequeñas y escribir el código que lo resuelva.</p>
                <p>Entender los conceptos básicos de esta Unidad III nos da una base súper sólida para escalar luego a proyectos mucho más complejos. ¡Nos vemos en la próxima entrada y éxito con sus códigos!</p>
            </div>
        </div>
    </div>

</body>
</html>
