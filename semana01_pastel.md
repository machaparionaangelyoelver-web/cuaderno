<!-- Encabezado animado en tonos pastel (sin 'cuaderno digital') -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=soft&height=140&color=0:FDE68A,100:FBCFE8&text=%F0%9F%93%95%20Bit%C3%A1cora%20de%20Aprendizaje%20%E2%80%94%20Semana%2001&fontAlign=50&fontAlignY=35&fontSize=30&fontColor=334155&desc=Fundamentos%20de%20la%20Tecnolog%C3%ADa%20Web&descAlign=50&descAlignY=65&animation=fadeIn" alt="Encabezado animado Semana 01" />
</p>

<!-- Título con efecto 'typing' -->
<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=22&duration=2400&pause=900&center=true&vCenter=true&width=920&lines=IS093%20%E2%80%94%20Desarrollo%20de%20Aplicaciones%20Web;Estudiante%3A%20Macha%20Pariona%20Angel%20Yoelver;Docente%3A%20Mg.%20Jaime%20Suasn%C3%A1bar%20Terrel" alt="Typing header" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Semana-01-fde68a?style=for-the-badge&labelColor=fbcfe8">
  <img src="https://img.shields.io/badge/Estado-En%20curso-a7f3d0?style=for-the-badge&labelColor=f5d0fe">
  <img src="https://img.shields.io/badge/Portafolio-GitHub%20Pages-93c5fd?style=for-the-badge&labelColor=ffe4e6">
</p>

---

## 🧭 Índice
- [Resumen breve](#resumen-breve)
- [Temas aprendidos](#temas-aprendidos)
- [Laboratorio y evidencias (imágenes de internet)](#laboratorio-y-evidencias-im%C3%A1genes-de-internet)
- [Tablas rápidas](#tablas-r%C3%A1pidas)
- [Diagramas Mermaid](#diagramas-mermaid)
- [Reflexión](#reflexi%C3%B3n)
- [Bibliografía](#bibliograf%C3%ADa)

---

## Resumen breve
> Semana 01. Entendí **cómo funciona la Web** y por qué los **estándares abiertos** (HTTP, HTML, CSS, JavaScript y Web APIs) permiten que cualquier navegador y servidor se entiendan. A nivel de infraestructura, repasé **DNS** y la **arquitectura cliente‑servidor**. Organicé mi **portafolio en GitHub Pages** para evidenciar prácticas y reflexiones.

---

## Temas aprendidos
- **Ecosistema base:** HTTP/HTTPS, HTML, CSS, JS y Web APIs.  
- **Open Web Platform:** principios de independencia, transparencia y documentación abierta.  
- **DNS:** traduce dominios (ej. `www.uncp.edu.pe`) a direcciones IP.  
- **Frontend vs Backend:** interfaz/experiencia vs. lógica/datos/seguridad.  
- **Herramientas:** Visual Studio Code, Git, GitHub Pages, Emmet, Codespaces.  

**Errores que evité**
- Mezclar estructura y estilos → separé HTML semántico y presentación.  
- No versionar cambios → usé `git add/commit/push` con mensajes claros.  
- No documentar → registré evidencias en el portafolio.

---

## Laboratorio y evidencias (imágenes de internet)
> Coloco referencias visuales **de internet** (no locales) que representan lo trabajado.

**Figura 1. Arquitectura cliente‑servidor**  
![Arquitectura cliente-servidor](https://upload.wikimedia.org/wikipedia/commons/thumb/c/c9/Client-server-model.svg/640px-Client-server-model.svg.png)

**Figura 2. Diagrama DNS**  
![DNS Diagram](https://www.cloudflare.com/img/learning/dns/what-is-dns/dns-diagram.png)

**Figura 3. Visual Studio Code — Interfaz**  
![VS Code UI](https://code.visualstudio.com/assets/docs/getstarted/userinterface/vscode-ui.png)

**Figura 4. GitHub Pages — Panel de ayuda**  
![GitHub Pages](https://docs.github.com/assets/cb-20364/images/help/pages/pages-home.png)

---

## Tablas rápidas

**Estándares y recursos**
| Área | Recurso | Descripción | Enlace |
|---|---|---|---|
| Protocolo | HTTP/HTTPS | Transporte de documentos hipermedia | https://httpwg.org/specs/ |
| Marcado | HTML (WHATWG) | Estructura semántica | https://html.spec.whatwg.org/ |
| Estilos | CSS (W3C) | Presentación y layout | https://www.w3.org/Style/CSS/Overview.en.html |
| APIs | Web APIs (MDN) | DOM, Fetch, Storage, etc. | https://developer.mozilla.org/en-US/docs/Web/API |
| Gráficos | WebGL (MDN) | 3D con `<canvas>` | https://developer.mozilla.org/en-US/docs/Web/API/WebGL_API/Tutorial |
| Accesibilidad | WAI‑ARIA | Roles/props accesibles | https://www.w3.org/TR/html-aria/ |

**Frontend vs Backend**
| Aspecto | Frontend | Backend |
|---|---|---|
| Lenguajes | HTML, CSS, JS/TS | Python, Node.js, Java, PHP |
| Frameworks | React, Vue, Angular | Django, Express, Spring, Laravel |
| Foco | UX, accesibilidad, rendimiento | Seguridad, escalado, datos |
| Entrega | CSR/SSR/SSG, CDN | APIs, microservicios, colas |

**Checklist Lab 01**
| Ítem | Hecho | Nota |
|---|:--:|---|
| Configuré VS Code y extensiones | ☐ |  |
| Probé Emmet y snippets | ☐ |  |
| Repo creado + primer commit | ☐ |  |
| Activé GitHub Pages | ☐ |  |
| Registré evidencias | ☐ |  |

---

## Diagramas Mermaid

**Flujo de petición web**
```mermaid
sequenceDiagram
  participant U as Usuario
  participant B as Navegador
  participant D as DNS
  participant S as Servidor Web
  participant API as Backend/API
  participant DB as Base de Datos

  U->>B: Ingresa URL
  B->>D: Resolver dominio
  D-->>B: IP del servidor
  B->>S: HTTP GET /
  S->>API: Lógica de negocio
  API->>DB: Consulta/Actualiza
  DB-->>API: Respuesta
  API-->>S: HTML/JSON
  S-->>B: 200 OK
  B-->>U: Renderiza página
```

**Arquitectura (alto nivel)**
```mermaid
flowchart LR
  A[Cliente/Frontend] -->|HTTPS| G(API Gateway)
  G --> B[(Auth)]
  G --> C[Servicio Usuarios]
  G --> D[Servicio Productos]
  G --> E[(DB SQL/NoSQL)]
  G --> F[(Cache/CDN)]
  G --> H[Logs/Monitoreo]
```

---

## Reflexión
> Aprendí a **fundamentar** lo que hago: estándares, DNS, cliente/servidor y control de versiones. Publicar en **GitHub Pages** me obligó a documentar y a cuidar accesibilidad y rendimiento desde el inicio. Para la siguiente semana, reforzaré **ARIA** y mediré **LCP/CLS** para mejorar tiempos y estabilidad visual.

---

## Bibliografía
- WHATWG · HTML Living Standard — https://html.spec.whatwg.org/  
- W3C · CSS Overview — https://www.w3.org/Style/CSS/Overview.en.html  
- HTTPWG · Especificaciones — https://httpwg.org/specs/  
- MDN · Web APIs — https://developer.mozilla.org/en-US/docs/Web/API  
- Cloudflare · ¿Qué es DNS? — https://www.cloudflare.com/learning/dns/what-is-dns/  
- Emmet · Cheat Sheet — https://docs.emmet.io/cheat-sheet/  
- GitHub Pages · Quickstart — https://docs.github.com/en/pages/quickstart

<!-- Pie animado pastel -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=soft&height=110&color=0:FBCFE8,100:A7F3D0&section=footer&animation=fadeIn" alt="Footer pastel" />
</p>
