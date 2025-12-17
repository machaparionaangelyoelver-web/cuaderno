<!-- ======================================================================
      📗 CUADERNO DIGITAL — SEMANA 12
      BACKEND CON PHP • MYSQL • CONCEPTOS • EVIDENCIAS
====================================================================== -->

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&height=160&color=0:7C3AED,50:2563EB,100:14B8A6&text=📗%20Cuaderno%20Digital%20—%20Semana%2012&fontAlign=50&fontAlignY=35&fontSize=36&fontColor=ffffff&animation=fadeIn" />
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/7fa4a9c04448511e1ca1aae80c2901fc3eedca56/semana12_imagenes/logo_uncp.png" width="95" alt="Logo UNCP" style="margin:10px;">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/7fa4a9c04448511e1ca1aae80c2901fc3eedca56/semana12_imagenes/logo_fis.png" width="95" alt="Logo FIS" style="margin:10px;">
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/7fa4a9c04448511e1ca1aae80c2901fc3eedca56/semana12_imagenes/logo_php.png" width="70" alt="PHP" style="margin:5px;">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/7fa4a9c04448511e1ca1aae80c2901fc3eedca56/semana12_imagenes/logo_mysql.png" width="70" alt="MySQL" style="margin:5px;">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/7fa4a9c04448511e1ca1aae80c2901fc3eedca56/semana12_imagenes/logo_apache.png" width="70" alt="Apache" style="margin:5px;">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/7fa4a9c04448511e1ca1aae80c2901fc3eedca56/semana12_imagenes/logo_composer.png" width="70" alt="Composer" style="margin:5px;">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/7fa4a9c04448511e1ca1aae80c2901fc3eedca56/semana12_imagenes/logo_postman.png" width="70" alt="Postman" style="margin:5px;">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/7fa4a9c04448511e1ca1aae80c2901fc3eedca56/semana12_imagenes/logo_vscode.png" width="70" alt="VS Code" style="margin:5px;">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/7fa4a9c04448511e1ca1aae80c2901fc3eedca56/semana12_imagenes/logo_intellij.png" width="70" alt="IntelliJ" style="margin:5px;">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/7fa4a9c04448511e1ca1aae80c2901fc3eedca56/semana12_imagenes/logo_laravel.png" width="70" alt="Laravel (opcional)" style="margin:5px;">
</p>

<p align="center">
  <img
    alt="Macha Pariona Angel Yoelver — Semana 12"
    src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=22&duration=2600&pause=900&color=2563EB&center=true&vCenter=true&width=980&lines=Macha%20Pariona%20Angel%20Yoelver;Curso%3A%20Desarrollo%20de%20Aplicaciones%20Web;Tema%3A%20Backend%20con%20PHP%20y%20MySQL%20(Semana%2012)"
  />
</p>

---

## Datos del informe

- **Autor:** Macha Pariona Angel Yoelver  
- **Curso:** Desarrollo de Aplicaciones Web  
- **Semana:** 12  
- **Tema:** Backend con PHP y MySQL (CRUD, validación, seguridad mínima y pruebas)  
- **Fecha:** 14 de diciembre de 2025  

---

# 1. Introducción

En la **Semana 12** se desarrolló un **backend** usando **PHP** como lenguaje del lado del servidor y **MySQL** como motor de base de datos.  
El objetivo central fue comprender y aplicar el rol del backend como capa que:

- Recibe solicitudes (HTTP) desde un cliente (navegador o Postman).  
- Valida datos antes de guardarlos.  
- Ejecuta lógica del negocio.  
- Accede a la base de datos de forma segura.  
- Responde con **JSON** y **códigos HTTP** adecuados.

Como práctica integradora se implementó un **CRUD completo** (Create, Read, Update, Delete), acompañado de validaciones y manejo de errores para asegurar resultados consistentes y verificables.

---

# 2. Objetivos

## 2.1 Objetivo general
Implementar un backend funcional con PHP y MySQL que permita gestionar registros mediante un CRUD, aplicando validación de datos, seguridad mínima con consultas preparadas y pruebas de endpoints.

## 2.2 Objetivos específicos
- Configurar y verificar el entorno local de ejecución (servidor, PHP, base de datos).
- Construir una base de datos y tabla base para el CRUD.
- Implementar conexión segura con **PDO** y manejo controlado de errores.
- Desarrollar endpoints CRUD con respuestas **JSON** y códigos **HTTP**.
- Aplicar reglas de validación y control de errores (400, 404, 500).
- Probar endpoints con Postman registrando evidencias.

---

# 3. Justificación

El backend define **la integridad y confiabilidad** de una aplicación web. Aunque el frontend sea visualmente atractivo, sin un backend que valide, controle errores y proteja el acceso a datos, el sistema queda expuesto a:

- Datos inconsistentes o duplicados (por ejemplo, correos repetidos).
- Fallas difíciles de depurar por respuestas sin estándar.
- Riesgos básicos de seguridad como inyección SQL.

Por ello, esta semana se enfocó en buenas prácticas mínimas pero profesionales: **PDO**, **prepared statements**, validación y pruebas reproducibles.

---

# 4. Alcance

Incluye:

- Entorno local: servidor web, PHP y MySQL.
- Base de datos: creación de BD y tabla principal del CRUD.
- Backend: endpoints CRUD con JSON y códigos HTTP.
- Validaciones: email, campos obligatorios, control de IDs.
- Pruebas: evidencias de consumo de endpoints con Postman.

No incluye:

- Autenticación (sesiones/JWT).
- Interfaz frontend completa para consumo del backend.
- Despliegue productivo (hosting, VPS o nube).

---

# 5. Metodología de desarrollo

Se aplicó una metodología práctica e incremental:

1. **Preparación del entorno:** verificar versiones, servidor y base de datos.
2. **Diseño de datos:** estructura de tabla con restricciones necesarias.
3. **Conexión a BD:** configuración con PDO y control de errores.
4. **Implementación CRUD:** construir rutas y operaciones principales.
5. **Validación y manejo de errores:** reglas de negocio y códigos HTTP.
6. **Pruebas y evidencias:** ejecutar casos en Postman y documentar capturas.

---

# 6. Stack y herramientas

| Componente | Uso |
|---|---|
| PHP | Lógica del backend y generación de respuestas JSON |
| MySQL | Persistencia de datos |
| Apache (XAMPP/Laragon) | Servidor local para ejecutar PHP |
| Composer | Gestión de dependencias (opcional, por ejemplo dotenv) |
| Postman | Pruebas de endpoints y verificación de códigos HTTP |
| VS Code / IntelliJ | Edición y organización del proyecto |

---

# 7. Conceptos clave trabajados

## 7.1 Backend
El backend es la capa que **procesa y protege** la información. Su responsabilidad no es solo “guardar datos”, sino garantizar que los datos cumplan reglas y que el cliente reciba respuestas claras.

## 7.2 API y endpoints
Un endpoint es una ruta (URL) que representa una acción. En un CRUD típico se manejan rutas para listar, crear, actualizar y eliminar.

## 7.3 CRUD
CRUD es el ciclo de vida de un dato:

- **Create:** insertar un registro nuevo.
- **Read:** consultar uno o varios registros.
- **Update:** modificar un registro existente.
- **Delete:** eliminar un registro.

## 7.4 HTTP y respuestas estándar
El backend debe comunicar el resultado con códigos HTTP:

| Código | Significado | Ejemplo |
|---|---|---|
| 200 | OK | Consulta correcta |
| 201 | Created | Registro creado |
| 400 | Bad Request | Datos inválidos |
| 404 | Not Found | ID no existe |
| 500 | Server Error | Error interno |

## 7.5 PDO y prepared statements
- **PDO** estandariza la conexión y ejecución de consultas.
- **Prepared statements** separan la consulta SQL de los datos de entrada, reduciendo el riesgo de inyección SQL.

---

# 8. Comandos y scripts utilizados

## 8.1 Verificación de versiones
```bash
php -v
composer -V
```

## 8.2 Servidor local (opción rápida)
```bash
php -S localhost:8000 -t public
```

## 8.3 Creación de base de datos y tabla
> Modelo base recomendado para un CRUD de docentes.

```sql
CREATE DATABASE semana12 CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
USE semana12;

CREATE TABLE docentes (
  id INT AUTO_INCREMENT PRIMARY KEY,
  nombre VARCHAR(120) NOT NULL,
  email VARCHAR(150) NOT NULL UNIQUE,
  facultad VARCHAR(120) NOT NULL,
  estado ENUM('activo','inactivo') DEFAULT 'activo',
  creado_en TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

## 8.4 Conexión PDO (base)
```php
<?php
$pdo = new PDO(
  "mysql:host=localhost;dbname=semana12;charset=utf8mb4",
  "root",
  "",
  [
    PDO::ATTR_ERRMODE => PDO::ERRMODE_EXCEPTION,
    PDO::ATTR_DEFAULT_FETCH_MODE => PDO::FETCH_ASSOC
  ]
);
```

## 8.5 Validación mínima (ejemplo)
```php
<?php
$email = $_POST["email"] ?? "";

if (!filter_var($email, FILTER_VALIDATE_EMAIL)) {
  http_response_code(400);
  echo json_encode(["ok"=>false, "msg"=>"Email inválido"]);
  exit;
}
```

---

# 9. Endpoints del CRUD

> Modelo típico para pruebas con Postman (adaptable a tu estructura de rutas).

| Método | Ruta | Acción | Respuesta esperada |
|---|---|---|---|
| GET | `/api/docentes` | Listar docentes | 200 + JSON |
| GET | `/api/docentes/{id}` | Obtener por ID | 200 o 404 |
| POST | `/api/docentes` | Crear docente | 201 o 400 |
| PUT | `/api/docentes/{id}` | Actualizar docente | 200, 400 o 404 |
| DELETE | `/api/docentes/{id}` | Eliminar docente | 200 o 404 |

---

# 10. Evidencias

A continuación se muestran capturas que respaldan el trabajo realizado (entorno, versiones, configuración, BD, Postman, validación y resultados).

## 10.1 Entorno y verificación

**Evidencia 01 — Instalación y entorno activo**  
<img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/7fa4a9c04448511e1ca1aae80c2901fc3eedca56/semana12_imagenes/evid_01_instalacion_entorno.png" width="760" alt="Evidencia 01 - Instalación y entorno" />

**Evidencia 02 — Versiones de PHP y Composer**  
<img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/7fa4a9c04448511e1ca1aae80c2901fc3eedca56/semana12_imagenes/evid_02_versiones_php_composer.png" width="760" alt="Evidencia 02 - Versiones" />

## 10.2 Construcción del proyecto y configuración

**Evidencia 03 — Creación del proyecto**  
<img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/7fa4a9c04448511e1ca1aae80c2901fc3eedca56/semana12_imagenes/evid_03_creacion_proyecto.png" width="760" alt="Evidencia 03 - Creación de proyecto" />

**Evidencia 04 — Configuración del entorno (.env o parámetros)**  
<img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/7fa4a9c04448511e1ca1aae80c2901fc3eedca56/semana12_imagenes/evid_04_env_config.png" width="760" alt="Evidencia 04 - Configuración" />

## 10.3 Base de datos

**Evidencia 05 — Migraciones o creación de tabla en MySQL**  
<img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/7fa4a9c04448511e1ca1aae80c2901fc3eedca56/semana12_imagenes/evid_05_migraciones_bd.png" width="760" alt="Evidencia 05 - BD y tabla" />

## 10.4 Pruebas con Postman

**Evidencia 06 — Prueba GET (listar)**  
<img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/7fa4a9c04448511e1ca1aae80c2901fc3eedca56/semana12_imagenes/evid_06_postman_get.png" width="760" alt="Evidencia 06 - Postman GET" />

**Evidencia 07 — Pruebas POST, PUT y DELETE**  
<img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/7fa4a9c04448511e1ca1aae80c2901fc3eedca56/semana12_imagenes/evid_07_postman_post_put_delete.png" width="760" alt="Evidencia 07 - Postman CRUD" />

## 10.5 Validaciones y errores controlados

**Evidencia 08 — Validaciones y manejo de errores**  
<img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/7fa4a9c04448511e1ca1aae80c2901fc3eedca56/semana12_imagenes/evid_08_validaciones_errores.png" width="760" alt="Evidencia 08 - Validaciones" />

## 10.6 Organización y cierre

**Evidencia 09 — Estructura del proyecto (organización)**  
<img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/7fa4a9c04448511e1ca1aae80c2901fc3eedca56/semana12_imagenes/evid_09_estructura_proyecto.png" width="760" alt="Evidencia 09 - Estructura del proyecto" />

**Evidencia 10 — Resultados finales**  
<img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/7fa4a9c04448511e1ca1aae80c2901fc3eedca56/semana12_imagenes/evid_10_resultados_finales.png" width="760" alt="Evidencia 10 - Resultados finales" />

---

# 11. KPIs de verificación

| KPI | Valor | Interpretación |
|---|---:|---|
| Endpoints probados | 4 | CRUD completo validado |
| Códigos HTTP cubiertos | 4 | 200/201, 400, 404, 500 |
| Evidencias registradas | 10 | Flujo completo documentado |
| Seguridad mínima aplicada | Sí | PDO y consultas preparadas |

---

# 12. Resultados

- Se obtuvo un backend funcional con endpoints CRUD y respuestas JSON.
- La base de datos responde correctamente y mantiene restricciones (email único).
- Las validaciones reducen errores comunes y mejoran la calidad del dato.
- Postman permitió verificar el contrato de la API y registrar evidencias de forma clara.

---

# 13. Conclusiones

1. El backend no solo “guarda datos”: define reglas, valida y controla errores para mantener integridad.
2. PDO y consultas preparadas son una base mínima profesional para reducir riesgos de inyección SQL.
3. El uso de JSON y códigos HTTP estandariza la comunicación con cualquier cliente (frontend o móvil).
4. La evidencia con Postman facilita la verificación y sustento del trabajo académico.

---

# 14. Recomendaciones y mejoras futuras

- Incorporar **paginación y filtros** (por query params) para listados grandes.
- Implementar **autenticación y roles** para proteger endpoints.
- Agregar **logging y auditoría** (registro de cambios, errores y accesos).
- Documentar la API con OpenAPI/Swagger (si se evoluciona a un framework).
- Preparar despliegue en hosting o servidor (configuración de producción).

---

## Anexo A — Plantilla de request para Postman

### Crear docente (POST)
```json
{
  "nombre": "Ana Pérez",
  "email": "ana.perez@correo.com",
  "facultad": "Ingeniería",
  "estado": "activo"
}
```

### Actualizar docente (PUT)
```json
{
  "nombre": "Ana Pérez",
  "email": "ana.perez@correo.com",
  "facultad": "Ingeniería de Sistemas",
  "estado": "activo"
}
```
