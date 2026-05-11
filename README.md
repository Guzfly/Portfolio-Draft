#Portfolio Draft

Aquí va una explicación **clara, visual y práctica** de **cómo se posicionan los elementos en una página web**, especialmente tus `<section>` y otros bloques.  
Esto es clave para que entiendas **cómo controlar dónde va cada cosa** en tu portfolio.

---

# 🧭 1) **Posicionamiento básico: el flujo natural**
Por defecto, los elementos **block** (como `<section>`, `<div>`, `<header>`, `<footer>`) se colocan **uno debajo del otro**, ocupando todo el ancho disponible.

Así:

```
HEADER
SECTION 1
SECTION 2
SECTION 3
FOOTER
```

Esto se llama **document flow**.

Tu portfolio funciona así ahora mismo.

---

# 🎯 2) **Cómo cambiar el posicionamiento**
Aquí entran las herramientas clave de CSS:

## ⭐ **1. Flexbox** → para alinear elementos en fila o columna  
Flexbox es la forma moderna y fácil de posicionar.

Ejemplo: poner elementos en fila:

```css
.container {
    display: flex;
    justify-content: space-between;
    align-items: center;
}
```

---

## ⭐ **2. Grid** → para diseños más complejos  
CSS Grid te permite crear columnas y filas como si fuera Excel.

Ejemplo:

```css
.grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
}
```

---

## ⭐ **3. Position** → para colocar elementos de forma absoluta o fija  
CSS Position tiene 4 modos útiles:

- `static` (por defecto)
- `relative`
- `absolute`
- `fixed` (para menús pegados arriba)
- `sticky` (se pega cuando haces scroll)

Ejemplo de menú fijo:

```css
nav {
    position: fixed;
    top: 0;
    width: 100%;
}
```

---

# 🧩 3) ¿Cómo se posicionan tus `<section>`?
Tus `<section>` ahora mismo se posicionan así:

- Son **block elements**
- Se colocan **uno debajo del otro**
- Tienen `padding` y `margin` para separarse
- Están centrados porque les pusiste `max-width: 900px` y `margin: auto`

Así:

```css
section {
    padding: 60px;
    max-width: 900px;
    margin: auto;
}
```

Esto hace que cada sección quede **centrada y con espacio alrededor**.

---

# 🎨 4) Ejemplo visual de posicionamiento con Flexbox
Si quieres poner 3 proyectos en fila:

```css
.projects {
    display: flex;
    gap: 20px;
}
```

---

# 🧱 5) Ejemplo visual de posicionamiento con Grid
Si quieres una cuadrícula:

```css
.projects {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
}
```
