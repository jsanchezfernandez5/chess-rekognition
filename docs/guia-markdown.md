# Sobre Markdown - Pequeña guía

**Markdown** es un lenguaje de marcado ligero que permite dar formato a un texto utilizando símbolos simples (como asteriscos o almohadillas). Fue creado en 2004 para que el contenido sea fácil de leer, escribir y convertir a otros formatos (como HTML o PDF) sin necesidad de usar editores complejos.

> `Ctrl (Cmd macOS) + Shift + V` Abrir preview  en Visual Code Studio en pestaña nueva

## Encabezados

```markdown
# H1 — Título principal
## H2 — Sección
### H3 — Subsección
#### H4
##### H5
###### H6
```

Ejemplos:

- # Encabezado H1
- ## Encabezado H2
- ### Encabezado H3
- #### Encabezado H4
- ##### Encabezado H5
- ###### Encabezado H6

## Énfasis de texto

```markdown
**negrita**
*cursiva*
~~tachado~~
**_negrita y cursiva_**
`código inline`
```

Ejemplo:

- **negrita**
- *cursiva*
- ~~tachado~~
- **_negrita y cursiva_**
- `código inline`

## Listas

**Desordenada:**
```markdown
- Elemento uno
- Elemento dos
  - Sub-elemento
  - Sub-elemento
- Elemento tres
```

Ejemplo:

- Elemento uno
- Elemento dos
  - Sub-elemento
  - Sub-elemento
- Elemento tres

**Ordenada:**
```markdown
1. Primero
2. Segundo
   1. Sub-elemento
3. Tercero
```

Ejemplo:

1. Primero
2. Segundo
   1. Sub-elemento
3. Tercero

**Checklist:**
```markdown
- [x] Tarea completada
- [ ] Tarea pendiente
- [ ] Otra tarea
```

Ejemplo:

- [x] Tarea completada
- [ ] Tarea pendiente
- [ ] Otra tarea

## Links e Imágenes

**Enlace básico:**
```markdown
[Texto del enlace](https://url.com)
[Enlace con título](https://url.com "Título opcional")
```

Ejemplo:

- [Texto del enlace](https://url.com)
- [Enlace con título](https://url.com "Título opcional")

**Imagen:**
```markdown
![Texto alternativo](imagen.png)
![Alt](imagen.png "Título opcional")
```

Ejemplo:

- ![Texto alternativo](imagen.png)
- ![Alt](imagen.png "Título opcional")

**Imagen con enlace:**
```markdown
[![Alt de imagen](imagen.png)](https://url.com)
```

Ejemplo:

- [![Alt de imagen](imagen.png)](https://url.com)

## Bloques de código

**Código inline:**
```markdown
Usa `npm install` para instalar.
```

Ejemplo:

- Usa `npm install` para instalar.

**Bloque con resaltado de lenguaje:**
```markdown
\`\`\`javascript
const saludo = 'Hola ajedrecista';
console.log(saludo);
\`\`\`
```

Ejemplo:

```javascript
javascript
const saludo = 'Hola ajedrecista';
console.log(saludo);
```


**Lenguajes soportados:** `javascript` `typescript` `python` `bash` `html` `css` `json` `sql` `yaml` `markdown` `java` `rust`

## Tablas

```markdown
| Columna 1 | Columna 2 | Columna 3 |
|-----------|:---------:|----------:|
| Alineación Izquierda | Alineación Centrado  |  Alineación Derecha  |
| Dato A    | Dato B    |   Dato C  |
```

Ejemplo:

| Columna alineada a la izquierda | Columna centrada | Columna alineada a la derecha |
|-----------|:---------:|----------:|
| Izquierda | Centrado  | Derecha  |
| Dato A    | Dato B    | Dato C  |

## Citas y separadores

**Cita simple y anidada:**
```markdown
> Esta es una cita.
> Puede tener varias líneas.
>> Cita anidada.
```

Ejemplo:

> Esta es una cita.
> Puede tener varias líneas.
>> Cita anidada.

**Separador horizontal:**
```markdown
---

***

___
```

Ejemplo:

---

***

___


---

## Avanzado
**HTML embebido — details/summary:**
```markdown
<details>
  <summary>Haz clic para expandir</summary>
  Contenido oculto aquí.
</details>
```

Ejemplo:

<details>
  <summary>Haz clic para expandir</summary>
  Contenido oculto aquí.
</details>


**Notas al pie:**
```markdown
Texto con nota[^1].

[^1]: Contenido de la nota al pie.
```

Ejemplo:

Texto con nota[^1].

[^1]: Contenido de la nota al pie.

**Escape de caracteres especiales:**
```markdown
\*no es cursiva\*
\# no es encabezado
\[ no es enlace
```

Ejemplo:

- \*no es cursiva\*
- \# no es encabezado
- \[ no es enlace

Caracteres escapables: `\` `` ` `` `*` `_` `{}` `[]` `()` `#` `+` `-` `.` `!` `|`
