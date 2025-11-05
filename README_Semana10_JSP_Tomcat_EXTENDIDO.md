
<!-- ======================================================================
      📗 CUADERNO DIGITAL — SEMANA 10
      JSP • TOMCAT • EVIDENCIAS
====================================================================== -->

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&height=150&color=0:0EA5E9,100:0F766E&text=📗%20Cuaderno%20Digital%20—%20Semana%2010%20(JSP%20%2B%20Tomcat%20%2B%20Evidencias)&fontAlign=50&fontAlignY=35&fontSize=34&fontColor=ffffff&animation=fadeIn" />
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/main/Semana10_imagenes/uncp.jpg" width="90" alt="Logo UNCP" style="margin:10px;">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/main/Semana10_imagenes/logoFIS.png" width="90" alt="Logo FIS" style="margin:10px;">
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/main/Semana10_imagenes/logo_java.png" width="70" alt="Logo Java" style="margin:5px;">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/main/Semana10_imagenes/logo-jsp.png" width="70" alt="Logo JSP" style="margin:5px;">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/main/Semana10_imagenes/logo_tomcat.png" width="70" alt="Logo Tomcat" style="margin:5px;">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/main/Semana10_imagenes/logo_maven.png" width="70" alt="Logo Maven" style="margin:5px;">
</p>

<p align="center">
  <img alt="Desarrollo Backend — JSP + Tomcat" 
       src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=24&duration=3500&pause=1200&color=14B8A6&center=true&vCenter=true&width=980&lines=Desarrollo+Backend+—+JSP+%2B+Tomcat+%2B+Evidencias;Programaci%C3%B3n+Web+Din%C3%A1mica+con+Java+EE+%7C+Apache+Tomcat" />
</p>

---

## 🧭 Introducción

Durante la **Semana 10** se exploraron los fundamentos del **desarrollo web dinámico con Java**, centrando la práctica en el uso de **JavaServer Pages (JSP)** y el **servidor Apache Tomcat**.  
Estos componentes permiten construir aplicaciones web que combinan **HTML, lógica de negocio Java y conexión a bases de datos** de manera integrada.

El objetivo principal fue comprender cómo el **servidor Tomcat interpreta, compila y ejecuta** las páginas JSP, así como desplegar aplicaciones funcionales que gestionen formularios, sesiones y salidas dinámicas.

---

## 🎯 Objetivos Específicos

1. Instalar y configurar correctamente **JDK**, **Tomcat** y las variables de entorno.  
2. Analizar la **estructura interna del servidor Apache Tomcat**.  
3. Comprender el funcionamiento del archivo **`server.xml`** y sus elementos clave.  
4. Desarrollar y desplegar **páginas JSP** dinámicas (fecha actual, contador de visitas, cálculo de factorial).  
5. Consolidar conocimientos del modelo **MVC** aplicados a proyectos con JSP.  
6. Generar y documentar **evidencias funcionales** en ejecución.

---

## ⚙️ Estructura del Servidor Apache Tomcat

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/main/Semana10_imagenes/estructura_tomcat_directorios.png" width="350" alt="Estructura de directorios Tomcat" />
</p>

El servidor **Tomcat** está organizado en carpetas que permiten administrar su comportamiento interno:

- **bin/** → scripts de inicio y apagado (`startup.bat`, `shutdown.bat`)
- **conf/** → archivos de configuración, incluyendo `server.xml` y `web.xml`
- **logs/** → registros de ejecución y errores
- **webapps/** → ubicación de las aplicaciones web desplegadas
- **work/** y **temp/** → archivos temporales generados en tiempo de ejecución

---

## 🧩 Archivo de Configuración `server.xml`

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/main/Semana10_imagenes/archivo_server_xml.png" width="350" alt="Archivo server.xml" />
</p>

Este archivo define los componentes principales del servidor:

- `<Server>` → elemento raíz del archivo  
- `<Service>` → agrupa los conectores y el motor de procesamiento  
- `<Connector>` → define el puerto (por defecto 8080) y protocolo de comunicación  
- `<Engine>` → motor encargado de procesar las solicitudes  
- `<Host>` → define los hosts virtuales disponibles  
- `<Context>` → parámetros específicos de las aplicaciones

**Parámetros relevantes:**
`port`, `maxThreads`, `connectionTimeout`, `redirectPort`.

---

## 🔄 Flujo de Procesamiento JSP → Servlet

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/main/Semana10_imagenes/flujo_peticion_tomcat.png" width="350" alt="Flujo de petición JSP en Tomcat" />
</p>

1. El cliente envía una petición al servidor (`http://localhost:8080/app/archivo.jsp`).  
2. Tomcat analiza la solicitud y **convierte el JSP en un Servlet Java**.  
3. El Servlet se **compila** y ejecuta, generando una **respuesta HTML dinámica**.  
4. Finalmente, el navegador muestra el resultado al usuario.

> Este proceso demuestra cómo JSP actúa como una capa de presentación conectada directamente con la lógica Java.

---

## 🧱 Estructura del Proyecto JSP

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/main/Semana10_imagenes/estructura_proyecto_jsp.png" width="350" alt="Estructura de proyecto JSP" />
</p>

Cada aplicación JSP debe ubicarse dentro de `webapps/` de Tomcat y contener al menos:

```
webapps/
 └── MiAppJSP/
      ├── index.jsp
      └── WEB-INF/
           └── web.xml
```

El archivo `web.xml` define configuraciones de despliegue y mapeo de servlets.

---

## 🧪 Variables de Entorno — JAVA_HOME y PATH

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/main/Semana10_imagenes/configuracion_variables_java.png" width="350" alt="Configuración variables Java" />
</p>

Configurar correctamente las variables del sistema permite ejecutar comandos desde cualquier ruta:

```bash
java --version
javac --version
```

Esto garantiza la comunicación entre el **JDK**, el **IDE** y el **servidor Tomcat**.

---

## 🧠 Arquitectura MVC en JSP

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/main/Semana10_imagenes/modelo_mvc_jsp.png" width="350" alt="Modelo MVC JSP" />
</p>

El patrón **Modelo–Vista–Controlador (MVC)** separa la lógica de negocio, la interfaz de usuario y el flujo de control, mejorando la escalabilidad y mantenibilidad del sistema.

---

## 🌐 Flujo del Formulario JSP (GET/POST)

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/main/Semana10_imagenes/flujo_formulario_get_post.png" width="350" alt="Flujo formulario JSP GET POST" />
</p>

Los formularios JSP pueden utilizar los métodos `GET` o `POST` para enviar información, la cual es procesada en el servidor mediante objetos como `request`, `response` y `session`.

---

## 📜 Instalación de Tomcat (Windows)

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/main/Semana10_imagenes/instalacion_tomcat_windows.png" width="350" alt="Instalación Tomcat Windows" />
</p>

1. Descargar el instalador desde [tomcat.apache.org](https://tomcat.apache.org).  
2. Ejecutar el asistente de instalación, aceptar licencia y seleccionar componentes.  
3. Configurar el **puerto 8080** y especificar la ruta del **JDK**.  
4. Finalizar e iniciar el servicio Tomcat.

---

## 🔍 Archivos de Log del Servidor

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/main/Semana10_imagenes/estructura_logs_tomcat.png" width="350" alt="Estructura logs Tomcat" />
</p>

- **catalina.log** → mensajes generales del servidor  
- **localhost_access_log.txt** → peticiones HTTP  
- **manager.log** → registros de despliegue

Estos registros son esenciales para la depuración de errores y monitoreo del rendimiento.

---

# 🌟 EVIDENCIAS PRÁCTICAS

## 🧾 Evidencia General — Semana 10

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/main/Semana10_imagenes/evidencia_semana10.png" width="700" alt="Evidencia Semana 10 JSP y Tomcat" />
</p>

La evidencia muestra el entorno completo de trabajo con **Tomcat ejecutando aplicaciones JSP**, verificando el correcto despliegue de los archivos en el navegador y la funcionalidad de los scripts dinámicos.

---

## 📅 Evidencia — fecha.jsp

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/main/Semana10_imagenes/evidencia_fecha.png" width="700" alt="Evidencia fecha.jsp" />
</p>

Esta página imprime la **fecha y hora actual del sistema**, demostrando la integración entre **Java y HTML**.  
El código utiliza expresiones JSP del tipo `<%= new java.util.Date() %>`, evidenciando el uso de objetos Java dentro de una página web.

---

## 👥 Evidencia — registroVisitas.jsp

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/main/Semana10_imagenes/evidencia_registrovisitas.png" width="700" alt="Evidencia registroVisitas.jsp" />
</p>

Este ejercicio implementa una **lógica de sesión**, almacenando la cantidad de veces que un usuario ha visitado la página.  
Utiliza `session.setAttribute()` y `session.getAttribute()` para persistir el contador, además de un scriptlet que determina el saludo dinámico (¡Buenos días, tardes o noches!).

---

## 🧩 Evidencia — Aplicación CRUD (Estudiantes)

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/main/Semana10_imagenes/evidencia_semana10.png" width="700" alt="Evidencia CRUD JSP MySQL" />
</p>

Se desarrolló una aplicación **CRUD con JSP + JDBC + MySQL**, donde es posible listar, agregar y eliminar registros de estudiantes.  
La interfaz incluye componentes visuales intuitivos, mostrando el uso de **formularios JSP, consultas SQL y actualización dinámica de datos**.

---

## 🧭 Conclusiones

- **JSP** permite construir interfaces dinámicas y personalizadas, integrando lógica Java directamente en HTML.  
- **Tomcat** actúa como un contenedor confiable que facilita el despliegue, ejecución y monitoreo de aplicaciones web.  
- Las **evidencias** desarrolladas validan la correcta implementación de los conceptos aprendidos: flujo de peticiones, gestión de sesiones y generación de contenido dinámico.  
- Este entorno constituye la base para avanzar hacia frameworks modernos como **Spring Boot** o **Jakarta EE**.

---

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&height=120&color=0:0F766E,100:0EA5E9&section=footer" />
</p>
