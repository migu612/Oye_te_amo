<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>TE AMO</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background-color: #AEDFF7; /* Azul cielo pastel */
      overflow: hidden;
      font-family: sans-serif;
      color: white;
    }

    .teamo {
      position: absolute;
      font-size: 1.2rem;
      color: #ff4081;
      animation: explode 1s ease-out forwards;
      pointer-events: none;
      user-select: none;
    }

    @keyframes explode {
      0% {
        opacity: 1;
        transform: scale(1);
      }
      100% {
        opacity: 0;
        transform: translate(var(--dx), var(--dy)) scale(2);
      }
    }

    .mensaje-central {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      font-size: 3rem;
      animation: pulse 2s infinite;
      color: #ff4081; /* Color rosa romántico */
    }

    @keyframes pulse {
      0%, 100% { transform: translate(-50%, -50%) scale(1); }
      50% { transform: translate(-50%, -50%) scale(1.1); }
    }
  </style>
</head>
<body>
  <div class="mensaje-central">TE AMO MI NEGRITA💖</div>

  <script>
    document.addEventListener('click', (e) => {
      for (let i = 0; i < 12; i++) {
        const span = document.createElement('span');
        span.className = 'teamo';
        span.textContent = 'TE AMO';

        // posición del clic
        span.style.left = `${e.clientX}px`;
        span.style.top = `${e.clientY}px`;

        // dirección aleatoria para la explosión
        const angle = Math.random() * 2 * Math.PI;
        const distance = 60 + Math.random() * 40;
        const dx = Math.cos(angle) * distance;
        const dy = Math.sin(angle) * distance;

        span.style.setProperty('--dx', `${dx}px`);
        span.style.setProperty('--dy', `${dy}px`);

        document.body.appendChild(span);

        // eliminar después de 1 segundo
        setTimeout(() => {
          span.remove();
        }, 1000);
      }
    });
  </script>
</body>
</html>
