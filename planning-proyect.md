# Planificación de Proyecto: Mapa Secreto de la Ciudad - Edición CABA (Versión 5)

## 1. Descripción General

Sitio web estático enfocado en descubrir lugares poco conocidos de la 
Ciudad Autónoma de Buenos Aires. El proyecto integra una arquitectura 
modular y mantenible, superando los requisitos básicos de la consigna 
mediante un mapa interactivo (GeoJSON), un sistema de temas dual
(Día/Noche) que interactúa con los datos y herramientas avanzadas de 
exploración.

---

## 2. Arquitectura de Carpetas y Archivos

Estructura diseñada para facilitar el control de versiones y la escalabilidad.

```text
proyecto/
├── index.html                 # Página de inicio y presentación
├── pages/
│   ├── lugares.html           # Catálogo, buscador, ordenamiento y vista Mis Favoritos
│   └── mapa.html              # Mapa interactivo vectorial
├── assets/
│   ├── css/
│   │   ├── styles.css         # Estilos globales, layout y tipografía
│   │   └── themes.css         # Variables CSS para Modo Día/Noche
│   ├── js/
│   │   ├── main.js            # Lógica global: navbar y theme toggle
│   │   ├── mapa.js            # Renderizado, lógica del GeoJSON y sincronización
│   │   ├── lugares.js         # Buscador, ordenamiento y renderizado de listas
│   │   └── storage.js         # Gestión de favoritos con localStorage
│   ├── data/
│   │   ├── lugares.json       # Base de datos local con horarios, precios y categorías
│   │   └── caba.geojson       # Datos vectoriales para el mapa
│   └── img/                   # Imágenes optimizadas
└── README.md                  # Documentación del proyecto
```

---

## 3. Funcionalidades Principales

### 🔎 Exploración y Búsqueda
- Buscador integrado por nombre y barrio.

### 📂 Filtros y Ordenamiento
- Filtrado por categoría.
- Filtrado por horario.
- Filtrado por precio.
- Ordenamiento dinámico por:
  - Precio.
  - Barrio.
  - Categoría.
  - Nombre (A-Z).

### ⭐ Gestión de Favoritos
- Persistencia de datos mediante `localStorage`.
- Vista dedicada de **Mis Favoritos** dentro de la página de lugares.

### 🌙 Modo Día / Noche
- Toggle almacenado en `localStorage`.
- Adaptación completa de la interfaz.
- Filtrado automático de disponibilidad según el horario de cada lugar.

### 🗺️ Mapa Interactivo Sincronizado
- Carga de coordenadas mediante GeoJSON.
- Sincronización bidireccional:
  - Al hacer clic en un marcador se resalta la tarjeta correspondiente.
  - Al seleccionar una tarjeta, el mapa se centra en esa ubicación.

### 💡 Recomendaciones Argumentadas
Cada lugar incluye una reseña detallada que justifica su incorporación al catálogo.

---

## 4. Fases de Desarrollo

### Fase 1 — Repositorio y Entorno
- Inicialización del repositorio Git.
- Vinculación con GitHub público.
- Creación de ramas:
  - `main`
  - `develop`
- Uso de **Conventional Commits**.

### Fase 2 — Estructura HTML Semántica
- Desarrollo de las tres páginas utilizando HTML5 semántico:
  - `<header>`
  - `<nav>`
  - `<main>`
  - `<section>`
  - `<article>`
  - `<footer>`

### Fase 3 — Datos y Lógica (JavaScript)
- Creación de `lugares.json`.
- Implementación del buscador.
- Funciones de ordenamiento.
- Renderizado dinámico del catálogo.
- Implementación del Theme Toggle.
- Vista exclusiva de Favoritos.

### Fase 4 — Mapa Vectorial y Eventos
- Solicitud asíncrona (`fetch`) de `caba.geojson`.
- Inyección dinámica de marcadores.
- Sincronización visual entre tarjetas y mapa.

### Fase 5 — Estilos y Diseño Responsivo
- Creación de variables CSS en `themes.css`.
- Diseño bajo enfoque **Mobile First**.
- Adaptación mediante Media Queries para:
  - Tablet.
  - Desktop.

### Fase 6 — Integración Final y Deploy
- Revisión de accesibilidad.
- Documentación final.
- Pull Request hacia `main`.
- Despliegue del proyecto.

---

## 5. Accesibilidad Inclusiva

El proyecto implementará las siguientes prácticas para garantizar una experiencia accesible:

- Imágenes con atributo `alt` descriptivo.
- Uso de `aria-label` en botones y enlaces sin texto visible.
- Contraste adecuado entre texto y fondo en ambos temas.
- Navegación completamente funcional mediante teclado.
- Estado `:focus` siempre visible.
- Mensajes de error y éxito representados mediante texto e íconos,
evitando depender únicamente del color.

---

## 6. Organización y Trabajo Colaborativo

Para mantener un historial de Git limpio (mínimo **15 commits**) y
reducir conflictos durante el desarrollo, se establece la siguiente
distribución de tareas:

| Rol | Responsabilidades |
|------|-------------------|
| **Integrante A (Estructura)** | HTML semántico, accesibilidad (`ARIA`, `alt`) y estructura del proyecto. |
| **Integrante B (Diseño)** | CSS, variables de temas, Mobile First, Grid y Flexbox. |
| **Integrante C (Lógica)** | JavaScript, Fetch de JSON, buscador, ordenamiento, `localStorage` y renderizado del mapa. |
| **Equipo Completo** | Revisión de Pull Requests hacia `develop`, resolución de conflictos y control de calidad final. |

---

## 7. Documentación y Entrega

### ✅ README.md

El archivo `README.md` deberá incluir:

- [ ] Nombre del proyecto.
- [ ] Breve descripción.
- [ ] Integrantes del equipo.
- [ ] Tecnologías utilizadas.
- [ ] Herramientas utilizadas.
- [ ] Funcionalidades implementadas.
- [ ] Explicación de la arquitectura del proyecto.
- [ ] Enlace al repositorio público de GitHub.
- [ ] Enlace al proyecto desplegado (Deploy).
- [ ] Referencia al informe de Inteligencia Artificial.

### ✅ Informe de Inteligencia Artificial

El informe (1 a 2 páginas) deberá incluir:

- [ ] Respuestas detalladas a las **10 preguntas obligatorias** de la consigna 
relacionadas con el uso de herramientas de Inteligencia Artificial durante el 
desarrollo del proyecto.

---

## Tecnologías Utilizadas

- HTML5
- CSS3
- JavaScript (ES6+)
- GeoJSON
- LocalStorage
- Fetch API
- Git
- GitHub

---

## Objetivo del Proyecto

Desarrollar un sitio web moderno, modular y accesible que permita descubrir
lugares poco conocidos de la Ciudad Autónoma de Buenos Aires mediante un
catálogo interactivo, un mapa sincronizado y herramientas de búsqueda avanzadas,
aplicando buenas prácticas de desarrollo web, trabajo colaborativo con Git y
una arquitectura escalable.