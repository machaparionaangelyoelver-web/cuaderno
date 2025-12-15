# Semana 11 – Intelligent CRUD Docentes

**Tecnologías:** Spring Boot · MySQL · Validación · Filtros inteligentes · Paginación · KPIs · Swagger · Postman  
**Fecha de elaboración:** 12 de noviembre de 2025  
**Autor:** Ángel Yoelver Macha  
**Universidad:** UNCP – Facultad de Ingeniería de Sistemas  

---

## 1. Introducción

Durante la Semana 11 se desarrolló un **CRUD inteligente para la gestión de docentes**, implementado mediante una **API REST con Spring Boot** y persistencia en **MySQL**.  

A diferencia de un CRUD básico, este proyecto incorpora **validaciones avanzadas**, **filtros dinámicos**, **paginación automática**, **KPIs** y **documentación interactiva**, orientándose a un contexto académico–empresarial real.

El sistema permite administrar información docente de forma eficiente, segura y escalable, aplicando buenas prácticas de arquitectura en capas y estándares profesionales de desarrollo backend.

---

## 2. Objetivos

### 2.1 Objetivo General

Desarrollar una **API REST inteligente** para la gestión de docentes, aplicando validación de datos, filtros dinámicos, paginación, documentación técnica y pruebas profesionales.

### 2.2 Objetivos Específicos

- Diseñar el modelo de datos relacional para docentes.  
- Implementar validaciones con Jakarta Validation.  
- Aplicar filtros dinámicos por múltiples atributos.  
- Incorporar paginación automática con Spring Data JPA.  
- Documentar la API con Swagger UI.  
- Realizar pruebas completas con Postman.  
- Generar indicadores (KPIs) para análisis del sistema.  

---

## 3. Arquitectura del Proyecto

El proyecto sigue el patrón **Controller – Service – Repository**, separando responsabilidades y facilitando el mantenimiento.

```text
src/
└── main/java/
    ├── controller/
    ├── service/
    ├── repository/
    ├── entity/
    ├── dto/
    └── config/
```

### Evidencia – Proyecto en IntelliJ IDEA

<img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/9cc259a4067621e2d0373ce3b3ed0e73f1465cff/Semana11_imagenes/evid_proyecto_intellij.png" width="360"/>

---

## 4. Modelo de Datos – MySQL

El modelo de datos se diseñó para garantizar **integridad**, **eficiencia** y **compatibilidad con Spring Boot**.  
Toda la lógica del CRUD inteligente opera sobre la tabla principal **`docentes`**.

---

### 4.1 Características del modelo

- Llave primaria autoincremental.  
- Restricciones `NOT NULL`, `UNIQUE` y `CHECK`.  
- Campos optimizados para filtros y KPIs.  
- Auditoría mediante timestamp de creación.  

---

### 4.2 Script SQL implementado

```sql
CREATE TABLE docentes (
    id_docente       INT AUTO_INCREMENT PRIMARY KEY,
    nom_docente      VARCHAR(120) NOT NULL,
    dir_docente      VARCHAR(150) NOT NULL,
    ciu_docente      VARCHAR(100) NOT NULL,
    email_docente    VARCHAR(150) NOT NULL UNIQUE,
    fec_nacimiento   DATE NOT NULL,
    tiempo_servicio  INT NOT NULL CHECK (tiempo_servicio >= 0),
    creado_en        TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

Este script se ejecutó en MySQL para crear la tabla **docentes**, que luego se mapea en Spring Boot mediante JPA.  
Toda la lógica del CRUD inteligente (validaciones, filtros, KPIs y paginación) opera sobre esta estructura.

---

### 4.3 Explicación de los campos

| Campo | Tipo / Restricción | Descripción |
|---|---|---|
| `id_docente` | INT, PK, AUTO_INCREMENT | Identificador único del docente. |
| `nom_docente` | VARCHAR(120), NOT NULL | Nombre completo del docente. |
| `dir_docente` | VARCHAR(150), NOT NULL | Dirección del docente. |
| `ciu_docente` | VARCHAR(100), NOT NULL | Ciudad; usada en filtros y KPIs. |
| `email_docente` | VARCHAR(150), UNIQUE | Correo institucional único. |
| `fec_nacimiento` | DATE, NOT NULL | Validada con `@Past` en la API. |
| `tiempo_servicio` | INT, CHECK ≥ 0 | Años trabajados; base estadística. |
| `creado_en` | TIMESTAMP | Fecha de registro en la base de datos. |

---

### 4.4 Evidencia – Tabla MySQL

<img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/9cc259a4067621e2d0373ce3b3ed0e73f1465cff/Semana11_imagenes/evid_tabla_mysql_docentes.png" width="360"/>

---

## 5. Endpoints del CRUD Inteligente

| Método | Endpoint | Descripción |
|---|---|---|
| GET | `/api/docentes` | Listado con filtros y paginación |
| GET | `/api/docentes/{id}` | Obtener docente por ID |
| POST | `/api/docentes` | Registrar docente |
| PUT | `/api/docentes/{id}` | Actualizar docente |
| DELETE | `/api/docentes/{id}` | Eliminar docente |

---

## 6. Filtros Inteligentes y Paginación

La API permite aplicar filtros dinámicos por ciudad, años de servicio y nombre, combinados con paginación automática.

### Evidencia – Filtros y paginación

<img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/9cc259a4067621e2d0373ce3b3ed0e73f1465cff/Semana11_imagenes/evid_filtros_paginacion.png" width="360"/>

---

## 7. Documentación con Swagger UI

Swagger UI permite visualizar y probar todos los endpoints de la API de forma interactiva.

### Evidencia – Swagger UI

<img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/9cc259a4067621e2d0373ce3b3ed0e73f1465cff/Semana11_imagenes/evid_swagger_ui.png" width="360"/>

---

## 8. Pruebas con Postman

Se realizaron pruebas completas de los endpoints GET, POST, PUT y DELETE, validando respuestas y códigos HTTP.

### Evidencia – Colección Postman

<img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/9cc259a4067621e2d0373ce3b3ed0e73f1465cff/Semana11_imagenes/evid_postman_collection.png" width="360"/>

---

## 9. KPIs del Sistema

Los KPIs permiten analizar:

- Número de docentes registrados.  
- Distribución por ciudad.  
- Años promedio de servicio.  
- Docentes activos en el sistema.  

### Evidencia – KPIs

<img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/9cc259a4067621e2d0373ce3b3ed0e73f1465cff/Semana11_imagenes/evid_kpis_docentes.png" width="360"/>

---

## 10. Conclusiones

El desarrollo del **CRUD inteligente de docentes** permitió aplicar conceptos avanzados de backend profesional, fortaleciendo el uso de Spring Boot, validación de datos y diseño de APIs REST.

El sistema es escalable, seguro y preparado para integrarse en entornos académicos o administrativos reales, sentando bases sólidas para proyectos de mayor complejidad.

---

## 11. Anexos

### 11.1 Logos utilizados (360 px)

<img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/9cc259a4067621e2d0373ce3b3ed0e73f1465cff/Semana11_imagenes/logo_uncp.png" width="360"/>
<img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/9cc259a4067621e2d0373ce3b3ed0e73f1465cff/Semana11_imagenes/logo_fis.png" width="360"/>
<img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/9cc259a4067621e2d0373ce3b3ed0e73f1465cff/Semana11_imagenes/logo_spring.png" width="360"/>
<img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/9cc259a4067621e2d0373ce3b3ed0e73f1465cff/Semana11_imagenes/logo_mysql.png" width="360"/>
<img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/9cc259a4067621e2d0373ce3b3ed0e73f1465cff/Semana11_imagenes/logo_swagger.png" width="360"/>
<img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/9cc259a4067621e2d0373ce3b3ed0e73f1465cff/Semana11_imagenes/logo_postman.png" width="360"/>
<img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/9cc259a4067621e2d0373ce3b3ed0e73f1465cff/Semana11_imagenes/logo_validacion.png" width="360"/>
