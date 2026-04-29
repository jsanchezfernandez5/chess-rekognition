# ♟️ Chess Rekognition

Bienvenido al repositorio central de **Chess Rekognition**, un proyecto dedicado a democratizar el ajedrez tradicional con las capacidades modernas de la **Visión Artificial**.

> **"Capture every move, play on!"**  
> Una solución diseñada para que los jugadores se concentren en el tablero físico mientras la tecnología se encarga del registro, análisis y difusión digital.

---

## Propósito del Proyecto

**Chess Rekognition** nace con el objetivo de eliminar las barreras entre el ajedrez físico y el digital. El sistema permite, mediante el uso de una cámara estándar, reconocer un tablero de ajedrez físico en tiempo real, digitalizar las jugadas automáticamente en formato PGN y retransmitirlas en directo a espectadores de todo el mundo.

Este proyecto integra múltiples disciplinas de la computación:
*   **Visión por Computador**: Para el reconocimiento de piezas y detección de movimientos.
*   **Sistemas en Tiempo Real**: Uso de WebSockets para una retransmisión sin latencia.
*   **Análisis Inteligente**: Integración con el motor Stockfish para evaluación de partidas.

---

## Estructura del Ecosistema

El sistema se ha dividido en módulos especializados para garantizar escalabilidad y un despliegue eficiente. Puedes acceder al código fuente completo en sus respectivos repositorios:

| Módulo | Repositorio GitHub | Descripción |
| :--- | :--- | :--- |
| **Página Central** | [chess-rekognition](https://github.com/jsanchezfernandez5/chess-rekognition) | Documentación maestra, actas y gestión del monorepo. |
| **Frontend (App)** | [chess-rekognition-app](https://github.com/jsanchezfernandez5/chess-rekognition-app) | Interfaz de usuario interactiva y cliente de retransmisión. |
| **Backend (API)** | [chess-rekognition-api](https://github.com/jsanchezfernandez5/chess-rekognition-api) | Procesamiento de imagen, lógica de ajedrez y gestión de datos. |

---

## Stack Tecnológico y Librerías

### Frontend (Aplicación React)
Diseñado bajo una estética moderna y funcional, priorizando la experiencia del usuario (UX):
*   **Core**: React 19, Vite, React Router Dom 7.
*   **Estilos**: TailwindCSS 4 (Aesthetics Premium).
*   **Iconografía**: Lucide React.
*   **Lógica de Ajedrez**: `chess.js` (validación de movimientos), `react-chessboard` (visualización).
*   **Animaciones**: Framer Motion.
*   **Seguridad**: Context API + JWT (JSON Web Tokens).

### Backend (API Python)
Un motor robusto capaz de procesar imágenes y gestionar múltiples conexiones simultáneas:
*   **Framework**: FastAPI (Alto rendimiento y WebSockets).
*   **Visión Artificial**: OpenCV (Procesamiento de imagen) y base para TensorFlow.
*   **Análisis**: Stockfish v17.1 (Integración nativa del motor de ajedrez).
*   **Base de Datos**: MySQL gestionado mediante SQLAlchemy ORM.
*   **Email**: Resend SDK para correos transaccionales.
*   **Seguridad**: PyJWT + Passlib (Bcrypt para encriptación de contraseñas).

---

## Direcciones de Producción

| Servicio | URL de Acceso | Plataforma |
| :--- | :--- | :--- |
| **Aplicación Web** | [https://chess-rekognition-app.vercel.app](https://chess-rekognition-app.vercel.app) | Vercel |
| **Servidor API** | [https://chess-rekognition-api-production.up.railway.app](https://chess-rekognition-api-production.up.railway.app) | Railway |
| **Documentación Técnica** | [/docs](https://chess-rekognition-api-production.up.railway.app/docs) | Swagger UI |

---

## Guía de Inicio Rápido (Local)

1. **Clonar el proyecto**:
   ```bash
   git clone https://github.com/jsanchezfernandez5/chess-rekognition.git
   ```
2. **Configurar Backend**:
   Instalar dependencias en `/api` vía `pip install -r requirements.txt` y ejecutar con `uvicorn main:app`.
3. **Configurar Frontend**:
   Instalar dependencias en `/app` vía `npm install` y ejecutar con `npm run dev`.