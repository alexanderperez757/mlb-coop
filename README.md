# MLB THE SHOW 26 COOP - STATS PRO ⚾🎮
### *Beto vs Nasa Edition*

Este proyecto es un prototipo interactivo en tiempo real diseñado para llevar el registro estadístico y el control de partidos cooperativos en el videojuego *MLB The Show*. Permite trackear eventos de bateo y pitcheo, calculando métricas avanzadas de béisbol de manera dinámica y sincronizada entre múltiples dispositivos gracias a su integración con una base de datos en la nube.

---

## 🚀 Características Principales

*   **Sincronización en Tiempo Real:** Integración nativa con **Firebase Realtime Database** que asegura que cualquier cambio se refleje instantáneamente en todas las pantallas activas.
*   **Módulo de Ofensiva (Lineup):** Registro rápido de hits (1B, 2B, 3B, HR), bases por bolas (BB), carreras impulsadas (RBI), ponches recibidos (K) y outs de contacto.
*   **Módulo de Pitcheo (Bullpen):** Control de ponches recetados (K), outs, hits permitidos, bases por bolas otorgadas, carreras limpias (ER) y carreras sucias (UER).
*   **Cálculo Automático de Métricas Avanzadas:**
    *   **Bateo:** Promedio de bateo (`AVG`) y Slugging (`SLG`).
    *   **Pitcheo:** Entradas lanzadas (`IP`), Efectividad (`ERA`) y `WHIP`.
*   **Control de Estado del Juego:** Marcador dinámico de carreras anotadas/permitidas, control automático de outs por inning y avance de entradas.
*   **Animaciones e Easter Eggs:** Pantalla interactiva especial de celebración al conectar un *Home Run* e integración de sprites dinámicos basados en los nombres de los jugadores (ej. *Beto* / *Nasa*).
*   **Sistema de Bitácora y Reversión (Undo):** Registro detallado de jugadas con la posibilidad de deshacer el último evento para corregir errores de dedo.

---

## 🛠️ Tecnologías Utilizadas

*   **HTML5 & CSS3:** Estructura limpia y semántica.
*   **Tailwind CSS (CDN):** Estilizado moderno, responsivo y con soporte para modo oscuro nativo.
*   **JavaScript (Vanilla ES6):** Lógica del juego, manejo del estado y mutación del DOM.
*   **Firebase (v9 Compat):** Base de datos NoSQL en tiempo real para la persistencia del estado global.

---

## 📦 Estructura del Código Prototipo

El archivo principal está autocontenido en un solo documento para facilitar su portabilidad y testeo rápido:

```text
├── index.html
    ├── <head>          # Estilos personalizados, fuentes (Inter) y CDN de Tailwind
    ├── <body>          # Componentes de la UI
    │   ├── Overlay     # Animación oculta de Home Run
    │   ├── Header      # Título y navegación entre pestañas
    │   ├── Scoreboard  # Marcador en vivo (Runs, Allowed, Outs, Inning)
    │   ├── Vista Juego # Tableros de control para Lineup y Bullpen + Eventos recientes
    │   ├── Vista Stats # Dashboard de estadísticas acumuladas y bitácora histórica
    │   └── Vista Setup # Gestión de roster del equipo y limpieza de datos
    └── <script>        # Configuración de Firebase y Máquina de Estados del juego
