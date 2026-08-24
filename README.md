# Chess Rekognition

> **"Capture every move!"**  
> Reconocimiento visual de jugadas en partidas de ajedrez presencial

Bienvenido al repositorio central de **Chess Rekognition**, un proyecto dedicado a democratizar el ajedrez tradicional con las capacidades modernas de la **Visión Artificial**.

---

## Propósito del Proyecto

**Chess Rekognition** es un **sistema híbrido de reconocimiento visual de jugadas en partidas presenciales de ajedrez**, orientado a su retransmisión en tiempo real sin necesidad de hardware especializado. Los tableros electrónicos existentes (DGT e-Board, ChessNut) tienen un coste unitario de entre 500 € y 800 €, lo que los hace inaccesibles para la mayoría de clubes amateurs y escuelas. Chess Rekognition resuelve este problema utilizando únicamente una cámara convencional sin pagos ni subscripciones.

El sistema se compone de un backend Python con FastAPI, OpenCV y TensorFlow, y un frontend con React, Vite y Tailwind CSS, comunicados en tiempo real mediante WebSockets. El procesamiento de imagen se realiza íntegramente en el servidor, lo que permite delegar la carga computacional del reconocimiento visual fuera del navegador y garantizar la compatibilidad con cualquier dispositivo cliente.

Como evolución del producto, el reconocimiento funciona con un sistema **dual de motores**: MobileNetV2 (clasificación casilla a casilla) como motor por defecto, y YOLO26 (detección de objetos con bounding boxes de piezas y manos) como segundo motor en paralelo. Un mecanismo de **fusión por arbitraje de confianza** decide casilla a casilla qué lectura gana, con criterio medible de promoción basado en métricas sobre validación (nunca preferencias). La retransmisión admite además el relay opcional de vídeo en directo al espectador por el mismo WebSocket.

La metodología sigue un enfoque ágil iterativo alineado con las entregas parciales del grado: computación del ajedrez, detección del tablero, entrenamiento del modelo/patrón de las piezas de ajedrez, integración del backend y validación con usuarios reales de clubes de ajedrez.

El resultado esperado es un sistema funcional capaz de reconocer automáticamente las piezas, generar la notación PGN (Portable Game Notation) de la partida y retransmitirla en directo por URL pública. Todo ello, desde el enfoque democratizador de código abierto eliminando la dependencia de hardware.

## Estructura del Ecosistema

El sistema se ha dividido en módulos especializados para garantizar escalabilidad y un despliegue eficiente. Puedes acceder al código fuente completo en sus respectivos repositorios:

| Módulo | Repositorio GitHub | Descripción |
| :--- | :--- | :--- |
| **Frontend (App)** | [chess-rekognition-app](https://github.com/jsanchezfernandez5/chess-rekognition-app) | Interfaz de usuario interactiva y cliente de retransmisión. |
| **Backend (API)** | [chess-rekognition-api](https://github.com/jsanchezfernandez5/chess-rekognition-api) | Procesamiento de imagen, lógica de ajedrez y gestión de datos. |

## Stack Tecnológico y Librerías

### Frontend (Aplicación React)
Diseñado bajo una estética moderna y funcional, priorizando la experiencia del usuario (UX):
*   **Core**: React 19, Vite, React Router Dom 7.
*   **Estilos**: TailwindCSS 4.
*   **Lógica de Ajedrez**: `chess.js` (validación de movimientos), `react-chessboard` (visualización).
*   **Iconografía**: Lucide React.
*   **Animaciones**: Framer Motion.
*   **Seguridad**: Context API + JWT (JSON Web Tokens).

### Backend (API Python)
APIRest en FastAPI de python para el procesamiento de la lógica del ajedrez y la integración con la visión artificial:
*   **Framework**: FastAPI (Alto rendimiento y WebSockets).
*   **Visión Artificial**: OpenCV (Procesamiento de imagen) y base para TensorFlow.
*   **Reconocimiento ML**: MobileNetV2 (TensorFlow, clasificación por casilla) + YOLO26 (Ultralytics, detección de objetos y manos) con fusión por arbitraje.
*   **Análisis**: Stockfish v17.1 (Integración nativa del motor de ajedrez).
*   **Base de Datos**: MySQL gestionado mediante SQLAlchemy ORM.
*   **Email**: Resend SDK para correos transaccionales.
*   **Seguridad**: PyJWT + Passlib (Bcrypt para encriptación de contraseñas).

## Direcciones de Producción

| Servicio | URL de Acceso | Plataforma |
| :--- | :--- | :--- |
| **Aplicación Web** | [https://chess-rekognition-app.vercel.app](https://chess-rekognition-app.vercel.app) | Vercel |
| **Servidor API y BBDD** | [https://chess-rekognition-api-production.up.railway.app](https://chess-rekognition-api-production.up.railway.app) | Railway |

## Sobre Markdown - Pequeña guía

Para consultar la guía de formato Markdown, accede a:
*   [Guía de Markdown](docs/guia-markdown.md)

