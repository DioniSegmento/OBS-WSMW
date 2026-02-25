🎛 OBS Multiview + TAKE (Mobile / Tablet)

Interfaz web en un único archivo HTML standalone que convierte cualquier móvil o tablet en un control táctil avanzado para OBS Studio mediante OBS WebSocket v5 (RPC v1).

Optimizada para producción en directo: rápida, ligera y pensada para realización real.

🚀 Características

✅ Conexión directa a OBS por WebSocket (v5)

🟢 Preview y 🔴 Program en tiempo real

🧩 Grid táctil de escenas con miniaturas dinámicas

🎬 Control de transiciones y botón TAKE

🔄 Toggle de Studio Mode

🔴 Indicadores REC / STREAM

🎚 Columna lateral de Fuentes (Scene Items) con ON/OFF

⚡ Refresco optimizado (round-robin thumbnails)

📱 Diseño responsive para tablet y móvil

💾 Configuración persistente (localStorage)

📄 Sin dependencias externas (archivo único)

📸 Vista general

Estructura principal:

| FUENTES | PREVIEW | PROGRAM | DOCK (TRANSICIÓN + TAKE) |
|-----------------------------------------------|
|                GRID DE ESCENAS               |
⚙️ Requisitos

OBS Studio

OBS WebSocket v5 habilitado (puerto 4455 por defecto)

Navegador moderno (Chrome, Edge, etc.)

Acceso de red al equipo que ejecuta OBS

🔌 Conexión

Abrir el archivo mwphone_t.html en el navegador.

Introducir:

URL WebSocket (ej: ws://192.168.1.100:4455)

Contraseña si está configurada.

Pulsar Conectar.

Pulsar Start.

Recomendado en móvil: 1–3 FPS para máxima estabilidad.

🎬 Funcionamiento
🎞 Selección de escenas

Studio Mode ON

Click escena → va a Preview

Pulsar TAKE → pasa a Program

Studio Mode OFF

Click escena → va directo a Program

🎚 Control de fuentes (Scene Items)

Al tocar una escena:

Se cargan sus fuentes en la columna izquierda

Cada fuente puede activarse/desactivarse (ON/OFF)

Ordenadas alfabéticamente

Ideal para overlays, lower thirds, gráficos, etc.

🎛 Transiciones

Permite:

Seleccionar tipo de transición

Ajustar duración en ms

Ejecutar TAKE

⚡ Optimización de rendimiento

Las miniaturas de escenas:

NO se actualizan todas a la vez

Se usa sistema round-robin

Se refrescan solo algunas por ciclo

Esto evita:

Saturación del WebSocket

Caídas de FPS

Latencia excesiva en móvil

Los parámetros de captura son configurables en el bloque CAPTURE dentro del script.

🧠 Arquitectura técnica

Implementa protocolo completo OBS WebSocket v5:

Hello

Identify

Request

RequestResponse

Event

Comandos principales utilizados:

GetStudioModeEnabled

SetStudioModeEnabled

GetCurrentPreviewScene

GetCurrentProgramScene

SetCurrentPreviewScene

SetCurrentProgramScene

GetSceneList

GetSceneTransitionList

SetCurrentSceneTransition

SetCurrentSceneTransitionDuration

TriggerStudioModeTransition

GetSourceScreenshot

GetSceneItemList

SetSceneItemEnabled

GetRecordStatus

GetStreamStatus

📱 Diseño responsive

Layout tablet: columna fija de fuentes + multiview

Layout móvil: apilado vertical

Header plegable

Botón pantalla completa

Optimizado para uso táctil

🔧 Configuración persistente

Se guarda automáticamente en localStorage:

URL WebSocket

Contraseña

FPS

Duración transición

Estado del header

🛠 Posibles ampliaciones

Sliders de audio

Control de filtros

Sistema de atajos configurables

Integración con hardware externo (ESP32, MIDI, etc.)

Modo producción avanzada estilo ATEM

📄 Licencia

Libre para uso personal y profesional.
Puedes modificarlo y adaptarlo según tus necesidades.

🎯 Objetivo del proyecto

Crear un control táctil rápido, ligero y estable para OBS, pensado para operadores reales que necesitan:

Velocidad

Claridad visual

Fiabilidad

Y cero complicaciones

Si quieres, puedo hacerte ahora:

🔥 Versión README más técnica tipo enterprise

💼 Versión comercial para vender el sistema

🧠 Versión ultra detallada para documentación técnica profesional

🎛 Versión enfocada a integración con ESP32 / hardware físico

Tú decides el nivel de locura 😎
