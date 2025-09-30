# 📘 Cuaderno Digital — Semana 01

<div align="center">

<img src="https://raw.githubusercontent.com/Aakarsh-B/trying-repos/master/Technology.gif" width="100%" alt="Banner Tecnologías Web">

<a href="https://git.io/typing-svg">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=700&size=34&duration=2800&pause=600&center=true&vCenter=true&width=900&height=60&color=FFFFFF&background=0B0E19&lines=📘+Cuaderno+Digital+—+Semana+01;Fundamentos+de+la+Tecnolog%C3%ADa+Web" alt="Cuaderno Digital — Semana 01">
</a>

<br/>
<a href="https://git.io/typing-svg">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=600&size=20&duration=2800&pause=600&center=true&vCenter=true&width=900&height=40&color=9BE1FF&background=0B0E19&lines=👨‍🎓+Estudiante:+Angel+Yoelver+Macha+Pariona;🎓+Semestre:+Noveno+Semestre;💻+Laboratorio:+Git+Bash+%2B+Visual+Studio+Code" alt="Nombre y semestre">
</a>

</div>

<p align="center">🌌 ✨ 🚀 ✨ 🌌</p>

<p align="center">
  <img src="https://img.shields.io/badge/HTML5-0B0E19?logo=html5&logoColor=E44D26&labelColor=1B1936&style=for-the-badge"/>
  <img src="https://img.shields.io/badge/CSS3-0B0E19?logo=css3&logoColor=1572B6&labelColor=1B1936&style=for-the-badge"/>
  <img src="https://img.shields.io/badge/JavaScript-0B0E19?logo=javascript&logoColor=F7DF1E&labelColor=1B1936&style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Git-0B0E19?logo=git&logoColor=F05032&labelColor=1B1936&style=for-the-badge"/>
  <img src="https://img.shields.io/badge/VS%20Code-0B0E19?logo=visualstudiocode&logoColor=22A7F2&labelColor=1B1936&style=for-the-badge"/>
</p>

---

## 🎯 Objetivos de aprendizaje
- Diferenciar **Frontend** (presentación) de **Backend** (lógica y datos).  
- Explicar el flujo **cliente → servidor** con **HTTP/HTTPS**.  
- Ejecutar un flujo básico de **Git**: `init → add → commit → push`.  
- Configurar **VS Code** con **Emmet** y extensiones útiles.  
- Comprender la **Open Web Platform** y su importancia.

![Arquitectura cliente servidor](https://miro.medium.com/v2/resize:fit:1200/1*eKfdQmQh5iJoz0oFvPOg0Q.png)

---

## 🧠 Conceptos clave

| Concepto | Descripción | Ejemplo |
|---|---|---|
| **HTML** | Estructura del contenido web. | Títulos, párrafos, formularios. |
| **CSS** | Estilos y diseño visual. | Grid, Flexbox, variables. |
| **JavaScript** | Interactividad y lógica en el navegador. | Validar formularios, consumir APIs. |
| **HTTP/HTTPS** | Transporte de datos; HTTPS cifra y autentica. | `GET /api/productos` → `200 OK`. |
| **API REST** | Interfaz basada en recursos y métodos HTTP. | `POST /ventas`. |
| **DNS** | Traduce dominios a IPs. | `midominio.com` → `203.0.113.10`. |
| **Open Web Platform** | Estándares abiertos de la Web. | HTML5, CSS3, ES6+, Web APIs. |

![DNS](https://upload.wikimedia.org/wikipedia/commons/0/0e/DNS_Server_icon.png)

---

## 🧭 Frontend vs Backend

| Aspecto | Frontend | Backend |
|---|---|---|
| Lenguajes | HTML, CSS, JS | Python, Node.js, Java, PHP |
| Propósito | UI/UX, accesibilidad, interacción | Lógica de negocio, seguridad, datos |
| Frameworks | React, Vue, Angular | Flask/Django, Express, Spring |
| Pruebas | Lighthouse, Jest | Unit tests, integración, Postman |
| Despliegue | Vercel, Netlify | VPS, Docker, Kubernetes |

![Frontend vs Backend](https://miro.medium.com/v2/resize:fit:1200/1*8ql7sHPV1lTYJxOZ1Hf9IQ.png)

---

## 🔧 Laboratorio 01: Git Bash + VS Code

**Comandos básicos**

| Acción | Comando |
|---|---|
| Iniciar repo | `git init` |
| Ver estado | `git status` |
| Agregar cambios | `git add .` |
| Commit | `git commit -m "mensaje"` |
| Conectar remoto | `git remote add origin <URL>` |
| Subir cambios | `git push -u origin main` |
| Crear rama | `git checkout -b feature/ui` |
| Mezclar | `git merge feature/ui` |
| Clonar | `git clone <URL>` |

![Git](https://git-scm.com/images/logos/downloads/Git-Icon-1788C.png)

---

## ⏳ Línea del tiempo de la Web

| Año | Hito |
|---|---|
| 1989–1991 | Nace la Web y el primer sitio público. |
| 1995 | JavaScript y auge del cliente–servidor. |
| 2008 | HTML5 toma forma como estándar. |
| 2015 | ES6 moderniza JavaScript. |
| 2020+ | React/Next/Vue dominan el frontend moderno. |

---

## 🧪 Ejercicio práctico

1. **Crea un proyecto** `portafolio-semana01`.  
   ```
   portafolio-semana01/
   ├─ index.html
   ├─ styles.css
   └─ app.js
   ```

2. **HTML base**
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
       <section id="about">
         <h2>Sobre mí</h2>
         <p>Breve descripción personal.</p>
       </section>
       <section id="lab">
         <h2>Laboratorio</h2>
         <p>Ejemplo de uso de Git y VSCode.</p>
       </section>
     </main>
     <footer>© 2025 Mi Portafolio</footer>
     <script src="app.js"></script>
   </body>
   </html>
   ```

3. **CSS oscuro**
   ```css
   :root {
     --bg: #0B0E19;
     --panel: #101225;
     --ink: #EAEAF2;
     --muted: #94A3B8;
     --accent: #F511C9;
   }
   html,body {
     margin:0; background:var(--bg); color:var(--ink);
     font:16px/1.6 ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Arial;
   }
   .hero {
     background: linear-gradient(135deg,#101225,#3B2066 55%,#8A107E);
     padding: 48px 20px; text-align: center;
   }
   h1,h2 { margin: .2em 0; }
   a { color: var(--accent); }
   main { max-width: 800px; margin: auto; padding: 20px; }
   footer { text-align:center; padding:20px; color:var(--muted); font-size:.9rem;}
   ```

4. **JavaScript simple**
   ```js
   console.log("Semana 01 lista ✨");
   document.addEventListener("DOMContentLoaded", () => {
     const about = document.querySelector("#about");
     about.insertAdjacentHTML("beforeend","<p><em>Hecho con JavaScript.</em></p>");
   });
   ```

5. **Publica** el proyecto en GitHub Pages o Vercel.  
6. Flujo Git:  
   ```bash
   git add .
   git commit -m "Semana 01"
   git push -u origin main
   ```

---

## ✅ Checklist

- [ ] Entiendo la diferencia **Frontend vs Backend**.  
- [ ] Puedo explicar **HTTP/HTTPS** y códigos 200, 301, 404, 500.  
- [ ] Hice un **commit** y un **push** a GitHub.  
- [ ] Configuré **VS Code** con extensiones útiles.  
- [ ] Comprendo el flujo básico del **DNS**.

---

## 📎 Glosario mínimo
- **SPA**: Single Page Application; la app se carga una sola vez y luego actualiza vistas dinámicamente.  
- **SSR**: Server-Side Rendering; el servidor envía HTML ya generado.  
- **REST**: Arquitectura para exponer recursos vía HTTP.  
- **CDN**: Red de entrega de contenido que acelera descargas.  
- **Cache**: Almacenamiento temporal para mejorar tiempos de respuesta.  

---

## ✨ Reflexión personal
> Esta semana entendí cómo se estructura la Web y la importancia de los estándares abiertos.  
> Aprendí el flujo cliente-servidor, el funcionamiento del DNS y la seguridad con HTTPS.  
> Practiqué **Git** para control de versiones y configuré **VS Code** con herramientas modernas para un desarrollo ágil.

---

## 📚 Recursos
- MDN Web Docs (ES): https://developer.mozilla.org/es/  
- VS Code Docs: https://code.visualstudio.com/docs  
- Git Handbook (GitHub): https://guides.github.com/introduction/git-handbook/  
