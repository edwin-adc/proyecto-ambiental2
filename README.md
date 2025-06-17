  #playPauseBtn {
    position: absolute;
    bottom: 14px;
    right: 14px;
    background: #4caf50cc;
    border: none;
    color: white;
    font-size: 2rem; /* más grande */
    border-radius: 50%;
    width: 56px; /* más grande */
    height: 56px; /* más grande */
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: background-color 0.3s ease, transform 0.3s ease;
    box-shadow: 0 0 10px #4caf50cc;
    user-select: none;
  }

  #playPauseBtn:hover,
  #playPauseBtn:focus {
    background: #388e3ccc;
    outline: none;
    transform: scale(1.2);
  }

  #playPauseBtn[aria-pressed="true"] {
    background: #d32f2fcc;
    box-shadow: 0 0 12px #d32f2fcc;
  }

  #videoEndedMsg {
    position: absolute;
    top: 14px;
    left: 50%;
    transform: translateX(-50%);
    background-color: #81c784dd;
    color: #1b5e20;
    padding: 10px 18px;
    border-radius: 20px;
    font-weight: 700;
    font-size: 1.1rem;
    pointer-events: none;
    user-select: none;
    opacity: 0;
    transition: opacity 0.5s ease;
  }

  #videoEndedMsg.show {
    opacity: 1;
  }

  .info-proyecto {
    flex: 1 1 400px;
    font-size: 1.15rem;
    color: #2e7d32;
    line-height: 1.6;
    user-select: text;
  }

  @media (max-width: 900px) {
    .contenido-proyecto {
      flex-direction: column;
      text-align: center;
    }
    .info-proyecto {
      max-width: 90%;
      margin: 0 auto;
    }
    .video-container {
      max-width: 100%;
      flex: 1 1 auto;
    }
  }

  @keyframes fadeInUp {
    from {
      opacity: 0;
      transform: translateY(15px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }

  .visually-hidden {
    position: absolute !important;
    height: 1px; width: 1px;
    overflow: hidden;
    clip: rect(1px, 1px, 1px, 1px);
    white-space: nowrap;
  }
</style>

<script>
  document.addEventListener('DOMContentLoaded', () => {
    const video = document.getElementById('ecoladrillosVideo');
    const btn = document.getElementById('playPauseBtn');
    const endedMsg = document.getElementById('videoEndedMsg');

    function updateButton() {
      if(video.paused) {
        btn.textContent = '▶️';
        btn.setAttribute('aria-label', 'Reproducir video');
        btn.setAttribute('aria-pressed', 'false');
      } else {
        btn.textContent = '⏸️';
        btn.setAttribute('aria-label', 'Pausar video');
        btn.setAttribute('aria-pressed', 'true');
      }
    }

    btn.addEventListener('click', () => {
      if(video.paused) {
        video.play();
      } else {
        video.pause();
      }
    });

    video.addEventListener('play', () => {
      updateButton();
      endedMsg.classList.remove('show');
    });

    video.addEventListener('pause', updateButton);

    video.addEventListener('ended', () => {
      updateButton();
      endedMsg.classList.add('show');
    });

    // Inicializar estado del botón
    updateButton();
  });
</script>

  </section>
    </section>
  </section>

<section id="programacion" class="section">
  <h2>Especialidad en Programación</h2>
  <ul>
    <li>MANEJO DE RESIDUOS SOLIDOS .</li>
    <li>Nuestro programa puede ayudar a la empresa a optimizar la asiganacion de recursos de recursos,evitando el uso inecesario de lectricidad agua o materiales
        Aparte la reduccion de energia aumentaria aun mas .</li>
  </ul>
  <!-- Más contenido de programación -->
  
  <!-- Imagen con tamaño más pequeño -->
  <div class="imagen-container">
    <img src="data:image/jpeg;base64,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" alt="Imagen 1 - Gestión de Residuos" class="imagen-pequena">
    <p></p>
  </div>
</section>

<footer>
  &copy; 2025 Proyecto Ambiental CBTis 118 - CULTURA DIGITAL
</footer>

<script>
  function showSection(sectionId, btn) {
    // Ocultar todas las secciones
    const sections = document.querySelectorAll('.section');
    sections.forEach(section => {
      section.classList.remove('active');
    });

    // Mostrar solo la sección seleccionada
    const selected = document.getElementById(sectionId);
    if (selected) {
      selected.classList.add('active');
      selected.scrollIntoView({ behavior: 'smooth' });
    }

    // Manejar estilos de botón activo
    const buttons = document.querySelectorAll('nav button');
    buttons.forEach(button => button.classList.remove('active'));
    if (btn) {
      btn.classList.add('active');
    }
  }
</script>

