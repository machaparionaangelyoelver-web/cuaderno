
<!-- ======================================================================
    ENCABEZADO (con fallback si el banner externo no carga)
====================================================================== -->

<!-- Banner animado (puede no cargar en algunos entornos) -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&height=140&color=0:0EA5E9,100:0F766E&text=📗%20Cuaderno%20Digital%20—%20Semana%2010%20(JSP%20%26%20Tomcat)&fontAlign=50&fontAlignY=35&fontSize=34&fontColor=ffffff&animation=fadeIn" alt="Banner Semana 10 — JSP & Tomcat" />
</p>

<!-- Fallback simple si el banner no carga -->
<div align="center">
  <div style="display:inline-block;padding:18px 22px;border-radius:10px;background:linear-gradient(90deg,#0EA5E9,#0F766E);color:#fff;font-family:Segoe UI,Arial,sans-serif;">
    <span style="font-size:28px;font-weight:700;">📗 Cuaderno Digital — Semana 10 (JSP & Tomcat)</span>
  </div>
</div>

<br/>

<!-- Logos institucionales con las RUTAS EXACTAS -->
<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/ff9b77146d41eed6035569e1e2c3f291116e9e72/Semana10_imagenes/uncp.png" width="96" alt="Logo UNCP" style="margin:10px;">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/ff9b77146d41eed6035569e1e2c3f291116e9e72/Semana10_imagenes/fis.png" width="96" alt="Logo FIS" style="margin:10px;">
</p>

<p align="center">
  <img
    alt="Semana 10 — JSP y Apache Tomcat"
    src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=24&duration=3500&pause=1200&color=14B8A6&center=true&vCenter=true&width=980&lines=%F0%9F%9A%9B%EF%B8%8F%20Semana%2010%20%E2%80%94%20JSP%20%26%20Apache%20Tomcat"
  />
</p>

<p align="center">
  <img
    alt="Macha Pariona Angel Yoelver — Desarrollo de Aplicaciones Web"
    src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=24&duration=3500&pause=1200&color=14B8A6&center=true&vCenter=true&width=980&lines=Macha%20Pariona%20Angel%20Yoelver%20%E2%80%94%20Desarrollo%20de%20Aplicaciones%20Web"
  />
</p>

---

## 🧭 Tabla de Contenidos
- [Introducción](#-introducción)
- [Objetivos de la Semana 10](#-objetivos-de-la-semana-10)
- [Requisitos y Entorno](#-requisitos-y-entorno)
- [Estructura de Directorios de Tomcat](#-estructura-de-directorios-de-tomcat)
- [server.xml — Elementos y Parámetros](#-serverxml--elementos-y-parámetros)
- [Flujo de Procesamiento de JSP en Tomcat](#-flujo-de-procesamiento-de-jsp-en-tomcat)
- [Variables de Entorno: JAVA_HOME y PATH](#-variables-de-entorno-javahome-y-path)
- [Instalación de Tomcat (Windows)](#-instalación-de-tomcat-windows)
- [Estructura de un Proyecto JSP](#-estructura-de-un-proyecto-jsp)
- [Evidencias de la Semana](#-evidencias-de-la-semana)
  - [fecha.jsp](#fechajsp)
  - [registroVisitas.jsp](#registrovisitasjsp)
  - [ejercicio10.jsp](#ejercicio10jsp)
- [Logs en Tomcat y Depuración](#-logs-en-tomcat-y-depuración)
- [MVC Básico aplicado a JSP](#-mvc-básico-aplicado-a-jsp)
- [Problemas Frecuentes y Soluciones](#-problemas-frecuentes-y-soluciones)
- [Conclusiones y Aprendizajes](#-conclusiones-y-aprendizajes)

---

## 🧭 Introducción

**JavaServer Pages (JSP)** permite mezclar **HTML** con **Java** para generar contenido dinámico del lado del servidor.  
**Apache Tomcat** funciona como **contenedor de servlets/JSP**, recibiendo peticiones HTTP, procesando la lógica y devolviendo respuestas HTML.

Esta semana te centraste en:
- Comprender **Tomcat** (directorios, `server.xml`, logs).
- Entender el **ciclo de vida** de una página **JSP**.
- Practicar con páginas funcionales: **`fecha.jsp`**, **`registroVisitas.jsp`**, **`ejercicio10.jsp`**.

> Las **evidencias** incluidas demuestran el flujo completo: peticiones, procesamiento JSP, uso de sesión y respuesta final al cliente.

---

## 🎯 Objetivos de la Semana 10

1. Identificar la **arquitectura** de Tomcat y su **estructura de directorios**.  
2. Reconocer los **elementos clave** de `server.xml` y sus **parámetros**.  
3. Comprender el **flujo de compilación/ejecución** de JSP en Tomcat.  
4. Configurar **JAVA_HOME** y **PATH** adecuadamente.  
5. Construir y desplegar un **proyecto JSP** mínimo y funcional.  
6. Presentar **evidencias** verificables en ejecución.

---

## 🧰 Requisitos y Entorno

- **JDK** instalado (OpenJDK o similar) y **variables** configuradas.  
- **Apache Tomcat 10+** (compatible con tu JDK).  
- Aplicación JSP dentro de `webapps/` (por ejemplo: `MiAppJSP/`).

---

## 🗂️ Estructura de Directorios de Tomcat

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/ff9b77146d41eed6035569e1e2c3f291116e9e72/Semana10_imagenes/estructura_tomcat_directorios.png" width="940" alt="Estructura de directorios de Tomcat" />
</p>

**Descripción:**
- **bin/**: scripts para iniciar/apagar Tomcat (`startup.bat`, `shutdown.bat`).  
- **conf/**: configuración (p. ej., `server.xml`, `web.xml`).  
- **logs/**: registros de ejecución.  
- **webapps/**: aplicaciones desplegadas (e.g., `ROOT/`, `MiAppJSP/`).  
- **temp/** y **work/**: archivos/clases temporales generados en runtime.

> *Figura 1*. Estructura de Tomcat. Recomendada para ubicar rápidamente `server.xml`, revisar `logs` y cargar tu app en `webapps`.

---

## ⚙️ `server.xml` — Elementos y Parámetros

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/ff9b77146d41eed6035569e1e2c3f291116e9e72/Semana10_imagenes/archivo_server_xml.png" width="940" alt="Elementos clave de server.xml" />
</p>

**Elementos principales:**
- `<Server>`: raíz del archivo, agrupa todo el servicio.  
- `<Service>`: organiza conectores y motor.  
- `<Connector>`: define **puerto** y protocolo (p. ej., `:8080`).  
- `<Engine>`: motor de procesamiento de peticiones.  
- `<Host>`: host virtual (dominio o nombre lógico).  
- `<Context>`: configuración específica por aplicación.

**Parámetros típicos útiles:**
- `port`: puerto del conector (ej. `8080`).  
- `maxThreads`: concurrencia máxima.  
- `connectionTimeout`: tiempo de espera de conexiones.  
- `redirectPort`: puerto para redirección a HTTPS.

> *Figura 2*. Mapa visual de `server.xml` para identificar qué cambia el **comportamiento** del servidor y **dónde** ajustarlo.

---

## 🔄 Flujo de Procesamiento de JSP en Tomcat

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/ff9b77146d41eed6035569e1e2c3f291116e9e72/Semana10_imagenes/flujo_peticion_tomcat.png" width="940" alt="Flujo petición JSP en Tomcat" />
</p>

**Secuencia:**
1. El cliente solicita `http://localhost:8080/MiAppJSP/fecha.jsp`.  
2. **Tomcat** (Conector 8080) recibe la petición.  
3. El **Motor JSP** traduce el `.jsp` a **Servlet** Java y lo **compila** (si no existe o cambió).  
4. El **Servlet** generado ejecuta la lógica y produce **HTML**.  
5. El cliente recibe la **respuesta**.

> *Figura 3*. El paso **JSP → Servlet** es clave: por eso los errores de compilación JSP aparecen como **HTTP 500** y se detallan en **`catalina.log`**.

---

## 🧪 Variables de Entorno: `JAVA_HOME` y `PATH`

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/ff9b77146d41eed6035569e1e2c3f291116e9e72/Semana10_imagenes/configuracion_variables_java.png" width="940" alt="Variables de entorno Java" />
</p>

- **`JAVA_HOME`** → carpeta de instalación del JDK.  
- **`PATH`** → incluye `%JAVA_HOME%\bin` para ejecutar `java` y `javac` desde cualquier carpeta.

**Verificación:**
```bash
java --version
javac --version
```
> *Figura 4*. Tener el **JDK** correctamente configurado evita fallos al compilar JSP o iniciar Tomcat.

---

## 🖥️ Instalación de Tomcat (Windows)

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/ff9b77146d41eed6035569e1e2c3f291116e9e72/Semana10_imagenes/instalacion_tomcat_windows.png" width="940" alt="Instalación de Tomcat Windows" />
</p>

**Resumen de pasos:**
1. Ejecutar **Windows Service Installer**.  
2. Aceptar licencia y seleccionar **componentes**.  
3. Configurar **puerto** (8080 por defecto) y **ruta del JDK**.  
4. Finalizar e iniciar el **servicio** de Tomcat.

> *Figura 5*. Si 8080 está ocupado, podrás cambiarlo luego en `conf/server.xml` (`<Connector port="8081" .../>`).

---

## 🧱 Estructura de un Proyecto JSP

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/ff9b77146d41eed6035569e1e2c3f291116e9e72/Semana10_imagenes/estructura_proyecto_jsp.png" width="940" alt="Estructura de proyecto JSP" />
</p>

```
webapps/
└─ MiAppJSP/
   ├─ index.jsp
   └─ WEB-INF/
      └─ web.xml
```

> *Figura 6*. Mantén tus JSPs organizados y utiliza `WEB-INF` para recursos que **no** deban ser accesibles directamente por URL.

---

## 🧪 Evidencias de la Semana

### `fecha.jsp`

**Descripción:** Imprime la fecha y hora actuales utilizando **expresiones JSP** y/o **scriptlets**.

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/ff9b77146d41eed6035569e1e2c3f291116e9e72/Semana10_imagenes/codigo_fecha_jsp.png" width="940" alt="Código fecha.jsp" />
</p>

**Código de referencia (opcional):**
```jsp
<%@ page language="java" contentType="text/html; charset=UTF-8" pageEncoding="UTF-8" %>
<!DOCTYPE html>
<html>
<head><title>Ejemplo JSP - Fecha</title></head>
<body>
  <h1>¡Hola desde JSP!</h1>
  <p>La fecha y hora actual es: <%= new java.util.Date() %></p>
</body>
</html>
```

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/ff9b77146d41eed6035569e1e2c3f291116e9e72/Semana10_imagenes/salida_fecha_jsp.png" width="940" alt="Salida fecha.jsp" />
</p>

---

### `registroVisitas.jsp`

**Descripción:** Saluda según la hora (mañana/tarde/noche), muestra fecha/hora y **cuenta visitas por sesión** con `session`.

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/ff9b77146d41eed6035569e1e2c3f291116e9e72/Semana10_imagenes/codigo_registrovisitas_jsp.png" width="940" alt="Código registroVisitas.jsp" />
</p>

**Código de referencia (opcional):**
```jsp
<%@ page language="java" contentType="text/html; charset=UTF-8" pageEncoding="UTF-8" %>
<!DOCTYPE html>
<html>
<head><title>Registro de Visitas</title></head>
<body>
<%
    java.util.Date ahora = new java.util.Date();
    int hora = ahora.getHours();
    String saludo = hora < 12 ? "¡Buenos días!" : (hora < 18 ? "¡Buenas tardes!" : "¡Buenas noches!");

    Integer contador = (Integer) session.getAttribute("contadorVisitas");
    if (contador == null) contador = 0;
    contador++;
    session.setAttribute("contadorVisitas", contador);
%>
  <h2><%= saludo %></h2>
  <p>Fecha y hora: <%= ahora.toLocaleString() %></p>
  <p>Visitas en esta sesión: <strong><%= contador %></strong></p>
</body>
</html>
```

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/ff9b77146d41eed6035569e1e2c3f291116e9e72/Semana10_imagenes/salida_registrovisitas_jsp.png" width="940" alt="Salida registroVisitas.jsp" />
</p>

---

### `ejercicio10.jsp`

**Descripción:** Formulario **GET** que calcula el **factorial** del número ingresado y maneja errores de entrada.

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/ff9b77146d41eed6035569e1e2c3f291116e9e72/Semana10_imagenes/codigo_ejercicio10_jsp.png" width="940" alt="Código ejercicio10.jsp" />
</p>

**Código de referencia (opcional):**
```jsp
<%@ page language="java" contentType="text/html; charset=UTF-8" pageEncoding="UTF-8" %>
<!DOCTYPE html>
<html>
<head><title>Cálculo del factorial</title></head>
<body>
  <h1>Cálculo del factorial</h1>
  <form action="ejercicio10.jsp" method="get">
    <p>Número: <input type="text" name="numero">
    <input type="submit" value="Calcular"></p>
  </form>

<%
  String numeroGet = request.getParameter("numero");
  if (numeroGet != null) {
      int n = 0;
      boolean error = false;
      double factorial = 1;
      try {
          n = Integer.parseInt(numeroGet);
          if (n < 1) error = true;
          else {
              for (int i = n; i > 1; i--) factorial *= i;
          }
      } catch (NumberFormatException e) { error = true; }

      if (error) {
          out.println("<p>Debe indicar un número entero mayor que 0</p>");
      } else {
          out.println("<p>Resultado: " + n + "! = " + factorial + "</p>");
      }
  }
%>
</body>
</html>
```

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/ff9b77146d41eed6035569e1e2c3f291116e9e72/Semana10_imagenes/salida_ejercicio10_jsp.png" width="940" alt="Salida ejercicio10.jsp" />
</p>

> *Figura 7*. Las tres evidencias validan: **entrada de datos**, **lógica de negocio en JSP** y **presentación HTML**.

---

## 🧾 Logs en Tomcat y Depuración

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/ff9b77146d41eed6035569e1e2c3f291116e9e72/Semana10_imagenes/estructura_logs_tomcat.png" width="940" alt="Estructura logs Tomcat" />
</p>

**Archivos más útiles:**
- `catalina.YYYY-MM-DD.log` → eventos generales del servidor.  
- `localhost_access_log.YYYY-MM-DD.txt` → **todas** las peticiones HTTP.  
- `manager.YYYY-MM-DD.log` → despliegues y errores del *Manager* (si lo usas).

**Tips de depuración:**
- Errores **500** en JSP → revisar `catalina.*.log` para ver la **stacktrace** de compilación.  
- **404** → revisar la **ruta** de la app en `webapps/` y la **URL** solicitada.  
- Puerto **8080** ocupado → cambiar en `server.xml` o **liberar** el puerto.

---

## 🧩 MVC Básico aplicado a JSP

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/ff9b77146d41eed6035569e1e2c3f291116e9e72/Semana10_imagenes/modelo_mvc_jsp.png" width="940" alt="Modelo MVC básico con JSP" />
</p>

- **Vista**: `formulario.jsp` (captura de datos).  
- **Controlador**: `ControllerServlet.java` (dirige flujo y lógica).  
- **Modelo**: clases Java (p. ej., `Usuario.java`) o acceso a datos.

> *Figura 8*. Aunque aquí trabajaste **JSP puro**, es importante visualizar la separación **Vista–Controlador–Modelo** para proyectos más grandes.

---

## 🛠️ Problemas Frecuentes y Soluciones

- **HTTP 404 (No encontrado)**  
  - Verifica la URL: `http://localhost:8080/MiAppJSP/archivo.jsp`.  
  - Confirma que la carpeta exista en `TOMCAT/webapps/MiAppJSP/`.

- **HTTP 500 (Error interno / Compilación JSP)**  
  - Revisa `catalina.YYYY-MM-DD.log`.  
  - Asegúrate de no usar clases/métodos inexistentes; valida imports.

- **Tomcat no inicia (puerto en uso)**  
  - Cambia `<Connector port="8081" .../>` en `conf/server.xml`.  
  - O libera el puerto 8080 (cerrando servicios que lo usen).

- **`JAVA_HOME` no configurado**  
  - Crea la variable apuntando al **JDK** y añade `%JAVA_HOME%\bin` a **`PATH`**.

---

## ✅ Conclusiones y Aprendizajes

- **JSP** permite generar contenido dinámico integrando **HTML + Java**.  
- **Tomcat** provee el entorno de ejecución y su configuración (directorios, `server.xml`, logs) es fundamental.  
- Las **evidencias** (`fecha.jsp`, `registroVisitas.jsp`, `ejercicio10.jsp`) demuestran dominio en: manejo de **sesiones**, **formularios** y **flujo JSP → Servlet → HTML**.  
- Con estas bases, estás listo para evolucionar hacia **MVC completo** (Servlets + JSP + DAO) o frameworks como **Jakarta EE / Spring** cuando corresponda.

---

### 📸 Anexo — Catálogo de Imágenes (Checklist)

| Nº | Archivo | Descripción breve |
|---:|---|---|
| 01 | `uncp.png` | Logo UNCP (portada y encabezados). |
| 02 | `fis.png` | Logo FIS (portada y encabezados). |
| 03 | `estructura_tomcat_directorios.png` | Árbol de directorios de Tomcat. |
| 04 | `archivo_server_xml.png` | Elementos `<Server>`, `<Service>`, `<Connector>`, `<Engine>`, `<Host>`, `<Context>`. |
| 05 | `flujo_peticion_tomcat.png` | Cliente → Tomcat → Motor JSP → Servlet → HTML. |
| 06 | `configuracion_variables_java.png` | `JAVA_HOME`, `PATH`, `java --version`, `javac --version`. |
| 07 | `instalacion_tomcat_windows.png` | Pasos del instalador (componentes, puerto, JDK). |
| 08 | `estructura_proyecto_jsp.png` | Estructura mínima de una app JSP. |
| 09 | `codigo_fecha_jsp.png` | Código de `fecha.jsp`. |
| 10 | `salida_fecha_jsp.png` | Navegador mostrando la salida de `fecha.jsp`. |
| 11 | `codigo_registrovisitas_jsp.png` | Código de `registroVisitas.jsp`. |
| 12 | `salida_registrovisitas_jsp.png` | Resultado con saludo + contador de sesión. |
| 13 | `flujo_registro_visitas_jsp.png` | Diagrama lógico del contador de visitas. |
| 14 | `codigo_ejercicio10_jsp.png` | Código del cálculo de factorial. |
| 15 | `salida_ejercicio10_jsp.png` | Resultado del factorial en navegador. |
| 16 | `estructura_logs_tomcat.png` | Archivos de log y su propósito. |
| 17 | `modelo_mvc_jsp.png` | Esquema MVC básico aplicable a JSP. |

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&height=120&color=0:0F766E,100:0EA5E9&section=footer" alt="Footer" />
</p>
