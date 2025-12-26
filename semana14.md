Semana 14 · Backend con Python y Flask (Apache, WSGI y MySQL)
===================================================================

<!-- ======================================================================
      📘 CUADERNO DIGITAL — SEMANA 14
      BACKEND PYTHON • FLASK • APACHE • WSGI • MYSQL • EVIDENCIAS
====================================================================== -->

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&height=175&color=0:6AA9FF,50:4B8FE6,100:FFB4D3&text=📘%20Cuaderno%20Digital%20—%20Semana%2014&fontAlign=50&fontAlignY=36&fontSize=38&fontColor=ffffff&animation=fadeIn" />
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/126ed8fb4a59266ecf5a75d9d57bb83067bd2890/semana14_imagenes/logo_uncp.png" width="95" alt="Logo UNCP" style="margin:10px;">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/126ed8fb4a59266ecf5a75d9d57bb83067bd2890/semana14_imagenes/logo_fis.png"  width="95" alt="Logo FIS"  style="margin:10px;">
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/126ed8fb4a59266ecf5a75d9d57bb83067bd2890/semana14_imagenes/logo_apache.png" width="72" alt="Apache" style="margin:6px;">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/126ed8fb4a59266ecf5a75d9d57bb83067bd2890/semana14_imagenes/logo_python.png" width="72" alt="Python" style="margin:6px;">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/126ed8fb4a59266ecf5a75d9d57bb83067bd2890/semana14_imagenes/logo_flask.png"  width="72" alt="Flask"  style="margin:6px;">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/126ed8fb4a59266ecf5a75d9d57bb83067bd2890/semana14_imagenes/logo_mysql.png"  width="72" alt="MySQL"  style="margin:6px;">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/126ed8fb4a59266ecf5a75d9d57bb83067bd2890/semana14_imagenes/logo_vscode.png" width="72" alt="VS Code" style="margin:6px;">
</p>

<p align="center">
  <img
    alt="Leonel Macha Pariona — Semana 14"
    src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=22&duration=2600&pause=900&color=4B8FE6&center=true&vCenter=true&width=980&lines=Leonel%20Macha%20Pariona;Curso%3A%20Desarrollo%20de%20Aplicaciones%20Web;Tema%3A%20Backend%20con%20Python%20y%20Flask%20con%20Apache%20(WSGI)%20y%20MySQL%20(Semana%2014)"
  />
</p>

---

Enlaces principales
------------------

<table>
  <tr>
    <td><b>Repositorio GitHub (perfil)</b></td>
    <td>https://github.com/machaparionaangelyoelver-web</td>
  </tr>
  <tr>
    <td><b>Carpeta de evidencias y logos</b></td>
    <td>https://github.com/machaparionaangelyoelver-web/fotosdecuaderno/tree/126ed8fb4a59266ecf5a75d9d57bb83067bd2890/semana14_imagenes</td>
  </tr>
  <tr>
    <td><b>Ejemplo de evidencia</b></td>
    <td>https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/126ed8fb4a59266ecf5a75d9d57bb83067bd2890/semana14_imagenes/evid_01_apache_lounge_it_works.png</td>
  </tr>
</table>

---

Ficha técnica
------------

<table>
  <tr>
    <td><b>Estudiante</b></td>
    <td>Leonel Macha Pariona</td>
  </tr>
  <tr>
    <td><b>Correo personal</b></td>
    <td>leonelmacha19@gmail.com</td>
  </tr>
  <tr>
    <td><b>Correo institucional</b></td>
    <td>e_2021200788i@uncp.edu.pe</td>
  </tr>
  <tr>
    <td><b>Universidad</b></td>
    <td>Universidad Nacional del Centro del Perú</td>
  </tr>
  <tr>
    <td><b>Facultad</b></td>
    <td>Facultad de Ingeniería de Sistemas</td>
  </tr>
  <tr>
    <td><b>Tema</b></td>
    <td>Backend con Python y Flask integrado con Apache mediante WSGI y persistencia en MySQL</td>
  </tr>
</table>

---

Resumen ejecutivo
----------------

Durante la Semana 14 se implementó una práctica completa orientada a comprender el backend con Python desde una perspectiva cercana a producción.  
Se trabajó con Apache como servidor web, mod_wsgi como componente de integración, Python con Programación Orientada a Objetos para estructurar la lógica, y Flask conectado a MySQL para registrar información desde un formulario web.

El flujo final validado fue: navegador envía formulario, Flask procesa solicitud, PyMySQL ejecuta inserción y MySQL persiste el registro.  
Las evidencias muestran el entorno operativo, la configuración, el código base y la verificación del dato almacenado.

---

Objetivos
---------

<table>
  <tr>
    <td width="240"><b>Objetivo general</b></td>
    <td>Construir un mini sistema backend con Python y Flask conectado a MySQL, comprendiendo el rol de Apache y WSGI en la ejecución controlada de aplicaciones Python.</td>
  </tr>
  <tr>
    <td><b>Objetivos específicos</b></td>
    <td>
      <ul>
        <li>Instalar y validar Apache como servidor web local.</li>
        <li>Configurar mod_wsgi para habilitar el estándar WSGI.</li>
        <li>Reforzar POO con clases Persona y Estudiante para organizar la lógica.</li>
        <li>Desarrollar un formulario web en Flask con inserción a MySQL.</li>
        <li>Verificar persistencia mediante consulta a la tabla estudiantes.</li>
      </ul>
    </td>
  </tr>
</table>

---

Stack y componentes
-------------------

<table>
  <tr>
    <th align="left">Componente</th>
    <th align="left">Rol en la práctica</th>
    <th align="left">Resultado</th>
  </tr>
  <tr>
    <td><b>Apache HTTP Server</b></td>
    <td>Servidor frontal que recibe solicitudes HTTP y administra configuración.</td>
    <td>Servidor operativo y accesible en entorno local.</td>
  </tr>
  <tr>
    <td><b>WSGI</b></td>
    <td>Interfaz estándar para comunicar servidor web con aplicaciones Python.</td>
    <td>Modelo de integración entendido y aplicado.</td>
  </tr>
  <tr>
    <td><b>mod_wsgi</b></td>
    <td>Módulo de Apache que ejecuta aplicaciones Python bajo WSGI.</td>
    <td>Configuración obtenida y lista para aplicar en Apache.</td>
  </tr>
  <tr>
    <td><b>Python</b></td>
    <td>Lenguaje del backend y base de la lógica de negocio.</td>
    <td>Entorno verificado y dependencias instaladas.</td>
  </tr>
  <tr>
    <td><b>Flask</b></td>
    <td>Framework para rutas, vistas, formularios y lógica web.</td>
    <td>Aplicación ejecutándose y procesando solicitudes.</td>
  </tr>
  <tr>
    <td><b>MySQL</b></td>
    <td>Persistencia de datos para registrar estudiantes.</td>
    <td>Registro insertado y verificado con consulta.</td>
  </tr>
</table>

---

Arquitectura y flujo de trabajo
-------------------------------

<table>
  <tr>
    <td width="260"><b>Entrada</b></td>
    <td>Navegador web, envío de formulario con datos del estudiante.</td>
  </tr>
  <tr>
    <td><b>Servidor web</b></td>
    <td>Apache gestiona el puerto y controla el enrutamiento.</td>
  </tr>
  <tr>
    <td><b>Puente</b></td>
    <td>WSGI define la comunicación y mod_wsgi ejecuta el runtime de Python para servir la aplicación.</td>
  </tr>
  <tr>
    <td><b>Aplicación</b></td>
    <td>Flask recibe la petición, valida datos, prepara la operación de base de datos y devuelve una respuesta.</td>
  </tr>
  <tr>
    <td><b>Persistencia</b></td>
    <td>PyMySQL realiza inserción y MySQL almacena el registro en la tabla estudiantes.</td>
  </tr>
  <tr>
    <td><b>Salida</b></td>
    <td>Confirmación en interfaz web y verificación mediante consulta SQL.</td>
  </tr>
</table>

---

Procedimiento de implementación
-------------------------------

<table>
  <tr>
    <th align="left">Fase</th>
    <th align="left">Acción</th>
    <th align="left">Comando o detalle</th>
  </tr>
  <tr>
    <td><b>Servidor</b></td>
    <td>Instalación y prueba de Apache.</td>
    <td>Acceso a localhost para validar respuesta del servidor.</td>
  </tr>
  <tr>
    <td><b>WSGI</b></td>
    <td>Generación de configuración de mod_wsgi.</td>
    <td><code>mod_wsgi-express module-config</code></td>
  </tr>
  <tr>
    <td><b>Python</b></td>
    <td>Verificación de entorno y gestor de paquetes.</td>
    <td><code>python --version</code> y <code>pip --version</code></td>
  </tr>
  <tr>
    <td><b>Dependencias</b></td>
    <td>Instalación de librerías necesarias para backend y base de datos.</td>
    <td><code>pip install flask pymysql</code></td>
  </tr>
  <tr>
    <td><b>POO</b></td>
    <td>Implementación de clases base y derivada para representar el dominio.</td>
    <td>Clases Persona y Estudiante con herencia.</td>
  </tr>
  <tr>
    <td><b>Base de datos</b></td>
    <td>Creación de base de datos y tabla estudiantes.</td>
    <td>Creación de estructura y tipos de dato.</td>
  </tr>
  <tr>
    <td><b>Flask</b></td>
    <td>Ejecución de la aplicación para pruebas locales.</td>
    <td><code>python app.py</code></td>
  </tr>
  <tr>
    <td><b>Verificación</b></td>
    <td>Consulta a tabla para confirmar inserción.</td>
    <td><code>SELECT</code> sobre la tabla estudiantes.</td>
  </tr>
</table>

---

Script de base de datos
-----------------------

```sql
CREATE DATABASE escuela;
USE escuela;

CREATE TABLE estudiantes (
  id INT AUTO_INCREMENT PRIMARY KEY,
  nombre VARCHAR(120) NOT NULL,
  edad INT NOT NULL,
  carrera VARCHAR(120) NOT NULL,
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

---

Estructura de proyecto recomendada
----------------------------------

```text
semana14
  app.py
  conexion.py
  templates
    formulario.html
  static
    styles.css
```

---

Conceptos desarrollados
-----------------------

Apache y mod_wsgi  
Apache se utiliza como servidor frontal para recibir solicitudes HTTP. Al integrar mod_wsgi se habilita la ejecución de aplicaciones Python bajo el estándar WSGI, permitiendo un despliegue más controlado que el servidor de desarrollo.

WSGI  
WSGI define la interfaz de comunicación entre el servidor web y la aplicación Python. La aplicación expone una función WSGI y el servidor la invoca para obtener la respuesta a cada solicitud.

Python y POO  
Se aplicó herencia para reutilizar atributos y comportamientos. Persona actúa como clase base y Estudiante incorpora campos específicos para el registro. Esta estructura facilita escalabilidad y mantenimiento del backend.

Flask y MySQL  
Flask recibe datos por POST desde un formulario, procesa la solicitud y ejecuta una inserción en MySQL mediante PyMySQL. La persistencia se verificó mediante consulta directa a la tabla.

---

Evidencias de la semana (tamaño 400 px)
---------------------------------------

<table>
  <tr>
    <td width="420" align="center">
      <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/126ed8fb4a59266ecf5a75d9d57bb83067bd2890/semana14_imagenes/evid_01_apache_lounge_it_works.png" width="400" alt="Evidencia 01 Apache funcionando">
    </td>
    <td>
      <b>Evidencia 01. Apache en funcionamiento</b><br><br>
      Se valida que Apache responde correctamente desde el navegador. La página de prueba confirma que el servicio está activo y listo para integrarse con el módulo WSGI y aplicaciones Python.<br><br>
      <b>Resultado:</b> servidor web operativo en entorno local.
    </td>
  </tr>
</table>

<br>

<table>
  <tr>
    <td>
      <b>Evidencia 02. Configuración de mod_wsgi</b><br><br>
      Se obtiene la salida del comando de configuración para habilitar WSGI en Apache. Se identifican directivas necesarias para cargar la librería de Python y registrar el módulo, dejando listo el entorno para servir aplicaciones Python.<br><br>
      <b>Resultado:</b> base de configuración preparada para integrar en el servidor.
    </td>
    <td width="420" align="center">
      <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/126ed8fb4a59266ecf5a75d9d57bb83067bd2890/semana14_imagenes/evid_02_mod_wsgi_module_config.png" width="400" alt="Evidencia 02 módulo mod_wsgi">
    </td>
  </tr>
</table>

<br>

<table>
  <tr>
    <td width="420" align="center">
      <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/126ed8fb4a59266ecf5a75d9d57bb83067bd2890/semana14_imagenes/evid_03_python_pip_version.png" width="400" alt="Evidencia 03 Python y pip">
    </td>
    <td>
      <b>Evidencia 03. Verificación de Python y pip</b><br><br>
      Se confirma la versión de Python instalada y el funcionamiento de pip para gestión de dependencias. Esto garantiza un entorno estable para instalar librerías y ejecutar la aplicación backend.<br><br>
      <b>Resultado:</b> entorno Python validado.
    </td>
  </tr>
</table>

<br>

<table>
  <tr>
    <td>
      <b>Evidencia 04. Instalación de Flask y PyMySQL</b><br><br>
      Se instalan dependencias necesarias para el servidor web y la conexión a base de datos. Flask se utiliza para rutas y vistas, mientras PyMySQL habilita operaciones SQL desde Python.<br><br>
      <b>Resultado:</b> dependencias instaladas correctamente.
    </td>
    <td width="420" align="center">
      <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/126ed8fb4a59266ecf5a75d9d57bb83067bd2890/semana14_imagenes/evid_04_pip_install_flask_pymysql.png" width="400" alt="Evidencia 04 pip install">
    </td>
  </tr>
</table>

<br>

<table>
  <tr>
    <td width="420" align="center">
      <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/126ed8fb4a59266ecf5a75d9d57bb83067bd2890/semana14_imagenes/evid_05_clase_persona_estudiante.png" width="400" alt="Evidencia 05 clases POO">
    </td>
    <td>
      <b>Evidencia 05. Clases Persona y Estudiante</b><br><br>
      Se implementa herencia para estructurar la lógica del dominio. Persona concentra atributos generales y Estudiante agrega campos propios, permitiendo orden y reutilización del código.<br><br>
      <b>Resultado:</b> POO aplicada como base del backend.
    </td>
  </tr>
</table>

<br>

<table>
  <tr>
    <td>
      <b>Evidencia 06. Creación de base de datos y tabla</b><br><br>
      Se crea la base de datos escuela y la tabla estudiantes con campos obligatorios. La estructura queda lista para recibir registros desde el formulario de la aplicación.<br><br>
      <b>Resultado:</b> modelo de datos preparado para persistencia.
    </td>
    <td width="420" align="center">
      <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/126ed8fb4a59266ecf5a75d9d57bb83067bd2890/semana14_imagenes/evid_06_creacion_bd_escuela_tabla_estudiantes.png" width="400" alt="Evidencia 06 base de datos">
    </td>
  </tr>
</table>

<br>

<table>
  <tr>
    <td width="420" align="center">
      <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/126ed8fb4a59266ecf5a75d9d57bb83067bd2890/semana14_imagenes/evid_07_conexion_py_ok.png" width="400" alt="Evidencia 07 conexión PyMySQL">
    </td>
    <td>
      <b>Evidencia 07. Conexión Python a MySQL</b><br><br>
      Se implementa el módulo de conexión y se verifica acceso correcto desde Python. La evidencia confirma que la aplicación puede abrir sesión en MySQL y ejecutar consultas.<br><br>
      <b>Resultado:</b> conexión funcional para operaciones de inserción y consulta.
    </td>
  </tr>
</table>

<br>

<table>
  <tr>
    <td>
      <b>Evidencia 08. Aplicación Flask en ejecución</b><br><br>
      Se ejecuta la aplicación y se confirma el servicio local activo para pruebas. La consola muestra la dirección de acceso para validar el formulario y el procesamiento backend.<br><br>
      <b>Resultado:</b> aplicación lista para recibir solicitudes.
    </td>
    <td width="420" align="center">
      <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/126ed8fb4a59266ecf5a75d9d57bb83067bd2890/semana14_imagenes/evid_08_app_flask_corriendo.png" width="400" alt="Evidencia 08 Flask corriendo">
    </td>
  </tr>
</table>

<br>

<table>
  <tr>
    <td width="420" align="center">
      <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/126ed8fb4a59266ecf5a75d9d57bb83067bd2890/semana14_imagenes/evid_09_formulario_registro_estudiantes.png" width="400" alt="Evidencia 09 formulario estudiantes">
    </td>
    <td>
      <b>Evidencia 09. Formulario de registro</b><br><br>
      Se visualiza el formulario renderizado en navegador. Los campos capturan datos del estudiante y envían la información por POST para su validación e inserción en la base de datos.<br><br>
      <b>Resultado:</b> interfaz funcional para captura de información.
    </td>
  </tr>
</table>

<br>

<table>
  <tr>
    <td>
      <b>Evidencia 10. Registro guardado en MySQL</b><br><br>
      Se realiza consulta de verificación a la tabla estudiantes y se observa el registro insertado desde la aplicación. Se confirma la persistencia del dato y el flujo completo del backend.<br><br>
      <b>Resultado:</b> inserción confirmada mediante consulta SQL.
    </td>
    <td width="420" align="center">
      <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/126ed8fb4a59266ecf5a75d9d57bb83067bd2890/semana14_imagenes/evid_10_registro_guardado_mysql.png" width="400" alt="Evidencia 10 registro guardado">
    </td>
  </tr>
</table>

---

Resultados obtenidos
--------------------

<table>
  <tr>
    <th align="left">Producto</th>
    <th align="left">Evidencia</th>
    <th align="left">Validación</th>
  </tr>
  <tr>
    <td>Apache operativo</td>
    <td>Evidencia 01</td>
    <td>Respuesta del servidor en navegador</td>
  </tr>
  <tr>
    <td>WSGI configurado</td>
    <td>Evidencia 02</td>
    <td>Directivas generadas para integrar en Apache</td>
  </tr>
  <tr>
    <td>Entorno Python listo</td>
    <td>Evidencia 03 y 04</td>
    <td>Versiones y dependencias instaladas</td>
  </tr>
  <tr>
    <td>Modelo POO aplicado</td>
    <td>Evidencia 05</td>
    <td>Clases con herencia y estructura ordenada</td>
  </tr>
  <tr>
    <td>Persistencia en MySQL</td>
    <td>Evidencia 06, 07 y 10</td>
    <td>Tabla creada, conexión verificada y registro confirmado</td>
  </tr>
  <tr>
    <td>Aplicación web funcional</td>
    <td>Evidencia 08 y 09</td>
    <td>Servidor activo, formulario operativo y procesamiento POST</td>
  </tr>
</table>

---

Conclusiones
------------

- Apache integrado con mod_wsgi permite ejecutar aplicaciones Python con mayor control del servidor y configuración centralizada.
- WSGI estandariza la comunicación entre servidor web y aplicación, facilitando el despliegue en escenarios reales.
- La Programación Orientada a Objetos mejora la organización del backend, facilitando reutilización y escalabilidad.
- Flask permite implementar rutas y formularios con un flujo claro de solicitud, validación, persistencia y respuesta.
- MySQL con PyMySQL completa el ciclo de backend al garantizar inserción y verificación de datos persistentes.

---

Control de versionamiento con Git
---------------------------------

<table>
  <tr>
    <td width="240"><b>Propósito</b></td>
    <td>Registrar avances por etapas para mantener trazabilidad del trabajo y facilitar recuperación o revisión.</td>
  </tr>
  <tr>
    <td><b>Comandos base</b></td>
    <td>
      <code>git init</code><br>
      <code>git add .</code><br>
      <code>git commit -m "Semana 14: configuración Apache y WSGI"</code><br>
      <code>git commit -m "Semana 14: POO Persona y Estudiante"</code><br>
      <code>git commit -m "Semana 14: Flask con MySQL y formulario"</code>
    </td>
  </tr>
</table>

---

Contacto
--------

<table>
  <tr>
    <td width="240"><b>Estudiante</b></td>
    <td>Leonel Macha Pariona</td>
  </tr>
  <tr>
    <td><b>Correo personal</b></td>
    <td>leonelmacha19@gmail.com</td>
  </tr>
  <tr>
    <td><b>Correo institucional</b></td>
    <td>e_2021200788i@uncp.edu.pe</td>
  </tr>
  <tr>
    <td><b>GitHub</b></td>
    <td>https://github.com/machaparionaangelyoelver-web</td>
  </tr>
</table>
