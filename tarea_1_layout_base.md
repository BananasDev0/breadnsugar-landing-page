# 🧩 Tarea 1 — Creación del Layout Base

## 🎯 Objetivo
Implementar la estructura principal del sitio web de **Bread’n’Sugar**, que servirá como el esqueleto sobre el cual se integrarán todos los componentes y secciones futuras.

## 🧱 Descripción
En esta tarea se construirá el **layout base** del proyecto, compuesto por la estructura HTML principal y la configuración global de estilos y tipografías.  
El propósito es garantizar que todas las páginas compartan un diseño consistente, limpio y centrado, conforme a la estética definida en el documento de diseño.

## 📁 Archivos a crear

### 1. `src/layouts/BaseLayout.astro`
- Servirá como plantilla raíz para todas las páginas.  
- Incluirá las fuentes globales **Playfair Display** (para títulos) y **Poppins** (para texto).  
- Aplicará el color de fondo principal `#FFF7F1` y un contenedor centralizado con `max-width` de aproximadamente `80rem`.  
- Contendrá las etiquetas `<Header />`, `<main>` y `<Footer />` o sus equivalentes.  

### 2. `src/components/Header.astro`
- Definirá la barra superior fija con el logotipo 🧁, el nombre “Bread’n’Sugar” y la navegación principal (*Sobre*, *Galería*, *Tienda*, *Personalizados*, *Contacto*).  
- Usará una estructura sencilla con `<header>` y `<nav>`, priorizando espacios y legibilidad.  
- Deberá mantener su diseño estable al hacer scroll (posición `sticky`).  

### 3. `src/components/Main.astro`
- Será el contenedor general para el cuerpo del sitio (`<main>`).  
- Gestionará la disposición de las secciones (Hero, Sobre, Galería, Tienda, Personalizados, Contacto) mediante `slot`.  
- Incluirá márgenes verticales generosos y centrado del contenido.  

## 🎨 Estilos globales
Archivo: `src/styles/global.css`

```css
@import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600&family=Poppins:wght@300;400;500&display=swap');

:root {
  --bg-color: #FFF7F1;
  --accent-color: #E7B7A0;
  --text-color: #6b5a58;
  --heading-color: #2F2726;
  --border-color: #EEDBD3;
}

body {
  background-color: var(--bg-color);
  color: var(--text-color);
  font-family: 'Poppins', sans-serif;
  line-height: 1.6;
  margin: 0;
}

h1, h2, h3, h4, h5, h6 {
  font-family: 'Playfair Display', serif;
  color: var(--heading-color);
}

a {
  color: var(--text-color);
  text-decoration: none;
}

a:hover {
  color: var(--accent-color);
}
```

## ✅ Resultado esperado
Una estructura base funcional y visualmente coherente que actúe como marco del sitio.  
Todas las páginas de Bread’n’Sugar deberán heredar de `BaseLayout.astro`, garantizando un diseño uniforme y preparado para añadir las secciones de contenido.