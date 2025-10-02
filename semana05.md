<!-- ENCABEZADO animado con ola -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&height=140&color=0:0F766E,100:0EA5E9&text=📕%20Cuaderno%20Digital%20—%20Semana%2005&fontAlign=50&fontAlignY=35&fontSize=34&fontColor=ffffff&animation=fadeIn" />
</p>

<!-- Animación con el nombre del estudiante -->
<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=26&duration=2500&pause=1000&color=0EA5E9&center=true&vCenter=true&width=820&lines=Estudiante%3A%20Macha%20Pariona%20Angel%20Yoelver;IX%20Semestre%20%E2%80%94%20Facultad%20de%20Ingenier%C3%ADa%20de%20Sistemas;Universidad%20Nacional%20del%20Centro%20del%20Per%C3%BA" />
</p>

---

# 🌌 Semana 05 — **Node.js, npm, React, Vite, Next.js + Práctica Calificada 3**

---

## 🎯 Objetivos
- Conocer en detalle **Node.js** y **npm** como base del ecosistema JavaScript.
- Aprender a crear proyectos con **React**, tanto con CRA como con **Vite**.
- Explorar **Next.js** como framework avanzado con SSR y optimización.
- Practicar el desarrollo con HTML, CSS y JS puro en la **Práctica Calificada 3** (ruleta + sorteo de equipos).
- Integrar teoría, práctica y diseño en un **cuaderno digital organizado**.

---

# 📚 Parte 1 — Node.js y npm

### 🔹 Node.js
<div align="center" style="max-width:760px; margin:12px auto; padding:16px; border:1px solid #e2e8f0; border-radius:14px; background:#f8fafc;">
  <div align="left"><b>Comentario:</b> Node.js permite ejecutar JavaScript en el servidor. Es rápido, ligero y usado para APIs y microservicios.</div>
  <img alt="Node.js" width="520" src="./semana05_imagenes/nodejs.png" />
</div>

Ejemplo de instalación y verificación:
```bash
node -v
npm -v
```

### 🔹 npm (Node Package Manager)
<div align="center" style="max-width:760px; margin:12px auto; padding:16px; border:1px solid #e2e8f0; border-radius:14px; background:#f8fafc;">
  <div align="left"><b>Comentario:</b> npm es el gestor de paquetes que acompaña a Node.js. Permite instalar librerías externas con facilidad.</div>
  <img alt="npm" width="520" src="./semana05_imagenes/npm.png" />
</div>

Comandos básicos:
```bash
npm install <paquete>
npm uninstall <paquete>
npm update
```

<div align="center" style="max-width:760px; margin:12px auto; padding:16px; border:1px solid #e2e8f0; border-radius:14px; background:#f8fafc;">
  <div align="left"><b>Comentario:</b> Ejemplo de instalación de un paquete con npm.</div>
  <img alt="npm install" width="520" src="./semana05_imagenes/npm-install.png" />
</div>

---

# 📚 Parte 2 — React

### 🔹 Conceptos Clave
- Biblioteca de JS para construir interfaces dinámicas.
- Usa **componentes reutilizables**.
- Maneja estado con **Hooks** (`useState`, `useEffect`).
- Virtual DOM para mejorar rendimiento.

<div align="center" style="max-width:760px; margin:12px auto; padding:16px; border:1px solid #e2e8f0; border-radius:14px; background:#f8fafc;">
  <div align="left"><b>Comentario:</b> Logo oficial de React.</div>
  <img alt="React logo" width="400" src="./semana05_imagenes/react-logo.png" />
</div>

### 🔹 Create React App
Comando para iniciar un proyecto React con CRA:
```bash
npx create-react-app mi-app
cd mi-app
npm start
```

<div align="center" style="max-width:760px; margin:12px auto; padding:16px; border:1px solid #e2e8f0; border-radius:14px; background:#f8fafc;">
  <div align="left"><b>Comentario:</b> Ejemplo de consola creando un proyecto con CRA.</div>
  <img alt="Create React App" width="520" src="./semana05_imagenes/create-react.png" />
</div>

### 🔹 Componentes y Hooks
- **Componentes:** bloques de construcción de interfaces.
- **Props:** parámetros que recibe un componente.
- **Hooks:** funciones especiales para manejar estado y ciclo de vida.

<div align="center" style="max-width:760px; margin:12px auto; padding:16px; border:1px solid #e2e8f0; border-radius:14px; background:#f8fafc;">
  <div align="left"><b>Comentario:</b> Diagrama visual de componentes React.</div>
  <img alt="React Components" width="520" src="./semana05_imagenes/react-components.png" />
</div>

<div align="center" style="max-width:760px; margin:12px auto; padding:16px; border:1px solid #e2e8f0; border-radius:14px; background:#f8fafc;">
  <div align="left"><b>Comentario:</b> Hooks principales de React: useState y useEffect.</div>
  <img alt="React Hooks" width="520" src="./semana05_imagenes/react-hooks.png" />
</div>

---

# 📚 Parte 3 — Vite

### 🔹 Conceptos Clave
- Herramienta moderna de bundling y desarrollo.
- Mucho más rápido que CRA.
- Usa ESModules en lugar de bundles pesados.

Instalación:
```bash
npm create vite@latest mi-app
cd mi-app
npm install
npm run dev
```

<div align="center" style="max-width:760px; margin:12px auto; padding:16px; border:1px solid #e2e8f0; border-radius:14px; background:#f8fafc;">
  <div align="left"><b>Comentario:</b> Logo oficial de Vite.</div>
  <img alt="Vite logo" width="400" src="./semana05_imagenes/vite.png" />
</div>

<div align="center" style="max-width:760px; margin:12px auto; padding:16px; border:1px solid #e2e8f0; border-radius:14px; background:#f8fafc;">
  <div align="left"><b>Comentario:</b> Ejemplo de consola al ejecutar npm run dev en Vite.</div>
  <img alt="Vite consola" width="520" src="./semana05_imagenes/vite-console.png" />
</div>

<div align="center" style="max-width:760px; margin:12px auto; padding:16px; border:1px solid #e2e8f0; border-radius:14px; background:#f8fafc;">
  <div align="left"><b>Comentario:</b> Estructura inicial de carpetas en un proyecto Vite.</div>
  <img alt="Vite estructura" width="520" src="./semana05_imagenes/vite-structure.png" />
</div>

---

# 📚 Parte 4 — Next.js

### 🔹 Conceptos Clave
- Framework basado en React con renderizado del lado del servidor (SSR).
- Rutas automáticas basadas en la carpeta `pages`.
- Incluye optimización de imágenes y SEO.

Instalación:
```bash
npx create-next-app mi-app
cd mi-app
npm run dev
```

<div align="center" style="max-width:760px; margin:12px auto; padding:16px; border:1px solid #e2e8f0; border-radius:14px; background:#f8fafc;">
  <div align="left"><b>Comentario:</b> Logo oficial de Next.js.</div>
  <img alt="Next.js logo" width="400" src="./semana05_imagenes/nextjs.png" />
</div>

<div align="center" style="max-width:760px; margin:12px auto; padding:16px; border:1px solid #e2e8f0; border-radius:14px; background:#f8fafc;">
  <div align="left"><b>Comentario:</b> Estructura de un proyecto Next.js (pages, public, styles).</div>
  <img alt="Next.js estructura" width="520" src="./semana05_imagenes/nextjs-structure.png" />
</div>

<div align="center" style="max-width:760px; margin:12px auto; padding:16px; border:1px solid #e2e8f0; border-radius:14px; background:#f8fafc;">
  <div align="left"><b>Comentario:</b> Ejemplo de páginas en Next.js convertidas automáticamente en rutas.</div>
  <img alt="Next.js páginas" width="520" src="./semana05_imagenes/nextjs-pages.png" />
</div>

---

# 📚 Parte 5 — Comparación

| Herramienta | Ventajas | Limitaciones | Uso recomendado |
|-------------|----------|--------------|-----------------|
| CRA | Fácil de usar, oficial de React | Lento en proyectos grandes | Proyectos educativos |
| Vite | Muy rápido, ligero | Menos tutoriales antiguos | Proyectos modernos |
| Next.js | SSR, SEO, optimización | Más complejo | Proyectos profesionales |

<div align="center" style="max-width:760px; margin:12px auto; padding:16px; border:1px solid #e2e8f0; border-radius:14px; background:#f8fafc;">
  <div align="left"><b>Comentario:</b> Comparación visual entre React CRA, Vite y Next.js.</div>
  <img alt="Comparación" width="520" src="./semana05_imagenes/comparacion.png" />
</div>

---

# 📝 Parte 6 — Práctica Calificada 3

### Ruleta dinámica
<div align="center" style="max-width:760px; margin:12px auto; padding:16px; border:1px solid #e2e8f0; border-radius:14px; background:#f8fafc;">
  <div align="left"><b>Comentario:</b> Ruleta dinámica creada en HTML, CSS y JS puro.</div>
  <img alt="Ruleta" width="520" src="./semana05_imagenes/ruleta.png" />
</div>

<div align="center" style="max-width:760px; margin:12px auto; padding:16px; border:1px solid #e2e8f0; border-radius:14px; background:#f8fafc;">
  <div align="left"><b>Comentario:</b> Animación de la ruleta girando y seleccionando un elemento.</div>
  <img alt="Ruleta girando" width="520" src="./semana05_imagenes/ruleta-girando.gif" />
</div>

### Sorteo de equipos
<div align="center" style="max-width:760px; margin:12px auto; padding:16px; border:1px solid #e2e8f0; border-radius:14px; background:#f8fafc;">
  <div align="left"><b>Comentario:</b> Aplicación de sorteo de equipos con participantes distribuidos.</div>
  <img alt="Sorteo de equipos" width="520" src="./semana05_imagenes/sorteo-equipos.png" />
</div>

<div align="center" style="max-width:760px; margin:12px auto; padding:16px; border:1px solid #e2e8f0; border-radius:14px; background:#f8fafc;">
  <div align="left"><b>Comentario:</b> Equipos generados y mostrados en pantalla.</div>
  <img alt="Equipos generados" width="520" src="./semana05_imagenes/equipos-generados.png" />
</div>

---

# ✅ Conclusiones

En esta semana aprendí cómo **Node.js y npm** forman la base del ecosistema JavaScript. npm permite instalar y gestionar librerías, lo que hace que cualquier proyecto sea más flexible y poderoso.  

Con **React** entendí cómo los componentes y los hooks hacen más simple y modular el desarrollo de interfaces modernas. Descubrí también que **Vite** es mucho más rápido que CRA y muy recomendable para proyectos nuevos. Por otro lado, **Next.js** lleva a React a un nivel superior con optimización, SEO y renderizado del lado del servidor.  

La **Práctica Calificada 3** me ayudó a aplicar JavaScript puro para construir aplicaciones interactivas como una ruleta y un sorteo de equipos. Con esto reforcé mis conocimientos de manipulación del DOM, eventos, localStorage y lógica de programación.  

En conclusión, esta semana me dejó claro que tengo una caja de herramientas muy amplia: Node.js y npm como base, React y Vite para desarrollo ágil, Next.js para proyectos profesionales y JS puro para entender cómo funcionan las cosas desde la raíz.

---

<p align="center">
✨ Elaborado por <b>Macha Pariona Angel Yoelver</b> · Cuaderno Digital — Semana 05 ✨
</p>
