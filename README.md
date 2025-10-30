🌿 Sistema de Riego Automatizado con Reserva de Agua Pluvial
📘 Descripción General

Este proyecto simula un sistema de riego por goteo automatizado, diseñado para optimizar el consumo de agua pluvial en zonas con escasez.
El sistema monitorea la humedad del suelo y el nivel de agua pluvial, controlando el riego de manera automática o manual.
Además, integra una reserva de agua secundaria, que se activa cuando el nivel de agua pluvial llega a su mínimo, trasvasa agua, se vacía y luego se recarga automáticamente.

👥 ¿Para quién está dirigido?

Estudiantes de ingeniería ambiental, agrícola o de software.

Docentes que deseen mostrar cómo se automatizan sistemas sustentables.

Personas interesadas en IoT o recursos hídricos que quieran visualizar un sistema de control lógico basado en sensores.

⚙️ Tecnologías Utilizadas
Tecnología	Uso Principal
HTML5	Estructura del panel de control y visualización de datos.
CSS3	Estilo visual del panel y tanque circular que representa el nivel de agua.
JavaScript (ES6 Modules)	Lógica del sistema: control automático, simulación de sensores, reserva y recarga.
CodeSandbox	Entorno de ejecución interactivo y sin instalación local.
🚀 Cómo Ejecutar el Proyecto

Abrir CodeSandbox

Crea un nuevo proyecto de tipo Vanilla JS.

Sube los archivos: index.html, styles.css, index.mjs y README.md.

Simulación automática

Cada 2 segundos el sistema revisa la humedad y el nivel de agua.

Si la humedad baja del mínimo o el tanque se vacía, se activa el riego o la reserva.

Modo manual

Usa los botones:

Iniciar Riego Manual 💧

Detener Riego Manual ⛔

Ajusta el caudal para observar los cambios en el tiempo estimado.

📂 Estructura del Proyecto
/sistema-riego-pluvial
│
├── index.html        # Interfaz principal del sistema
├── styles.css        # Diseño visual y tanque circular
├── index.mjs         # Lógica del sistema (riego automático y reserva)
└── README.md         # Documentación y justificación técnica

🔄 Diagrama de Flujo del Sistema
          ┌───────────────────────────┐
          │   Inicio del Programa     │
          └────────────┬──────────────┘
                       │
                       ▼
             ¿Humedad < mínima?
                       │
          ┌────────────┴────────────┐
          │                         │
         Sí                         No
          │                         │
          ▼                         ▼
  ¿Nivel de agua > mínimo?       Esperar ciclo
          │
 ┌────────┴────────┐
 │                 │
Sí                 No
 │                 │
 ▼                 ▼
Inicia riego       Activar reserva
automático         (trasvasa agua)
 │                 │
 ▼                 ▼
Aumenta humedad    Nivel de reserva ↓
Nivel pluvial ↓    Nivel pluvial ↑
 │                 │
 ▼                 ▼
¿Reserva vacía? → Inicia recarga lenta
 │
 ▼
Riego finaliza y sistema espera nuevo ciclo

🧠 SECCIÓN: Justificación Técnica
🔹 Elección del Lenguaje y Framework

El sistema se desarrolló en JavaScript puro (ES6) con estructura modular por los siguientes motivos:

Curva de aprendizaje corta:
Permite a estudiantes y docentes comprender la lógica sin conocimientos avanzados de backend o compilación.

Amplia comunidad y documentación:
JavaScript cuenta con una comunidad muy activa, lo que facilita la resolución de dudas y la integración con otras tecnologías.

Ejecución directa en CodeSandbox:
No requiere instalación de entornos, compiladores ni dependencias.
Ideal para entornos educativos y de demostración rápida.

Rendimiento suficiente para simulación visual:
Aunque no es un sistema industrial, JavaScript puede actualizar valores en tiempo real mediante setInterval y manipular el DOM para mostrar los cambios de estado.

Facilidad de integración futura:
Podría conectarse con hardware real (Arduino, ESP32) mediante comunicación serial o API WebSocket sin cambiar la estructura base.

💬 En resumen

Se eligió JavaScript por su accesibilidad, facilidad de despliegue, amplia comunidad y compatibilidad inmediata con navegadores y CodeSandbox.
La prioridad de este proyecto es la simulación educativa de sostenibilidad hídrica, no la automatización industrial.
