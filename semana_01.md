# 📘 Cuaderno Digital — Semana 01  
**👨‍🎓 Estudiante:** Macha Pariona Angel Yoelver  
**💻 Laboratorio:** Git Bash + Visual Studio Code  

> Semana de introducción con enfoque en estándares Web, arquitectura cliente–servidor, herramientas de desarrollo y control de versiones con Git/GitHub.  
> Tema visual: **oscuro minimalista**.

---

## 🎯 Objetivos de aprendizaje
- Diferenciar **Frontend** (presentación) de **Backend** (lógica/datos).
- Explicar el flujo **cliente → servidor** con **HTTP/HTTPS**.
- Ejecutar un flujo básico de **Git**: `init → add → commit → push`.
- Configurar **VS Code** con **Emmet** y extensiones.
- Entender la **Open Web Platform** y su importancia.

---

## 🧠 Conceptos clave

| Concepto | Descripción breve | Ejemplo |
|---|---|---|
| **HTML** | Estructura del contenido web. | Páginas con títulos, párrafos, tablas. |
| **CSS** | Estilos y diseño visual. | Grid, Flexbox, variables, media queries. |
| **JavaScript** | Interactividad y lógica en el navegador. | Validación de formularios, fetch a APIs. |
| **HTTP/HTTPS** | Protocolo de transferencia; HTTPS cifra la comunicación. | `GET /api/productos` con respuesta `200 OK`. |
| **API REST** | Interfaz para exponer recursos vía HTTP. | `POST /ventas` guarda datos. |
| **DNS** | Traduce dominios a direcciones IP. | `midominio.com` → `203.0.113.10`. |
| **Open Web Platform** | Conjunto abierto de estándares web. | HTML5, CSS3, ES6+, Web APIs. |

---

## 🧭 Frontend vs Backend

| Aspecto | Frontend | Backend |
|---|---|---|
| Lenguajes | HTML, CSS, JS | Python, Node.js, Java, PHP |
| Propósito | UI/UX, accesibilidad, interacción | Lógica de negocio, seguridad, datos |
| Frameworks | React, Vue, Angular | Flask/Django, Express, Spring |
| Pruebas | Lighthouse, Jest | Unit tests, integración, Postman |
| Despliegue | Vercel, Netlify | VPS, Docker, Kubernetes |

---

## 🔧 Laboratorio 01: Git Bash + VS Code

**Comandos base**

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

**Snippets útiles (Emmet)**  
- `!` → estructura HTML5  
- `ul>li*5` → lista con 5 ítems  
- `.card>h3.title+p.text` → bloque con título + párrafo  

**VS Code recomendado**  
- Extensiones: *ESLint*, *Prettier*, *Live Server*, *GitLens*.  
- Atajos: `Ctrl+Shift+P` (paleta), `Alt+Shift+F` (formatear).

---

## ⏳ Línea del tiempo de la Web

| Año | Hito |
|---|---|
| 1989–1991 | Nace la Web y el primer sitio público. |
| 1995 | JavaScript y auge cliente–servidor. |
| 2008 | HTML5 toma forma como estándar. |
| 2015 | ES6 moderniza JavaScript. |
| 2020+ | React/Next/Vue dominan el frontend moderno. |

---

## 🧪 Ejercicio práctico (mejorado)

1. **Crea un proyecto** `portafolio-semana01`.  
   Estructura mínima:

