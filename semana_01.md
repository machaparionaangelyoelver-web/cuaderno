<!-- ========================================================= -->
<!-- 🪐 HERO OSCURO con animaciones de typing (se renderiza en GitHub/MD con HTML embebido) -->
<!-- ========================================================= -->

<div align="center" style="background: linear-gradient(135deg,#0b0e19 0%, #121433 45%, #541a63 85%, #8a107e 100%); padding: 32px 16px; border-radius: 18px; color: #eaeaf2;">

  <!-- Título animado -->
  <a href="https://git.io/typing-svg">
    <img src="https://readme-typing-svg.herokuapp.com?color=EAEAF2&size=32&center=true&vCenter=true&width=900&lines=📘+Cuaderno+Digital+—+Semana+01;Fundamentos+de+la+Tecnolog%C3%ADa+Web" alt="Typing: Cuaderno Digital — Semana 01"/>
  </a>

  <!-- Nombre + Laboratorio animados -->
  <br/>
  <a href="https://git.io/typing-svg">
    <img src="https://readme-typing-svg.herokuapp.com?color=B8F5FF&size=20&center=true&vCenter=true&width=900&lines=👨‍🎓+Estudiante:+Macha+Pariona+Angel+Yoelver;💻+Laboratorio:+Git+Bash+%2B+Visual+Studio+Code" alt="Typing: Nombre y Laboratorio"/>
  </a>

  <p style="max-width: 880px; margin: 14px auto 0; line-height: 1.5; opacity:.95">
    Semana de introducción con enfoque en estándares Web, arquitectura cliente–servidor, herramientas de desarrollo y control de versiones con Git/GitHub. Editor base: VS Code + extensiones.
  </p>

  <p>
    <a href="#contenido" style="background:#f511c9;padding:10px 22px;border-radius:24px;color:#fff;text-decoration:none;font-weight:700">Ir al contenido</a>
    <a href="#recursos" style="background:#ffffff1a;padding:10px 22px;border-radius:24px;color:#fff;text-decoration:none;">Recursos</a>
    <a href="https://github.com/" style="background:#fff;padding:10px 22px;border-radius:24px;color:#121433;text-decoration:none;font-weight:800">Informe 01</a>
  </p>
</div>

<p align="center">🌌 ✨ 🚀 ✨ 🌌</p>

<!-- Badges -->
<p align="center">
  <img src="https://img.shields.io/badge/HTML5-%230b0e19?logo=html5&logoColor=E44D26&labelColor=1f233e&style=for-the-badge"/>
  <img src="https://img.shields.io/badge/CSS3-%230b0e19?logo=css3&logoColor=1572B6&labelColor=1f233e&style=for-the-badge"/>
  <img src="https://img.shields.io/badge/JavaScript-%230b0e19?logo=javascript&logoColor=F7DF1E&labelColor=1f233e&style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Git-%230b0e19?logo=git&logoColor=F05032&labelColor=1f233e&style=for-the-badge"/>
  <img src="https://img.shields.io/badge/VS%20Code-%230b0e19?logo=visualstudiocode&logoColor=22A7F2&labelColor=1f233e&style=for-the-badge"/>
</p>

---

## 📚 Índice
1. [Objetivos de aprendizaje](#objetivos-de-aprendizaje)
2. [Conceptos clave](#conceptos-clave)
3. [Arquitectura Web moderna (SVG)](#arquitectura-web-moderna-svg)
4. [Cómo funciona el DNS (SVG)](#cómo-funciona-el-dns-svg)
5. [Frontend vs Backend](#frontend-vs-backend)
6. [Laboratorio 01: Git Bash + VS Code](#laboratorio-01-git-bash--vs-code)
7. [Línea del tiempo de la Web](#línea-del-tiempo-de-la-web)
8. [Ejercicio práctico guiado](#ejercicio-práctico-guiado)
9. [Checklist de la semana](#checklist-de-la-semana)
10. [Glosario mínimo](#glosario-mínimo)
11. [Autoevaluación](#autoevaluación)
12. [Rúbrica breve de entrega](#rúbrica-breve-de-entrega)
13. [Reflexión personal](#reflexión-personal)
14. [Recursos](#recursos)

---

## 🎯 Objetivos de aprendizaje
- Diferenciar **Frontend** (presentación) de **Backend** (lógica/datos).
- Explicar el flujo **cliente → servidor** con **HTTP/HTTPS**.
- Ejecutar un flujo básico de **Git**: `init → add → commit → push`.
- Configurar **VS Code** con **Emmet** y **extensiones** útiles.
- Entender la **Open Web Platform** y por qué los estándares importan.

---

## 🧠 Conceptos clave
| Concepto | Descripción breve | Ejemplo |
|---|---|---|
| **HTML** | Estructura del contenido. | Títulos, párrafos, tablas, formularios. |
| **CSS** | Estilos y diseño. | Grid, Flexbox, variables, media queries. |
| **JS** | Interactividad y lógica en el navegador. | Validación de formularios, fetch a APIs. |
| **HTTP/HTTPS** | Protocolo de transferencia; HTTPS cifra la comunicación. | `GET /api/productos` con respuesta `200 OK`. |
| **API REST** | Interfaz de comunicación basada en recursos y métodos HTTP. | `POST /ventas`, `DELETE /clientes/{id}`. |
| **DNS** | Traduce dominios a direcciones IP. | `midominio.com` → `203.0.113.10`. |
| **Open Web Platform** | Conjunto de estándares abiertos para la Web. | HTML5, CSS3, ES6+, Web APIs. |

---

## 🏗️ Arquitectura Web moderna (SVG)
> SVG embebido (sin depender de imágenes externas). Se ve en GitHub/Markdown que permita HTML.

<div align="center">

<svg width="880" height="420" viewBox="0 0 880 420" xmlns="http://www.w3.org/2000/svg" style="max-width:100%;background:#0b0e19;border:1px solid #24283f;border-radius:12px;box-shadow:0 8px 24px rgba(0,0,0,.35)">
  <style>
    .cap{font:700 13px Inter, Arial; fill:#eaeaf2}
    .tx{font:12px Inter, Arial; fill:#cbd5e1}
    .bx1{fill:#141935;stroke:#34406a;stroke-width:2}
    .bx2{fill:#161e3d;stroke:#4b2b74;stroke-width:2}
    .bx3{fill:#132335;stroke:#1e5166;stroke-width:2}
    .ln{stroke:#8a9cc3;stroke-width:2;marker-end:url(#m)}
  </style>
  <defs>
    <marker id="m" markerWidth="10" markerHeight="10" refX="9" refY="3" orient="auto">
      <path d="M0,0 L0,6 L9,3 z" fill="#8a9cc3"/>
    </marker>
  </defs>

  <!-- Presentación -->
  <rect class="bx1" x="30" y="28" width="820" height="90" rx="12"/>
  <text class="cap" x="45" y="55">Presentación / Cliente</text>
  <text class="tx"  x="45" y="78">Navegador • SPA/SSR • HTML • CSS • JS • Accesibilidad • Caché • Service Worker</text>

  <!-- Aplicación -->
  <rect class="bx2" x="30" y="140" width="820" height="120" rx="12"/>
  <text class="cap" x="45" y="168">Aplicación / APIs</text>
  <text class="tx"  x="45" y="190">Servidor Web • API REST/GraphQL • Autenticación • Control de acceso • Rate limiting • Logs</text>
  <rect class="bx2" x="540" y="170" width="140" height="70" rx="10"/>
  <text class="tx" x="550" y="195">WebSockets</text>
  <text class="tx" x="550" y="215">Jobs / Queues</text>
  <rect class="bx2" x="700" y="170" width="140" height="70" rx="10"/>
  <text class="tx" x="710" y="195">CDN / Edge</text>
  <text class="tx" x="710" y="215">Load Balancer</text>

  <!-- Datos -->
  <rect class="bx3" x="30" y="280" width="820" height="110" rx="12"/>
  <text class="cap" x="45" y="308">Datos</text>
  <text class="tx"  x="45" y="330">SQL (MySQL/PostgreSQL) • NoSQL (Mongo) • Cache (Redis) • Almacenamiento (S3) • Analytics</text>
  <rect class="bx3" x="540" y="300" width="140" height="70" rx="10"/>
  <text class="tx" x="550" y="325">Data Lake</text>
  <text class="tx" x="550" y="345">Warehouse/BI</text>

  <!-- Líneas -->
  <line class="ln" x1="440" y1="118" x2="440" y2="140"/>
  <line class="ln" x1="440" y1="260" x2="440" y2="280"/>
  <line class="ln" x1="610" y1="240" x2="610" y2="300"/>
  <line class="ln" x1="770" y1="240" x2="770" y2="300"/>
</svg>

</div>

---

## 🌐 Cómo funciona el DNS (SVG)
<div align="center">

<svg width="820" height="360" viewBox="0 0 820 360" xmlns="http://www.w3.org/2000/svg" style="max-width:100%;background:#0b0e19;border:1px solid #24283f;border-radius:12px;box-shadow:0 8px 24px rgba(0,0,0,.35)">
  <style>
    .box{fill:#121a3a;stroke:#36417a;stroke-width:2}
    .title{font:700 14px Inter, Arial; fill:#eaeaf2}
    .text{font:12px Inter, Arial; fill:#cbd5e1}
    .arrow{stroke:#9f7aea;stroke-width:2;marker-end:url(#a)}
    .arrow2{stroke:#22d3ee;stroke-width:2;marker-end:url(#a)}
  </style>
  <defs>
    <marker id="a" markerWidth="10" markerHeight="10" refX="9" refY="3" orient="auto">
      <path d="M0,0 L0,6 L9,3 z" fill="#9f7aea"/>
    </marker>
  </defs>

  <rect class="box" x="30"  y="40"  width="200" height="70" rx="12"/>
  <text class="title" x="40" y="62">Navegador</text>
  <text class="text"  x="40" y="82">www.ejemplo.com</text>

  <rect class="box" x="290" y="20"  width="220" height="70" rx="12"/>
  <text class="title" x="300" y="42">Resolutor (ISP)</text>
  <text class="text"  x="300" y="62">Caché DNS</text>

  <rect class="box" x="560" y="20"  width="230" height="70" rx="12"/>
  <text class="title" x="570" y="42">Servidor Raíz</text>
  <text class="text"  x="570" y="62">Indica TLD</text>

  <rect class="box" x="560" y="120" width="230" height="70" rx="12"/>
  <text class="title" x="570" y="142">Servidor TLD (.com)</text>
  <text class="text"  x="570" y="162">Indica autoritativo</text>

  <rect class="box" x="290" y="230" width="220" height="70" rx="12"/>
  <text class="title" x="300" y="252">DNS Autoritativo</text>
  <text class="text"  x="300" y="272">Responde IP</text>

  <rect class="box" x="30"  y="240" width="200" height="70" rx="12"/>
  <text class="title" x="40" y="262">Servidor Web</text>
  <text class="text"  x="40" y="282">203.0.113.10</text>

  <!-- Flechas -->
  <line class="arrow"  x1="230" y1="75" x2="290" y2="55"/>
  <line class="arrow"  x1="510" y1="55" x2="560" y2="55"/>
  <line class="arrow"  x1="675" y1="90" x2="675" y2="120"/>
  <line class="arrow"  x1="560" y1="155" x2="510" y2="265"/>
  <line class="arrow2" x1="290" y1="265" x2="230" y2="275"/>

  <!-- Pasos -->
  <text class="text" x="250" y="45">1. Consulta</text>
  <text class="text" x="520" y="40">2. Raíz</text>
  <text class="text" x="688" y="112">3. TLD</text>
  <text class="text" x="522" y="210">4. Autoritativo</text>
  <text class="text" x="115" y="225">5. Conexión HTTPS</text>
</svg>

</div>

---

## 🧭 Frontend vs Backend
| Aspecto | Frontend | Backend |
|---|---|---|
| Lenguajes | HTML, CSS, JS | Python, Node.js, Java, PHP |
| Propósito | UI/UX, accesibilidad, interacción | Lógica de negocio, seguridad, datos |
| Frameworks | React, Vue, Angular | Flask/Django, Express, Spring |
| Pruebas | Lighthouse, Jest, Playwright | Unit tests, integración, Postman |
| Despliegue | Vercel, Netlify, GitHub Pages | VPS, Docker, PaaS, Kubernetes |

---

## 🔧 Laboratorio 01: Git Bash + VS Code
**Comandos base (tabla resumen)**

| Acción | Comando |
|---|---|
| Iniciar repo | `git init` |
| Ver estado | `git status` |
| Agregar cambios | `git add .` |
| Commit | `git commit -m "mensaje"` |
| Conectar remoto | `git remote add origin <URL>` |
| Enviar cambios | `git push -u origin main` |
| Crear rama | `git checkout -b feature/ui` |
| Mezclar | `git merge feature/ui` |
| Clonar | `git clone <URL>` |

**Snippets útiles (Emmet)**
- `!` → boilerplate HTML5  
- `ul>li*5` → lista con 5 elementos  
- `.card>h3.title+p.text` → bloque de tarjeta con título + párrafo

**VS Code (sugerencias)**
- Extensiones: *ESLint*, *Prettier*, *Live Server*, *GitLens*.  
- Atajos: `Ctrl+Shift+P` (paleta), `Alt+Shift+F` (formatear).

---

## ⏳ Línea del tiempo de la Web
| Año | Hito |
|---|---|
| 1989–1991 | Nace la Web y el primer sitio público. |
| 1995 | JavaScript + auge del modelo cliente–servidor. |
| 2008 | HTML5 toma forma como estándar. |
| 2015 | ES6 moderniza el lenguaje JS. |
| 2020+ | React/Next/Vue dominan el frontend moderno. |

---

## 🧪 Ejercicio práctico guiado
1. Crea una carpeta `portafolio-semana01` y dentro `index.html`, `styles.css`, `app.js`.  
2. En `index.html`, estructura mínima:
   ```html
   <!doctype html>
   <html lang="es">
   <head>
     <meta charset="utf-8">
     <meta name="viewport" content="width=device-width,initial-scale=1">
     <title>Portafolio · Semana 01</title>
     <link rel="stylesheet" href="styles.css">
   </head>
   <body>
     <header class="hero">
       <h1>Mi primera página</h1>
       <p>HTML + CSS + JS</p>
     </header>
     <main>
       <section id="about"><h2>Sobre mí</h2><p>…</p></section>
       <section id="lab"><h2>Laboratorio</h2><p>…</p></section>
     </main>
     <script src="app.js"></script>
   </body>
   </html>

