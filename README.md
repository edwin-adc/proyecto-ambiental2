<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Proyecto Ambiental CBTis 118</title>
  <style>
    /* Estilos */
    :root {
      --dark-bg: #050505;
      --accent: #00e676;
      --text: #f1f1f1;
    }
    * {
      box-sizing: border-box;
      margin: 0; padding: 0;
      scroll-behavior: smooth;
    }
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background-color: var(--dark-bg);
      color: var(--text);
    }
    /* Portada */
    .hero {
      background: url('https://media.istockphoto.com/id/1402801804/es/foto/vista-de-la-naturaleza-de-cerca-de-las-palmeras-y-el-fondo-de-la-monstera-y-la-hoja-de-helecho.jpg?s=612x612&w=0&k=20&c=U2xApVAPMnfv2dGluOXMKuL-gEXbbTTAsXNQZxFBmdQ=') no-repeat center center/cover;
      height: 90vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      color: #fff;
      text-align: center;
      text-shadow: 2px 2px 10px #000;
      animation: zoomFade 3s ease;
      padding: 0 20px;
    }
    .hero h1 {
      font-size: 3.5rem;
      margin-bottom: 10px;
    }
    .hero p {
      font-size: 1.5rem;
    }
    /* Menú */
    nav {
      background-color:#000000ef;
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      padding: 12px 0;
      position: sticky;
      top: 0;
      z-index: 999;
      box-shadow: 0 0 15px #00e676aa;
    }
    nav button {
      background: none;
      border: none;
      color: var(--text);
      padding: 14px 28px;
      cursor: pointer;
      font-size: 16px;
      transition: 0.4s;
      position: relative;
      margin: 4px;
      border-radius: 6px;
    }
    nav button::after {
      content: '';
      position: absolute;
      bottom: 5px;
      left: 50%;
      transform: translateX(-50%);
      width: 0%;
      height: 3px;
      background-color: var(--accent);
      transition: width 0.3s ease;
      border-radius: 3px;
    }
    nav button:hover::after,
    nav button.active::after {
      width: 100%;
    }
    nav button:hover,
    nav button.active {
      color: var(--accent);
      background-color: #003d1f;
      box-shadow: 0 0 10px var(--accent);
    }
    /* Secciones */
    .section {
      display: none;
      max-width: 1000px;
      margin: 40px auto;
      background-color: #1e1e1e;
      border-radius: 12px;
      box-shadow: 0 0 30px #00e676cc;
      padding: 30px 40px;
      animation: slideFade 1s ease;
    }
    .section.active {
      display: block;
    }
    h2 {
      color: var(--accent);
      margin-bottom: 20px;
      font-weight: 700;
    }
    ul {
      list-style: none;
      line-height: 1.8;
      margin-bottom: 30px;
    }
    ul li::before {
      margin-right: 8px;
    }
    .img-box {
      overflow: hidden;
      border-radius: 10px;
      margin-bottom: 25px;
      box-shadow: 0 0 10px #00e67688;
      cursor: pointer;
      transition: transform 0.3s ease;
    }
    .img-box img {
      width: 100%;
      display: block;
      transition: transform 0.7s ease, filter 0.5s ease;
    }
    .img-box:hover img {
      transform: scale(1.08);
      filter: brightness(1.15);
    }
    footer {
      background-color: #111;
      color: #aaa;
      text-align: center;
      padding: 25px 10px;
      font-size: 14px;
      margin-top: 60px;
    }
    @keyframes zoomFade {
      from {
        transform: scale(1.2);
        opacity: 0;
      }
      to {
        transform: scale(1);
        opacity: 1;
      }
    }
    @keyframes slideFade {
      from {
        transform: translateY(40px);
        opacity: 0;
      }
      to {
        transform: translateY(0);
        opacity: 1;
      }
    }
  </style>
</head>
<body>

  <!-- Portada -->
  <div class="hero">
    <h1>Proyecto Ambiental CBTis 118</h1>
    <p>Separación Responsable de Residuos Sólidos y Desarrollo de Hábitos Conscientes de consumo en el CBTis 118 y la comunidad.</p>
  </div>

  <!-- Menú -->
  <nav id="nav-menu">
    <button onclick="showSection('integrantes', this)">Equipo</button>
    <button class="active" onclick="showSection('objetivos', this)">Objetivos</button>
    <button onclick="showSection('matematicas', this)">Matemáticas II</button>
    <button onclick="showSection('lengua', this)">Lengua y Comunicación</button>
    <button onclick="showSection('ingles', this)">Inglés II</button>
    <button onclick="showSection('cultura', this)">Cultura Digital II</button>
    <button onclick="showSection('sociales', this)">Ciencias Sociales II</button>
    <button onclick="showSection('energia', this)">Conservación de Energía</button>
    <button onclick="showSection('programacion', this)">Especialidad</button>

  </nav>
   <section id="integrantes" class="section">
    <h2>Integrantes del equipo</h2>
    <ul>
      <li>Servin Vazquez Karen Marlene.</li>
      <li>Gutierrez Olivares Karla Natalia.</li>
      <li>Yareli Monserrat Maldonado Sanchez.</li>
      <li>Martinez Hernandez Sofia Yaneth.</li>
      <li>Dominguez Castro Edwin Alberto.</li>
    </ul>
  </section>

  <!-- Secciones -->
  <section id="objetivos" class="section active">
    <h2>Objetivos Generales</h2>
    <ul>
      <li>La comunidad escolar del CBTis 118(estudiantes,
personal administrativo y docentes) fomentan en la
comunidad cercana al plantel la conciencia y la
práctica sobre la separación de residuos sólidos a
partir de la difusión, práctica y desarrollo de hábitos
de consumo conscientes que disminuyan la
generación de dichos residuos tanto en la escuela
como en la comunidad.</li>
      <li>Específicos:</li>
      <li>1.Comprender la separación de residuos sólidos: 
Brindar capacitación a la comunidad escolar para que comprenda la
importancia y el proceso adecuado de separación de residuos sólidos.</li>
      <li>2.Practicar la separación responsable:
Implementar estrategias (como el aprendizaje basado en retos)
para garantizar la separación efectiva de residuos sólidos en el centro
escolar y en las ubicaciones elegidas para intervenir en la comunidad.</li>
      <li>3.Distribuir residuos a empresas recicladoras:
Gestionar eficientemente los residuos sólidos, promoviendo distribución a
empresas recicladoras locales.</li>
      <li>4.Difundir los logros:
Compartir las acciones y resultados obtenidos para sensibilizar y motivar a
otros a separar los residuos, esto a través de los espacios digitales
generados.</li>
    </ul>
    <div class="img-box">
      <img src="https://www.gaceta.unam.mx/wp-content/uploads/2023/05/230522-aca5-des-f1-medio-ambiente-responsabilidad-todos.jpg" alt="Separación de residuos" />
    </div>
    </ul>
  </section>

   <section id="matematicas" class="section">
    <h2>Pensamiento Matemático II</h2>
    <ul>
      <li>Como parte del desarrollo del pensamiento matemático, se llevó a cabo un proyecto donde los estudiantes participaron activamente en una iniciativa de recolección de latas de aluminio. El objetivo fue combinar el análisis matemático con acciones ambientales concretas, fomentando la conciencia ecológica y el uso práctico de datos estadísticos.</li>
      <li>Para iniciar el proyecto, se aplicó una encuesta a los estudiantes con el propósito de conocer sus hábitos y disposición hacia el reciclaje. Algunas de las preguntas incluidas fueron:</li>
      <li>¿Separas los residuos en casa?.</li>
      <li>¿Tienes el hábito de reciclar?.</li>
      <li>¿Estarías dispuesto/a a recolectar latas de aluminio?.</li>
      <li>¿Qué crees que se puede hacer con el dinero obtenido por reciclar?.</li>
      <li>A partir de los resultados, se elaboró un análisis que incluyó frecuencias, porcentajes y gráficas para visualizar los datos. La mayoría de los estudiantes mostró interés en participar, aunque también se identificó que muchos no reciclan de forma constante en sus hogares.</li>
      <li>Se organizó una campaña de recolección de latas, dejando claro que no se trataba de consumir más bebidas enlatadas, sino de recolectar aquellas que ya están en circulación o que se encuentran tiradas. Los estudiantes comenzaron a traer latas separadas de sus casas o recolectadas del entorno.</li>
      <li>Desde la perspectiva matemática, se llevaron a cabo cálculos como:</li>
      <li>Total de kilos de latas recolectadas.</li>
      <li>Promedios por alumno y por grupo.</li>
      <li>Cálculo del ingreso económico generado por la venta de latas.</li>
      <li>Con el dinero recaudado, se propuso una dinámica donde los estudiantes identificaron necesidades del aula de matemáticas y sugirieron cómo invertir esos recursos. Algunas ideas destacadas fueron:</li>
      <li>Comprar material didáctico.</li>
      <li>Adquirir juegos o recursos manipulativos.</li>
      <li>Decorar el aula con murales matemáticos.</li>
      <li>Estas propuestas también se analizaron matemáticamente, usando porcentajes de preferencia y estimaciones presupuestales.</li>
      <li>Finalmente, se evaluó el impacto del proyecto en tres niveles:</li>
      <li>Ecológico: Menor cantidad de latas tiradas, reducción de residuos en el entorno escolar.</li>
      <li>Social: Mayor conciencia ambiental entre los estudiantes y sus familias.</li>
      <li>Académico: Aplicación de conocimientos matemáticos en situaciones reales y toma de decisiones basada en datos.</li>
      <li>Conclusión:.</li>
      <li>Este proyecto permitió a los estudiantes ver cómo las matemáticas no solo están en los libros, sino también en las acciones cotidianas. Desde leer gráficas, hacer cálculos, estimar ingresos, hasta analizar datos reales y proponer soluciones, lograron involucrarse de forma activa y responsable en una causa que también beneficia a su entorno..</li>

    </ul>
 <h2>Gráfica: Latas recolectadas por grupo (CBTis 118 - Todos los semestres)</h2>

<div style="max-width: 700px; font-family: Arial, sans-serif;">

<div class="interactive-bar-chart" aria-label="Gráfica interactiva de grupos y semestres" role="img" aria-describedby="chart-desc">
  <p id="chart-desc" class="visually-hidden">Gráfica interactiva mostrando especialidades, grupos y semestres con interacción táctil.</p>

  <!-- Electrónica con grupos A y B -->
  <div class="bar-item" tabindex="0" role="button" aria-pressed="false" aria-label="Electrónica">
    <span class="bar-label">Electrónica</span>
    <div class="bar-wrapper">
      <div class="bar" data-percentage="90" style="--bar-color: linear-gradient(90deg, #2979ff, #1565c0);"></div>
      <span class="percentage">0%</span>
      <div class="tooltip" role="tooltip">Electrónica: 90%</div>
    </div>
    <div class="details" aria-hidden="true">
      <ul>
        <li>Grupo A
          <ul>
            <li>Semestre 2 - 50 alumnos</li>
            <li>Semestre 4 - 50 alumnos</li>
            <li>Semestre 6 - 50 alumnos</li>
          </ul>
        </li>
        <li>Grupo B
          <ul>
            <li>Semestre 2 - 50 alumnos</li>
            <li>Semestre 4 - 50 alumnos</li>
            <li>Semestre 6 - 50 alumnos</li>
          </ul>
        </li>
      </ul>
    </div>
  </div>

  <!-- Puericultura con grupos A y B -->
  <div class="bar-item" tabindex="0" role="button" aria-pressed="false" aria-label="Puericultura">
    <span class="bar-label">Puericultura</span>
    <div class="bar-wrapper">
      <div class="bar" data-percentage="75" style="--bar-color: linear-gradient(90deg, #ff6f00, #ffab00);"></div>
      <span class="percentage">0%</span>
      <div class="tooltip" role="tooltip">Puericultura: 75%</div>
    </div>
    <div class="details" aria-hidden="true">
      <ul>
        <li>Grupo A
          <ul>
            <li>Semestre 2 - 50 alumnos</li>
            <li>Semestre 4 - 50 alumnos</li>
            <li>Semestre 6 - 50 alumnos</li>
          </ul>
        </li>
        <li>Grupo B
          <ul>
            <li>Semestre 2 - 50 alumnos</li>
            <li>Semestre 4 - 50 alumnos</li>
            <li>Semestre 6 - 50 alumnos</li>
          </ul>
        </li>
      </ul>
    </div>
  </div>

  <!-- Logística solo grupo A -->
  <div class="bar-item" tabindex="0" role="button" aria-pressed="false" aria-label="Logística">
    <span class="bar-label">Logística</span>
    <div class="bar-wrapper">
      <div class="bar" data-percentage="60" style="--bar-color: linear-gradient(90deg, #00e676, #00c853);"></div>
      <span class="percentage">0%</span>
      <div class="tooltip" role="tooltip">Logística: 60%</div>
    </div>
    <div class="details" aria-hidden="true">
      <ul>
        <li>Grupo A
          <ul>
            <li>Semestre 2 - 50 alumnos</li>
            <li>Semestre 4 - 50 alumnos</li>
            <li>Semestre 6 - 50 alumnos</li>
          </ul>
        </li>
      </ul>
    </div>
  </div>

  <!-- Mecatrónica solo grupo A -->
  <div class="bar-item" tabindex="0" role="button" aria-pressed="false" aria-label="Mecatrónica">
    <span class="bar-label">Mecatrónica</span>
    <div class="bar-wrapper">
      <div class="bar" data-percentage="70" style="--bar-color: linear-gradient(90deg, #d50000, #9b0000);"></div>
      <span class="percentage">0%</span>
      <div class="tooltip" role="tooltip">Mecatrónica: 70%</div>
    </div>
    <div class="details" aria-hidden="true">
      <ul>
        <li>Grupo A
          <ul>
            <li>Semestre 2 - 50 alumnos</li>
            <li>Semestre 4 - 50 alumnos</li>
            <li>Semestre 6 - 50 alumnos</li>
          </ul>
        </li>
      </ul>
    </div>
  </div>

  <!-- Mecánica Industrial solo grupo A -->
  <div class="bar-item" tabindex="0" role="button" aria-pressed="false" aria-label="Mecánica Industrial">
    <span class="bar-label">Mecánica Industrial</span>
    <div class="bar-wrapper">
      <div class="bar" data-percentage="55" style="--bar-color: linear-gradient(90deg, #9c27b0, #6a1b9a);"></div>
      <span class="percentage">0%</span>
      <div class="tooltip" role="tooltip">Mecánica Industrial: 55%</div>
    </div>
    <div class="details" aria-hidden="true">
      <ul>
        <li>Grupo A
          <ul>
            <li>Semestre 2 - 50 alumnos</li>
            <li>Semestre 4 - 50 alumnos</li>
            <li>Semestre 6 - 50 alumnos</li>
          </ul>
        </li>
      </ul>
    </div>
  </div>
</div>

<style>
  .interactive-bar-chart {
    max-width: 700px;
    margin: 20px auto 40px;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  }
  .bar-item {
    display: flex;
    flex-direction: column;
    align-items: stretch;
    margin-bottom: 22px;
    cursor: pointer;
    outline-offset: 4px;
    transition: transform 0.3s ease;
    position: relative;
    background: #111;
    padding: 10px 15px;
    border-radius: 10px;
  }
  .bar-item:focus {
    outline: 3px solid #00e676;
    outline-offset: 6px;
  }
  .bar-item.active {
    transform: translateY(-12px);
    box-shadow: 0 4px 10px #00e676aa;
  }
  .bar-label {
    font-weight: 700;
    color: #00e676;
    font-size: 1.2rem;
    user-select: none;
    margin-bottom: 6px;
  }
  .bar-wrapper {
    position: relative;
    height: 28px;
    background-color: #222;
    border-radius: 16px;
    overflow: visible;
    box-shadow: inset 0 0 5px #000;
  }
  .bar {
    height: 100%;
    width: 0%;
    background: var(--bar-color);
    border-radius: 16px 0 0 16px;
    box-shadow: 0 0 8px var(--bar-color);
    transition: width 2.5s cubic-bezier(0.4, 0, 0.2, 1);
  }
  .percentage {
    margin-left: 10px;
    font-weight: 600;
    color: #151414;
    min-width: 50px;
    text-align: right;
    font-variant-numeric: tabular-nums;
    user-select: none;
    position: absolute;
    right: 10px;
    top: 0;
    height: 28px;
    line-height: 28px;
  }
  .tooltip {
    position: absolute;
    left: 50%;
    bottom: 100%;
    transform: translateX(-50%) translateY(10px);
    background-color: #00e676cc;
    padding: 6px 12px;
    border-radius: 12px;
    color: #000;
    font-weight: 700;
    font-size: 0.9rem;
    white-space: nowrap;
    opacity: 0;
    pointer-events: none;
    transition: opacity 0.25s ease, transform 0.25s ease;
    user-select: none;
    box-shadow: 0 0 6px #00e676cc;
  }
  .bar-item.active .tooltip {
    opacity: 1;
    transform: translateX(-50%) translateY(-6px);
    pointer-events: auto;
    z-index: 10;
  }
  .details {
    max-height: 0;
    overflow: hidden;
    transition: max-height 0.5s ease, padding 0.3s ease;
    color: #ccc;
    font-size: 0.9rem;
    margin-top: 10px;
    padding-left: 15px;
  }
  .bar-item.active .details {
    max-height: 500px; /* suficientemente alto para mostrar el contenido */
    padding-top: 10px;
  }
  .details ul {
    list-style: none;
    padding-left: 10px;
    margin: 0;
  }
  .details ul ul {
    padding-left: 15px;
  }
  /* Visually hidden for accessibility */
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
    const bars = document.querySelectorAll('.interactive-bar-chart .bar');
    const barItems = document.querySelectorAll('.interactive-bar-chart .bar-item');

    // Animar ancho y porcentaje al cargar
    bars.forEach(bar => {
      const percent = parseInt(bar.getAttribute('data-percentage'));
      setTimeout(() => {
        bar.style.width = percent + '%';
      }, 200);

      // Animar número porcentaje
      const percentageLabel = bar.nextElementSibling;
      let current = 0;
      const intervalTime = 2000 / percent;
      const interval = setInterval(() => {
        if(current >= percent) {
          clearInterval(interval);
          percentageLabel.textContent = percent + '%';
        } else {
          current++;
          percentageLabel.textContent = current + '%';
        }
      }, intervalTime);
    });

    // Funcionalidad interacción click y tecla Enter/Space para expandir detalles
    let activeItem = null;

    function activateBar(barItem) {
      if(activeItem) {
        activeItem.classList.remove('active');
        activeItem.setAttribute('aria-pressed', 'false');
        activeItem.querySelector('.details').setAttribute('aria-hidden', 'true');
      }
      if(activeItem === barItem) {
        activeItem = null;
        return;
      }
      barItem.classList.add('active');
      barItem.setAttribute('aria-pressed', 'true');
      barItem.querySelector('.details').setAttribute('aria-hidden', 'false');
      activeItem = barItem;
    }

    barItems.forEach(item => {
      item.addEventListener('click', () => activateBar(item));
      item.addEventListener('keydown', e => {
        if(e.key === 'Enter' || e.key === ' ') {
          e.preventDefault();
          activateBar(item);
        }
      });
    });
  });
</script>

    </ul>
    <div class="img-box">
      <img src="https://www.derichebourgespana.com/wp-content/uploads/2024/07/Importancia-de-que-las-latas-sean-de-aluminio-para-su-reciclaje.jpg" alt="Análisis de datos" />
    </div>
    </ul>
  </section>

  <section id="lengua" class="section">
    <h2>Lengua y Comunicación II</h2>
    <div class="paec-container">
      <h3>PAEC - Proyecto Aula Escuela Comunidad</h3>
      <p><strong>PAEC - Proyecto Aula Escuela Comunidad</h2>

    <p><strong>Integrantes:</strong></p>
    <ul>
      <li>Maldonado Sánchez Yareli Monserrat</li>
      <li>Servín Vázquez Karen Marlene</li>
      <li>Domínguez Castro Edwin Alberto</li>
      <li>Gutiérrez Olivares Karla Natalia</li>
      <li>Martínez Hernández Sofia Yaneth</li>
    </ul>

    <p><strong>Fecha:</strong> Junio 2025</p>
    <p><strong>Materias:</strong> Lengua y Comunicación (Reseña), Cultura Digital (Página web)</p>

    <h3>Descripción del Proyecto</h3>
    <p>
      El <strong>PAEC</strong>, o Proyecto Aula Escuela Comunidad, es una iniciativa que nace desde el aula con el objetivo de fortalecer los vínculos entre el entorno educativo y la sociedad que lo rodea. En este caso, el proyecto se centra en una problemática ambiental de gran relevancia: la <strong>gestión y reducción de residuos sólidos</strong> dentro del plantel <strong>CBTis 118</strong>.
    </p>
    <p>
      Este proyecto busca fomentar la responsabilidad ambiental y social en la comunidad estudiantil mediante actividades prácticas como la recolección, clasificación, reciclaje y correcta disposición de residuos sólidos. A través de distintas asignaturas y enfoques pedagógicos, se promueve la participación activa del alumnado en acciones concretas que generan un impacto positivo tanto en el ambiente escolar como en la comunidad.
    </p>

    <h3>Objetivo General</h3>
    <p>
      Desarrollar una conciencia ecológica en los estudiantes del CBTis 118 mediante estrategias integrales que impulsen la separación adecuada de residuos sólidos, el reciclaje y el aprovechamiento de materiales reutilizables, mejorando así el entorno escolar y fomentando la colaboración comunitaria.
    </p>

    <h3>Objetivos Específicos</h3>
    <ul>
      <li>Identificar las principales fuentes de residuos dentro del plantel escolar.</li>
      <li>Diseñar campañas de concientización y señalización bilingüe (español-inglés) para los contenedores de residuos.</li>
      <li>Registrar evidencias fotográficas de alumnos que ya practican la separación de residuos.</li>
      <li>Fomentar el uso de tecnologías digitales mediante la creación de un sitio web educativo sobre el tema.</li>
      <li>Motivar la participación de la comunidad escolar y vecinos a través de actividades colaborativas.</li>
    </ul>

    <h3>Importancia del Proyecto</h3>
    <p>
      En el contexto actual, donde el cambio climático y la contaminación ambiental son temas urgentes, proyectos como el PAEC son fundamentales para construir una ciudadanía más consciente. Educar a los jóvenes sobre la correcta gestión de los residuos no solo mejora las condiciones del espacio que habitan, sino que también genera un efecto multiplicador en sus hogares y comunidades.
    </p>
    <p>
      Además, esta propuesta promueve el trabajo en equipo, el pensamiento crítico y el uso de herramientas digitales para resolver problemas reales. Con estas actividades, los estudiantes comprenden que cada acción, por pequeña que sea, puede contribuir al cuidado del planeta.
    </p>

    <h3>Conclusión</h3>
    <p>
      Para que este proyecto tenga un impacto real y duradero, es necesario el compromiso de todos los actores educativos: directivos, docentes, estudiantes y personal administrativo. La colaboración de la comunidad cercana también es clave para ampliar los efectos positivos de esta iniciativa.
    </p>
    <p>
      El PAEC busca dejar una huella más allá del aula. Pretende inculcar hábitos sostenibles que trasciendan al hogar, la calle y el entorno inmediato del CBTis 118. Solo con el esfuerzo conjunto podremos lograr un espacio escolar más limpio, ordenado y respetuoso con el medio ambiente. Este proyecto es una invitación a actuar, a educar y a transformar.
    </p>

    <div class="paec-imagen">
      <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSs3Uur7j_1A2qnPslAbEntuHTgNSqcBNBGtQ&s" alt="Latas recicladas" class="imagen-latas">
    </div>
  </div>
</section>

<style>
  .paec-proyecto {
    background-color: #fefffe;
    padding: 40px 20px;
    border-radius: 10px;
    margin: 40px auto;
    max-width: 900px;
    font-family: 'Segoe UI', sans-serif;
    color: #f3f3f3;
    box-shadow: 0 0 10px rgb(253, 252, 252);
  }

  .paec-container h2 {
    font-size: 2rem;
    margin-bottom: 20px;
    color: #fcfdfd;
    text-align: center;
  }

  .paec-container h3 {
    color: #379683;
    margin-top: 30px;
    font-size: 1.3rem;
  }

  .paec-container ul {
    list-style: disc inside;
    padding-left: 20px;
    margin-top: 5px;
    margin-bottom: 20px;
  }

  .paec-container p {
    line-height: 1.7;
    margin: 12px 0;
    font-size: 1rem;
    text-align: justify;
  }

  .paec-container strong {
    color: #f8f8f8;
  }

  .paec-imagen {
    margin-top: 30px;
    text-align: center;
  }

  .imagen-latas {
    width: 80%;
    max-width: 600px;
    height: auto;
    border: 5px solid #ffffff;
    border-radius: 10px;
    box-shadow: 0 0 15px rgba(240, 229, 229, 0.877);
  }
</style>
    </ul>
</di>
  </section>

  <section id="ingles" class="section">
    <h2>Inglés II</h2>
    <ul>
    </ul>
  </section>

  <section id="cultura" class="section">
    <h2> <section class="galeria-cultura">
  <h2>Galería del Proyecto PAEC</h2>
  <p class="descripcion">A continuación se presentan imágenes de nuestra página web y actividades realizadas como parte del proyecto PAEC. Cada una representa momentos clave en la concientización sobre el reciclaje en nuestro plantel CBTIS 118.</p>

  <div class="grid-imagenes">
    <div class="imagen-box">
      <img src="c:\Users\ADMIN\Downloads\WhatsApp Image 2025-06-16 at 10.44.17 AM.jpeg" alt="Codigo">
      <div class="texto-hover">Código</div>
    </div>
    <div class="imagen-box">
      <img src="c:\Users\ADMIN\Downloads\WhatsApp Image 2025-06-16 at 10.44.20 AM.jpeg" alt="Sección de reciclaje">
      <div class="texto-hover">Código</div>
    </div>
    <div class="imagen-box">
      <img src="c:\Users\ADMIN\Downloads\WhatsApp Image 2025-06-16 at 10.44.18 AM.jpeg" alt="Estudiantes separando residuos">
      <div class="texto-hover">Parte inicial</div>
    </div>
    <div class="imagen-box">
      <img src="c:\Users\ADMIN\Downloads\WhatsApp Image 2025-06-16 at 10.44.18 AM (1).jpeg" alt="Gráfica interactiva del sitio">
      <div class="texto-hover">Apartados </div>
    </div>
    <div class="imagen-box">
      <img src="c:\Users\ADMIN\Downloads\WhatsApp Image 2025-06-16 at 10.44.19 AM.jpeg" alt="Contenedores rotulados">
      <div class="texto-hover">Diseño finales de los apartados </div>
    </div>
    <div class="imagen-box">
      <img src="c:\Users\ADMIN\Downloads\WhatsApp Image 2025-06-16 at 10.44.19 AM (1).jpeg" alt="Página de evidencias">
      <div class="texto-hover">Diseño final</div>
    </div>
  </div>
</section>

<style>
  .galeria-cultura {
    background: #e8f5e9;
    padding: 40px 20px;
    font-family: 'Segoe UI', sans-serif;
    border: 3px solid #00e676;
    border-radius: 12px;
    max-width: 1200px;
    margin: auto;
  }

  .galeria-cultura h2 {
    text-align: center;
    color: #00796b;
    margin-bottom: 10px;
  }

  .descripcion {
    text-align: center;
    max-width: 700px;
    margin: 0 auto 30px;
    font-size: 1.1rem;
    color: #444;
  }

  .grid-imagenes {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
    gap: 20px;
  }

  .imagen-box {
    position: relative;
    overflow: hidden;
    border-radius: 10px;
    box-shadow: 0 6px 15px rgba(0,0,0,0.2);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }

  .imagen-box img {
    width: 100%;
    height: auto;
    display: block;
    transition: transform 0.5s ease;
  }

  .imagen-box:hover {
    transform: translateY(-6px);
    box-shadow: 0 12px 20px rgba(0, 230, 118, 0.4);
  }

  .imagen-box:hover img {
    transform: scale(1.05);
  }

  .texto-hover {
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    background: rgba(0,230,118,0.85);
    color: black;
    padding: 10px;
    font-weight: bold;
    text-align: center;
    transform: translateY(100%);
    transition: transform 0.4s ease;
  }

  .imagen-box:hover .texto-hover {
    transform: translateY(0%);
  }
</style>


  </section>
    </section>
  </section>

  <section id="sociales" class="section">
    <h2>Ciencias Sociales II</h2>
    <ul>
    </ul>
  </section>

  <section id= "energia" class="section">
    <h2>Conservación de Energía</h2>
    <ul>
      <section class="proyecto-ecoladrillos">
  <h2>Proyecto Ecoladrillos: Conservación de la Energía</h2>
  <div class="contenido-proyecto">
    <div class="video-container" tabindex="0" aria-label="Video del proyecto ecoladrillos">
      <video id="ecoladrillosVideo" controls muted preload="metadata" poster="imagenes/ecoladrillos-poster.jpg" aria-describedby="video-desc">
      <source src="videos/ecoladrillos.mp4" type="video/mp4" />
        Tu navegador no soporta el elemento de video.
      </video>
      <button id="playPauseBtn" aria-pressed="false" aria-label="Reproducir video">
        ▶️
      </button>
      <div id="videoEndedMsg" role="alert" aria-live="polite" class="hidden">¡Gracias por ver el video!</div>
      <p id="video-desc" class="visually-hidden">Video sobre el proyecto de ecoladrillos mostrando su fabricación y uso para conservar la energía y el medio ambiente.</p>
    </div>
    <div class="info-proyecto">
      <p>
        El proyecto de <strong>ecoladrillos</strong> busca reducir la contaminación por plásticos reutilizando residuos no reciclables para fabricar bloques que pueden emplearse en diversas construcciones, ayudando a conservar la energía y proteger el medio ambiente.
      </p>
      <p>
        Esta iniciativa permite a nuestra comunidad escolar aprender sobre la importancia de la reducción, reutilización y reciclaje, promoviendo prácticas responsables y sostenibles.
      </p>
      <p>
        Con talleres y actividades prácticas, impulsamos la creación de ecoladrillos para disminuir la generación de residuos sólidos y favorecer un entorno más limpio y saludable.
      </p>
    </div>
  </div>
</section>

<style>
  .proyecto-ecoladrillos {
    max-width: 1100px; /* aumenté el max ancho */
    margin: 40px auto;
    padding: 25px 30px;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    border: 3px solid #4caf50;
    border-radius: 12px;
    background: #e8f5e9;
    box-shadow: 0 8px 20px rgba(76,175,80,0.2);
  }

  .proyecto-ecoladrillos h2 {
    text-align: center;
    color: #2e7d32;
    margin-bottom: 30px;
    opacity: 0;
    animation: fadeInUp 0.8s forwards;
  }

  .contenido-proyecto {
    display: flex;
    flex-wrap: wrap;
    gap: 25px;
    align-items: center;
    justify-content: center;
    opacity: 0;
    animation: fadeInUp 1s 0.4s forwards;
  }

  .video-container {
    position: relative;
    flex: 1 1 600px; /* aumento tamaño base */
    max-width: 720px; /* ancho máximo más grande */
    border-radius: 12px;
    overflow: hidden;
    box-shadow: 0 6px 25px rgba(46,125,50,0.35);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }

  .video-container:hover,
  .video-container:focus-within {
    transform: scale(1.07);
    box-shadow: 0 12px 35px rgba(46,125,50,0.55);
  }

  video {
    width: 100%;
    height: auto;
    display: block;
    border-radius: 12px;
  }

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
