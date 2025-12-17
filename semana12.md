<!-- ======================================================================
      📗 CUADERNO DIGITAL — SEMANA 12
      Backend con PHP • MySQL • Composer • Postman • Evidencias
====================================================================== -->

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&height=160&color=0:7C3AED,50:22D3EE,100:D946EF&text=📗%20Cuaderno%20Digital%20—%20Semana%2012&fontAlign=50&fontAlignY=35&fontSize=36&fontColor=ffffff&animation=fadeIn" />
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/7fa4a9c04448511e1ca1aae80c2901fc3eedca56/semana12_imagenes/logo_uncp.png" width="90" alt="Logo UNCP" style="margin:10px;">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/7fa4a9c04448511e1ca1aae80c2901fc3eedca56/semana12_imagenes/logo_fis.png" width="90" alt="Logo FIS" style="margin:10px;">
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/7fa4a9c04448511e1ca1aae80c2901fc3eedca56/semana12_imagenes/logo_php.png" width="70" alt="PHP" style="margin:6px;">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/7fa4a9c04448511e1ca1aae80c2901fc3eedca56/semana12_imagenes/logo_mysql.png" width="70" alt="MySQL" style="margin:6px;">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/7fa4a9c04448511e1ca1aae80c2901fc3eedca56/semana12_imagenes/logo_apache.png" width="70" alt="Apache" style="margin:6px;">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/7fa4a9c04448511e1ca1aae80c2901fc3eedca56/semana12_imagenes/logo_composer.png" width="70" alt="Composer" style="margin:6px;">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/7fa4a9c04448511e1ca1aae80c2901fc3eedca56/semana12_imagenes/logo_postman.png" width="70" alt="Postman" style="margin:6px;">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/7fa4a9c04448511e1ca1aae80c2901fc3eedca56/semana12_imagenes/logo_vscode.png" width="70" alt="VS Code" style="margin:6px;">
</p>

<p align="center">
  <img
    alt="Macha Pariona Angel Yoelver — Desarrollo de Aplicaciones Web — Semana 12"
    src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=24&duration=2800&pause=1000&color=22D3EE&center=true&vCenter=true&width=980&lines=Macha%20Pariona%20Angel%20Yoelver;Curso%3A%20Desarrollo%20de%20Aplicaciones%20Web;Tema%3A%20Backend%20con%20PHP%20%2B%20MySQL%20(Semana%2012);Evidencias%3A%20Composer%20%7C%20PDO%20%7C%20Prepared%20Statements%20%7C%20Postman"
  />
</p>

---

## 📌 Datos generales

- **Autor:** Macha Pariona Angel Yoelver  
- **Curso:** Desarrollo de Aplicaciones Web  
- **Semana:** 12  
- **Tema:** Backend con PHP + MySQL (CRUD + validación + pruebas)  
- **Repositorio de evidencias (carpeta pública):** https://github.com/machaparionaangelyoelver-web/fotosdecuaderno/tree/7fa4a9c04448511e1ca1aae80c2901fc3eedca56/semana12_imagenes

---

## 1. Introducción

En esta semana se desarrolló el concepto de **backend** como la capa que recibe peticiones (HTTP), aplica **reglas de negocio**, valida entradas y se comunica con una base de datos para retornar respuestas claras (generalmente en **JSON**).  

Se trabajó un backend con **PHP** conectado a **MySQL**, priorizando:

- **Persistencia de datos** (CRUD).
- **Validación** antes de guardar (calidad e integridad).
- **Seguridad mínima** mediante **PDO** y **prepared statements**.
- **Pruebas de endpoints** con **Postman** para verificar códigos HTTP y respuestas.

---

## 2. Objetivos

### 2.1 Objetivo general
Implementar un backend funcional en PHP conectado a MySQL que permita gestionar registros mediante operaciones CRUD, con validaciones y pruebas de funcionamiento.

### 2.2 Objetivos específicos
- Configurar el entorno local (Apache/PHP) y herramientas de apoyo (Composer, editor).
- Definir la base de datos y la tabla principal (campos + restricciones).
- Implementar endpoints CRUD (Create, Read, Update, Delete).
- Aplicar validaciones y manejo de errores con códigos HTTP.
- Registrar evidencias mediante pruebas en Postman y capturas del proceso.

---

## 3. Conceptos clave

- **Backend:** capa responsable de procesar y controlar el acceso a datos.  
- **API (REST básica):** interfaz que expone rutas/endpoints para operaciones.  
- **CRUD:** operaciones principales sobre datos (Crear, Leer, Actualizar, Eliminar).  
- **PDO:** estándar de conexión a BD en PHP, con control de errores y compatibilidad.  
- **Prepared Statements:** separan consulta y datos, reduciendo el riesgo de inyección SQL.  
- **Códigos HTTP:** comunican el estado del resultado (200/201, 400, 404, 500).  
- **Postman:** herramienta para validar endpoints y generar evidencia de respuestas.

---

## 4. Stack y herramientas

| Componente | Uso |
|---|---|
| PHP | Lógica del backend y endpoints |
| MySQL | Persistencia y consultas de datos |
| Apache (XAMPP/Laragon) | Servidor local |
| Composer | Gestión de dependencias (si aplica) |
| Postman | Pruebas de API y evidencia de respuestas |
| VS Code / IntelliJ | Edición y organización del proyecto |

---

## 5. Flujo de trabajo realizado

1) **Entorno local listo:** servidor, rutas y ejecución de PHP.  
2) **Base de datos creada:** estructura y restricciones necesarias.  
3) **Proyecto organizado:** carpetas claras y archivos por responsabilidad.  
4) **Endpoints CRUD:** rutas para gestionar datos.  
5) **Validación y errores:** respuestas consistentes según el caso.  
6) **Pruebas con Postman:** confirmación funcional + capturas para evidencias.

---

## 6. Evidencias

> Las siguientes capturas están alojadas públicamente en GitHub y se insertan directamente desde la ruta *raw*.


<details>
  <summary><b>Evidencia 01 — Instalación/entorno</b> — Servidor local listo (Apache/PHP) y verificación de ejecución.</summary>

  <p align="center">
    <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/7fa4a9c04448511e1ca1aae80c2901fc3eedca56/semana12_imagenes/evid_01_instalacion_entorno.png" alt="Evidencia 01 — Instalación/entorno" style="max-width: 100%; border-radius: 14px;" />
  </p>
</details>


<details>
  <summary><b>Evidencia 02 — Versiones (PHP/Composer)</b> — Comprobación de versiones para asegurar compatibilidad del proyecto.</summary>

  <p align="center">
    <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/7fa4a9c04448511e1ca1aae80c2901fc3eedca56/semana12_imagenes/evid_02_versiones_php_composer.png" alt="Evidencia 02 — Versiones (PHP/Composer)" style="max-width: 100%; border-radius: 14px;" />
  </p>
</details>


<details>
  <summary><b>Evidencia 03 — Creación del proyecto</b> — Estructura inicial del proyecto y carpetas base.</summary>

  <p align="center">
    <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/7fa4a9c04448511e1ca1aae80c2901fc3eedca56/semana12_imagenes/evid_03_creacion_proyecto.png" alt="Evidencia 03 — Creación del proyecto" style="max-width: 100%; border-radius: 14px;" />
  </p>
</details>


<details>
  <summary><b>Evidencia 04 — Configuración .env</b> — Parámetros de conexión/entorno separados del código.</summary>

  <p align="center">
    <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/7fa4a9c04448511e1ca1aae80c2901fc3eedca56/semana12_imagenes/evid_04_env_config.png" alt="Evidencia 04 — Configuración .env" style="max-width: 100%; border-radius: 14px;" />
  </p>
</details>


<details>
  <summary><b>Evidencia 05 — BD y tabla (MySQL)</b> — Creación de base de datos/tabla principal y preparación para CRUD.</summary>

  <p align="center">
    <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/7fa4a9c04448511e1ca1aae80c2901fc3eedca56/semana12_imagenes/evid_05_migraciones_bd.png" alt="Evidencia 05 — BD y tabla (MySQL)" style="max-width: 100%; border-radius: 14px;" />
  </p>
</details>


<details>
  <summary><b>Evidencia 06 — Postman (GET)</b> — Consulta de registros y validación de respuesta JSON.</summary>

  <p align="center">
    <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/7fa4a9c04448511e1ca1aae80c2901fc3eedca56/semana12_imagenes/evid_06_postman_get.png" alt="Evidencia 06 — Postman (GET)" style="max-width: 100%; border-radius: 14px;" />
  </p>
</details>


<details>
  <summary><b>Evidencia 07 — Postman (POST/PUT/DELETE)</b> — Pruebas de creación, actualización y eliminación con códigos HTTP.</summary>

  <p align="center">
    <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/7fa4a9c04448511e1ca1aae80c2901fc3eedca56/semana12_imagenes/evid_07_postman_post_put_delete.png" alt="Evidencia 07 — Postman (POST/PUT/DELETE)" style="max-width: 100%; border-radius: 14px;" />
  </p>
</details>


<details>
  <summary><b>Evidencia 08 — Validaciones y errores</b> — Respuestas controladas (400/404/500) y mensajes claros.</summary>

  <p align="center">
    <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/7fa4a9c04448511e1ca1aae80c2901fc3eedca56/semana12_imagenes/evid_08_validaciones_errores.png" alt="Evidencia 08 — Validaciones y errores" style="max-width: 100%; border-radius: 14px;" />
  </p>
</details>


<details>
  <summary><b>Evidencia 09 — Estructura del proyecto</b> — Organización de carpetas/archivos del backend.</summary>

  <p align="center">
    <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/7fa4a9c04448511e1ca1aae80c2901fc3eedca56/semana12_imagenes/evid_09_estructura_proyecto.png" alt="Evidencia 09 — Estructura del proyecto" style="max-width: 100%; border-radius: 14px;" />
  </p>
</details>


<details>
  <summary><b>Evidencia 10 — Resultados finales</b> — Backend operando con evidencias completas del flujo.</summary>

  <p align="center">
    <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/7fa4a9c04448511e1ca1aae80c2901fc3eedca56/semana12_imagenes/evid_10_resultados_finales.png" alt="Evidencia 10 — Resultados finales" style="max-width: 100%; border-radius: 14px;" />
  </p>
</details>


---

## 7. Estructura de carpeta (según evidencias)

```text
semana12_imagenes/
├─ evid_01_instalacion_entorno.png
├─ evid_02_versiones_php_composer.png
├─ evid_03_creacion_proyecto.png
├─ evid_04_env_config.png
├─ evid_05_migraciones_bd.png
├─ evid_06_postman_get.png
├─ evid_07_postman_post_put_delete.png
├─ evid_08_validaciones_errores.png
├─ evid_09_estructura_proyecto.png
├─ evid_10_resultados_finales.png
├─ lista.txt
├─ logo_apache.png
├─ logo_composer.png
├─ logo_fis.png
├─ logo_intellij.png
├─ logo_laravel.png
├─ logo_mysql.png
├─ logo_php.png
├─ logo_postman.png
├─ logo_uncp.png
└─ logo_vscode.png
```

---

## 8. KPIs simples (verificación rápida)

- **Endpoints probados:** 4 (GET, POST, PUT, DELETE)  
- **Códigos HTTP verificados:** 200/201, 400, 404, 500  
- **Evidencias registradas:** 10 capturas del flujo completo  

---

## 9. Conclusiones

- Se consolidó el **rol del backend** como “controlador” del sistema: valida entradas, procesa lógica y protege datos antes de guardar.  
- El uso de **PDO + prepared statements** aporta una base segura y profesional para cualquier API en PHP, reduciendo riesgos comunes como la inyección SQL.  
- **Postman** permitió comprobar el comportamiento real de los endpoints y documentar evidencias de los resultados, facilitando depuración y presentación del trabajo.

---

## 10. Enlace rápido

- **Carpeta de imágenes (GitHub):** https://github.com/machaparionaangelyoelver-web/fotosdecuaderno/tree/7fa4a9c04448511e1ca1aae80c2901fc3eedca56/semana12_imagenes

---

<p align="center"><sub>Hecho por Angel Yoelver Macha · UNCP — Semana 12 (Backend con PHP + MySQL)</sub></p>
