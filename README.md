# Chess Rekognition

> **"Capture every move!"**  
> Reconocimiento visual de jugadas en partidas de ajedrez presencial

Bienvenido al repositorio central de **Chess Rekognition**, un proyecto dedicado a democratizar el ajedrez tradicional con las capacidades modernas de la **Visión Artificial**.

---

## Propósito del Proyecto

**Chess Rekognition** es un **sistema híbrido de reconocimiento visual de jugadas en partidas presenciales de ajedrez**, orientado a su retransmisión en tiempo real sin necesidad de hardware especializado. Los tableros electrónicos existentes (DGT e-Board, ChessNut) tienen un coste unitario de entre 500 € y 800 €, lo que los hace inaccesibles para la mayoría de clubes amateurs y escuelas. Chess Rekognition resuelve este problema utilizando únicamente una cámara convencional sin pagos ni subscripciones.

El sistema se compone de un backend Python con FastAPI, OpenCV y TensorFlow, y un frontend con React, Vite y Tailwind CSS, comunicados en tiempo real mediante WebSockets. El procesamiento de imagen se realiza íntegramente en el servidor, lo que permite delegar la carga computacional del reconocimiento visual fuera del navegador y garantizar la compatibilidad con cualquier dispositivo cliente.

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
*   **Análisis**: Stockfish v17.1 (Integración nativa del motor de ajedrez).
*   **Base de Datos**: MySQL gestionado mediante SQLAlchemy ORM.
*   **Email**: Resend SDK para correos transaccionales.
*   **Seguridad**: PyJWT + Passlib (Bcrypt para encriptación de contraseñas).

## Direcciones de Producción

| Servicio | URL de Acceso | Plataforma |
| :--- | :--- | :--- |
| **Aplicación Web** | [https://chess-rekognition-app.vercel.app](https://chess-rekognition-app.vercel.app) | Vercel |
| **Servidor API** | [https://chess-rekognition-api-production.up.railway.app](https://chess-rekognition-api-production.up.railway.app) | Railway |

## Sobre Markdown - Pequeña guía

**Markdown** es un lenguaje de marcado ligero que permite dar formato a un texto utilizando símbolos simples (como asteriscos o almohadillas). Fue creado en 2004 para que el contenido sea fácil de leer, escribir y convertir a otros formatos (como HTML o PDF) sin necesidad de usar editores complejos.

> `Ctrl (Cmd macOS) + Shift + V` Abrir preview  en Visual Code Studio en pestaña nueva

### Encabezados

```markdown
# H1 — Título principal
## H2 — Sección
### H3 — Subsección
#### H4
##### H5
###### H6
```

### Énfasis de texto

```markdown
**negrita**
*cursiva*
~~tachado~~
**_negrita y cursiva_**
`código inline`
```

### Listas

**Desordenada:**
```markdown
- Elemento uno
- Elemento dos
  - Sub-elemento
  - Sub-elemento
- Elemento tres
```

**Ordenada:**
```markdown
1. Primero
2. Segundo
   1. Sub-elemento
3. Tercero
```

**Checklist:**
```markdown
- [x] Tarea completada
- [ ] Tarea pendiente
- [ ] Otra tarea
```

### Links e Imágenes

**Enlace básico:**
```markdown
[Texto del enlace](https://url.com)
[Enlace con título](https://url.com "Título opcional")
```

**Imagen:**
```markdown
![Texto alternativo](imagen.png)
![Alt](imagen.png "Título opcional")
```

**Imagen con enlace:**
```markdown
[![Alt de imagen](imagen.png)](https://url.com)
```

### Bloques de código

**Código inline:**
```markdown
Usa `npm install` para instalar.
```

**Bloque con resaltado de lenguaje:**
```markdown
\`\`\`javascript
const saludo = 'Hola mundo';
console.log(saludo);
\`\`\`
```

**Lenguajes soportados:** `javascript` `typescript` `python` `bash` `html` `css` `json` `sql` `yaml` `markdown` `java` `rust`

### Tablas

```markdown
| Columna 1 | Columna 2 | Columna 3 |
|-----------|:---------:|----------:|
| Alineación Izquierda | Alineación Centrado  |  Alineación Derecha  |
| Dato A    | Dato B    |   Dato C  |
```

Ejemplo:

| Columna alineado a la izquierda | Columna centrada | Columna alineada a la derecha |
|-----------|:---------:|----------:|
| Izquierda | Centrado  | Derecha  |
| Dato A    | Dato B    | Dato C  |

### Citas y separadores

**Cita simple y anidada:**
```markdown
> Esta es una cita.
> Puede tener varias líneas.
>> Cita anidada.
```

**Separador horizontal:**
```markdown
---

***

___
```

---

### Avanzado
**HTML embebido — details/summary:**
```markdown
<details>
  <summary>Haz clic para expandir</summary>
  Contenido oculto aquí.
</details>
```

**Notas al pie:**
```markdown
Texto con nota[^1].

[^1]: Contenido de la nota al pie.
```

**Escape de caracteres especiales:**
```markdown
\*no es cursiva\*
\# no es encabezado
\[ no es enlace
```

Caracteres escapables: `\` `` ` `` `*` `_` `{}` `[]` `()` `#` `+` `-` `.` `!` `|`
