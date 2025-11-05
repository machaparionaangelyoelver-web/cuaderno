
<!-- ENCABEZADO animado con ola -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&height=140&color=0:0EA5E9,100:0F766E&text=📗%20Cuaderno%20Digital%20—%20Semana%2010%20(JSP%20%26%20Tomcat)&fontAlign=50&fontAlignY=35&fontSize=34&fontColor=ffffff&animation=fadeIn" />
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/main/Semana10_imagenes/uncp.png" width="90" alt="Logo UNCP" style="margin:10px;">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/main/Semana10_imagenes/fis.png" width="90" alt="Logo FIS" style="margin:10px;">
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
- [Requisitos Previos](#-requisitos-previos)
- [Estructura de Directorios de Tomcat](#-estructura-de-directorios-de-tomcat)
- [server.xml — Elementos Clave](#-serverxml--elementos-clave)
- [Flujo de Procesamiento de JSP en Tomcat](#-flujo-de-procesamiento-de-jsp-en-tomcat)
- [Variables de Entorno — JAVA_HOME y PATH](#-variables-de-entorno--javahome-y-path)
- [Instalación de Tomcat (Windows)](#-instalación-de-tomcat-windows)
- [Estructura de un Proyecto JSP](#-estructura-de-un-proyecto-jsp)
- [Evidencias Prácticas](#-evidencias-prácticas)
  - [fecha.jsp](#fechajsp)
  - [registroVisitas.jsp](#registrovisitasjsp)
  - [ejercicio10.jsp](#ejercicio10jsp)
- [Logs en Tomcat](#-logs-en-tomcat)
- [MVC Básico aplicado a JSP](#-mvc-básico-aplicado-a-jsp)
- [Problemas Comunes y Soluciones](#-problemas-comunes-y-soluciones)
- [Conclusiones](#-conclusiones)

---

## 🧭 Introducción

**JavaServer Pages (JSP)** permite mezclar **HTML** con **Java** para generar contenido dinámico en el servidor.  
**Apache Tomcat** actúa como **contenedor de servlets/JSP**, recibiendo peticiones HTTP del cliente, ejecutando la lógica en el servidor y respondiendo con HTML.

> Esta semana se consolidan conceptos de **instalación y configuración de Tomcat**, **procesamiento de JSP**, manejo de **sesiones**, y construcción de pequeñas **páginas dinámicas** como evidencias de aprendizaje.

---

## 🎯 Objetivos de la Semana 10

1. Entender la **arquitectura** y **directorios** de Tomcat.  
2. Identificar los **elementos clave** del archivo `server.xml`.  
3. Comprender el **flujo de ejecución** de una página JSP dentro de Tomcat.  
4. Configurar correctamente **JAVA_HOME** y **PATH**.  
5. Construir y desplegar un **proyecto JSP** funcional.  
6. Presentar **evidencias** (`fecha.jsp`, `registroVisitas.jsp`, `ejercicio10.jsp`).

---

## 🧰 Requisitos Previos

- **JDK** instalado y configurado (`JAVA_HOME`, `PATH`).  
- **Tomcat 10+** instalado (o versión compatible con tu JDK).  
- Carpeta `webapps/` con tu aplicación JSP (por ejemplo, `MiAppJSP`).

---

## 🗂️ Estructura de Directorios de Tomcat

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/main/Semana10_imagenes/estructura_tomcat_directorios.png" width="820" alt="Estructura de directorios de Tomcat" />
</p>

**Descripción rápida**  
- **bin/**: scripts de inicio/parada (`startup.bat`, `shutdown.bat`).  
- **conf/**: archivos de configuración (p. ej. `server.xml`, `web.xml`).  
- **logs/**: registros del servidor.  
- **webapps/**: aplicaciones desplegadas (por ejemplo `ROOT/`, `MiAppJSP/`).  
- **temp/** y **work/**: archivos y clases temporales.

---

## ⚙️ `server.xml` — Elementos Clave

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/main/Semana10_imagenes/archivo_server_xml.png" width="820" alt="Elementos clave de server.xml" />
</p>

- `<Server>`: raíz de la configuración.  
- `<Service>`: agrupa conectores y motor.  
- `<Connector>`: puerto/protocolo de entrada (p. ej. `8080`).  
- `<Engine>`: motor de procesamiento.  
- `<Host>`: host virtual.  
- `<Context>`: configuración puntual de una app.

**Parámetros típicos**: `port`, `maxThreads`, `connectionTimeout`, `redirectPort`.

---

## 🔄 Flujo de Procesamiento de JSP en Tomcat

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/main/Semana10_imagenes/flujo_peticion_tomcat.png" width="820" alt="Flujo petición JSP en Tomcat" />
</p>

1. **Cliente** solicita `http://localhost:8080/MiAppJSP/fecha.jsp`.  
2. **Tomcat** (Conector 8080) recibe la petición.  
3. **Motor JSP** transforma el `.jsp` en **Servlet** y lo compila (si es necesario).  
4. **Servlet** genera **HTML** de respuesta.  
5. **Cliente** recibe la página renderizada.

---

## 🧪 Variables de Entorno — `JAVA_HOME` y `PATH`

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/main/Semana10_imagenes/configuracion_variables_java.png" width="820" alt="Variables de entorno Java" />
</p>

- `JAVA_HOME` → ruta de instalación del JDK.  
- `PATH` → incluye `%JAVA_HOME%\bin` para ejecutar `java` y `javac` en cualquier ruta.  
- Comandos de verificación:
  ```bash
  java --version
  javac --version
  ```

---

## 🖥️ Instalación de Tomcat (Windows)

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/main/Semana10_imagenes/instalacion_tomcat_windows.png" width="820" alt="Instalación de Tomcat Windows" />
</p>

Pasos generales:
1. Descargar el **Windows Service Installer**.  
2. Aceptar licencia, seleccionar **componentes**.  
3. Especificar **puerto** (por defecto 8080) y **JDK**.  
4. Finalizar e iniciar el servicio.

---

## 🧱 Estructura de un Proyecto JSP

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/main/Semana10_imagenes/estructura_proyecto_jsp.png" width="820" alt="Estructura de proyecto JSP" />
</p>

```
webapps/
└─ MiAppJSP/
   ├─ index.jsp
   └─ WEB-INF/
      └─ web.xml
```

> **Sugerencia**: mantén tus JSP en la raíz de tu app o bajo subcarpetas lógicas (`/views`, `/pages`), y configura rutas en `web.xml` si lo requieres.

---

## 🧪 Evidencias Prácticas

### `fecha.jsp`

**Descripción:** Página que imprime la fecha y hora actuales usando una **expresión JSP** y/o **scriptlet**.

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/main/Semana10_imagenes/codigo_fecha_jsp.png" width="820" alt="Código fecha.jsp" />
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
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/main/Semana10_imagenes/salida_fecha_jsp.png" width="820" alt="Salida fecha.jsp" />
</p>

---

### `registroVisitas.jsp`

**Descripción:** Página que **saluda** según la hora (mañana/tarde/noche), **muestra fecha/hora** y **cuenta** visitas por sesión.

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/main/Semana10_imagenes/codigo_registrovisitas_jsp.png" width="820" alt="Código registroVisitas.jsp" />
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
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/main/Semana10_imagenes/salida_registrovisitas_jsp.png" width="820" alt="Salida registroVisitas.jsp" />
</p>

---

### `ejercicio10.jsp`

**Descripción:** Formulario que envía un número y calcula su **factorial**; incluye manejo básico de errores.

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/main/Semana10_imagenes/codigo_ejercicio10_jsp.png" width="820" alt="Código ejercicio10.jsp" />
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
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/main/Semana10_imagenes/salida_ejercicio10_jsp.png" width="820" alt="Salida ejercicio10.jsp" />
</p>

---

## 🧾 Logs en Tomcat

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/main/Semana10_imagenes/estructura_logs_tomcat.png" width="820" alt="Estructura logs Tomcat" />
</p>

- **catalina.YYYY-MM-DD.log** → mensajes generales del servidor.  
- **localhost_access_log.YYYY-MM-DD.txt** → peticiones HTTP.  
- **manager.YYYY-MM-DD.log** → despliegues y errores del *Manager*.

> Úsalos para depurar fallos de despliegue, errores 500, y monitorear peticiones.

---

## 🧩 MVC Básico aplicado a JSP

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/main/Semana10_imagenes/modelo_mvc_jsp.png" width="820" alt="Modelo MVC básico con JSP" />
</p>

- **Vista**: `formulario.jsp` (entrada de datos).  
- **Controlador**: `ControllerServlet.java` (procesa la lógica y decide la vista).  
- **Modelo**: clases Java (p. ej. `Usuario.java`) o acceso a datos.  

> En esta semana, el foco está en **JSP puro**, pero es útil entender que la separación en capas mejora mantenibilidad.

---

## 🛠️ Problemas Comunes y Soluciones

- **HTTP 404 en tu JSP**  
  - Verifica la ruta: `http://localhost:8080/MiAppJSP/archivo.jsp`.  
  - Confirma que la carpeta está en `TOMCAT/webapps/MiAppJSP/`.  

- **HTTP 500 – Compilación JSP**  
  - Revisa el log `catalina.*.log`.  
  - Asegúrate de que tu código JSP no contiene métodos o imports faltantes.  

- **Tomcat no inicia / Puerto 8080 ocupado**  
  - Cambia el puerto en `conf/server.xml` (`<Connector port="8081" .../>`) o libera el 8080.  

- **JAVA_HOME no configurado**  
  - Crea `JAVA_HOME` apuntando a tu JDK y añade `%JAVA_HOME%/bin` a `PATH`.

---

## ✅ Conclusiones

- **JSP** facilita la creación de contenido dinámico sobre **HTML**.  
- **Tomcat** provee el entorno de ejecución (contenedor de servlets/JSP) y su configuración es clave.  
- Las **evidencias** (`fecha.jsp`, `registroVisitas.jsp`, `ejercicio10.jsp`) demuestran la comprensión del flujo: **petición → procesamiento JSP → respuesta HTML → sesión**.  

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&height=120&color=0:0F766E,100:0EA5E9&section=footer" />
</p>
