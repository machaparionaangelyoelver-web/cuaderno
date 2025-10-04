<!-- ENCABEZADO animado con ola -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&height=140&color=0:0F766E,100:0EA5E9&text=📕%20Cuaderno%20Digital%20—%20Semana%2006&fontAlign=50&fontAlignY=35&fontSize=34&fontColor=ffffff&animation=fadeIn" />
</p>

<!-- Logos (puedes cambiar las URLs si subes nuevos) -->
<p align="center">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/main/semana03_imagenes/uncp.jpg" width="96" height="96" alt="Logo UNCP" style="margin:10px;">
  <img src="https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/main/semana03_imagenes/logoFIS.png" width="96" height="96" alt="Logo FIS" style="margin:10px;">
</p>

<!-- Animación con el nombre del estudiante -->
<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=26&duration=2500&pause=1000&color=0EA5E9&center=true&vCenter=true&width=920&lines=Estudiante%3A%20Macha%20Pariona%20Angel%20Yoelver;IX%20Semestre%20%E2%80%94%20Facultad%20de%20Ingenier%C3%ADa%20de%20Sistemas;Universidad%20Nacional%20del%20Centro%20del%20Per%C3%BA" />
</p>

<!-- Animación adicional con el título largo de la semana -->
<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=24&duration=2400&pause=900&color=14B8A6&center=true&vCenter=true&width=980&lines=🌌%20Semana%2006%20—%20Componentes%20en%20React%3A%20JSX%2C%20Props%2FChildren%2C%20Comunicaci%C3%B3n%2C%20TSX%2C%20Estilos" alt="🌌 Semana 06 — Componentes en React: JSX, Props/Children, Comunicación, TSX, Estilos" />
</p>

---

# Semana 06 — Componentes en React
**Cuaderno digital · Frontend**  
**Tema:** Componentización, JSX, comunicación entre componentes, tipado con TypeScript y estilos.

> Esta semana consolidamos la base de React: cómo se **monta** la aplicación, cómo **piensa** el **Virtual DOM**, cómo **creamos componentes** (clase vs función), cómo **escribimos JSX** de forma correcta, cómo **tipamos** con **TypeScript**, cómo **estilizamos** (CSS, Modules, inline, Tailwind) y cómo **comunicamos** datos entre componentes (**props, children, lifting state**). Cerramos con dos casos prácticos y 5 evidencias.

---

## Índice
- [Objetivos y contexto](#objetivos-y-contexto)
- [Renderizado y Virtual DOM](#renderizado-y-virtual-dom)
- [¿Qué es un componente? (Clase vs Función)](#qué-es-un-componente-clase-vs-función)
- [JSX en la práctica](#jsx-en-la-práctica)
- [TypeScript en React (TSX)](#typescript-en-react-tsx)
- [Estilos en componentes](#estilos-en-componentes)
- [Props y Children](#props-y-children)
- [Composición y comunicación](#composición-y-comunicación)
- [Casos prácticos](#casos-prácticos)
- [Evidencias (galería)](#evidencias-galería)
- [Conclusiones](#conclusiones)
- [Referencias](#referencias)

---

## Objetivos y contexto
1. Comprender **cómo se monta** una app React en el DOM y por qué el **Virtual DOM** hace eficiente la actualización de UI.  
2. Dominar la **creación de componentes** (preferentemente **funcionales**) y el uso correcto de **JSX**.  
3. Aplicar **props**, **children**, **composición** y **comunicación** (padre→hijo, hijo→padre y entre hermanos).  
4. Introducir **TypeScript (TSX)** para tipado de **props** y más robustez.  
5. Evaluar opciones de **estilos** (CSS, CSS Modules, inline, Tailwind) para distintos escenarios.  
6. Implementar un **layout responsivo** y una **tabla de estudiantes** como casos integradores.

> **Comentario:** React es una librería de *UI*. No decide todo tu stack; por eso es importante comparar alternativas (p. ej., CSS Modules vs Tailwind) y entender cuándo conviene cada una.

![Portada de la Semana 06: Componentes en React](https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/08066b9a50f2a050e1c1e095700a705057456e67/semana06_imagenes/portada/portada_semana06.jpg)

---

## Renderizado y Virtual DOM
El punto de entrada en Vite/React suele ser `main.jsx` (o `main.tsx`). Desde allí, **montamos** la App sobre un nodo del DOM como `#root`.

**React 18+ (createRoot):**
```jsx
// main.jsx
import React from 'react'
import { createRoot } from 'react-dom/client'
import App from './App.jsx'

const root = createRoot(document.getElementById('root'))
root.render(<App />)
```

> **Nota:** `ReactDOM.render` está **obsoleto** para nuevas apps. Usa `createRoot` (React 18+).

**¿Virtual DOM?**  
React mantiene una representación en memoria del DOM (árbol de nodos). Cuando el estado cambia, React calcula un **diff** entre el árbol previo y el nuevo, y aplica **solo** las modificaciones mínimas necesarias al DOM real (**reconciliación**).

![Esquema de ReactDOM renderizando en el elemento root](https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/08066b9a50f2a050e1c1e095700a705057456e67/semana06_imagenes/renderizado_dom/reactdom_render_esquema.png)
![Diagrama de Virtual DOM, diffing y reconciliación](https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/08066b9a50f2a050e1c1e095700a705057456e67/semana06_imagenes/renderizado_dom/virtual_dom_diffing.png)

> **Comentario:** El DOM real es costoso de manipular. El Virtual DOM permite *agrupar* y optimizar cambios, mejorando performance.

---

## ¿Qué es un componente? (Clase vs Función)
Un **componente** es una pieza reutilizable de UI. Hoy se priorizan los **componentes de función** (con *hooks*).

### Clase (histórico)
```jsx
import { Component } from 'react'

class SaludoClase extends Component {
  render(){
    return <h2>Hola desde un componente de Clase</h2>
  }
}
export default SaludoClase
```
![Ejemplo de componente de clase en React](https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/08066b9a50f2a050e1c1e095700a705057456e67/semana06_imagenes/componentes/componente_clase.png)

### Función (preferido)
```jsx
function Saludo({ nombre = 'Mundo' }) {
  return <h2>Hola, {nombre} 👋</h2>
}
export default Saludo
```
Con estado y eventos:
```jsx
import { useState } from 'react'

function Contador(){
  const [n, setN] = useState(0)
  return (
    <div>
      <p>Valor: {n}</p>
      <button onClick={() => setN(n + 1)}>Incrementar</button>
    </div>
  )
}
```
![Ejemplo de componente de función en React](https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/08066b9a50f2a050e1c1e095700a705057456e67/semana06_imagenes/componentes/componente_funcion.png)

> **Comentario:** Con **hooks** (`useState`, `useEffect`, etc.) los componentes de función resultan más expresivos y fáciles de testear.

---

## JSX en la práctica

### Variables, atributos y expresiones
```jsx
const usuario = { id: 7, name: 'Ada' }
const estilo = { color: '#0ea5e9', fontWeight: 'bold' }

export default function Perfil(){
  return (
    <div id={`user-${usuario.id}`} style={estilo}>
      <p>Usuario: {usuario.name}</p>
      <p>Edad estimada: {20 + 4}</p>
    </div>
  )
}
```
![Inserción de variables en JSX](https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/08066b9a50f2a050e1c1e095700a705057456e67/semana06_imagenes/jsx/jsx_variables.png)
![Atributos dinámicos en JSX](https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/08066b9a50f2a050e1c1e095700a705057456e67/semana06_imagenes/jsx/jsx_atributos.png)
![Expresiones JavaScript dentro de JSX](https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/08066b9a50f2a050e1c1e095700a705057456e67/semana06_imagenes/jsx/jsx_expresiones.png)

### Fragments y regla de etiqueta raíz
```jsx
export default function Lista(){
  return (
    <>
      <li>A</li>
      <li>B</li>
    </>
  )
}
```
![Fragmentos en JSX como contenedor raíz](https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/08066b9a50f2a050e1c1e095700a705057456e67/semana06_imagenes/jsx/jsx_fragment.png)

> **Regla:** Las etiquetas **autocerradas** deben cerrarse: `<img />`, `<input />`.
![Regla de cierre de etiquetas en JSX](https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/08066b9a50f2a050e1c1e095700a705057456e67/semana06_imagenes/jsx/jsx_cerrar_etiquetas.png)

### Render condicional (if, ternario, &&)
```jsx
function Estado({ online }){
  if (!online) return <span>Offline</span>
  return <span>Online</span>
}

const EstadoTernario = ({ n }) => <p>{n % 2 === 0 ? 'Par' : 'Impar'}</p>
const Mensaje = ({ ok }) => <p>{ok && 'Éxito'}</p>
```
![Render condicional con if en React](https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/08066b9a50f2a050e1c1e095700a705057456e67/semana06_imagenes/jsx/jsx_condicional_if.png)
![Render condicional con ? : en JSX](https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/08066b9a50f2a050e1c1e095700a705057456e67/semana06_imagenes/jsx/jsx_condicional_ternario.png)
![Render condicional con operador AND lógico](https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/08066b9a50f2a050e1c1e095700a705057456e67/semana06_imagenes/jsx/jsx_condicional_and.png)

### Listas con `.map()` y `key`
```jsx
const estudiantes = [
  { id: 'a1', nombre: 'Ana', activo: true },
  { id: 'b2', nombre: 'Bruno', activo: false }
]

export default function ListaEstudiantes(){
  return (
    <ul>
      {estudiantes.map(e => (
        <li key={e.id}>
          {e.nombre} {e.activo ? '✅' : '⛔'}
        </li>
      ))}
    </ul>
  )
}
```
![Renderizado de listas con map en JSX](https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/08066b9a50f2a050e1c1e095700a705057456e67/semana06_imagenes/jsx/jsx_map_listas.png)

> **Comentario:** La `key` debe ser **estable y única** (evita el índice del array en listas mutables).

---

## TypeScript en React (TSX)
**Props tipadas** aportan autocompletado y evitan errores comunes.

```tsx
// Saludo.tsx
type Props = {
  nombre?: string
  veces?: number
}

export default function Saludo({ nombre = 'Mundo', veces = 1 }: Props){
  return <h3>{`Hola ${nombre}! `.repeat(veces)}</h3>
}
```
![Variables tipadas en TypeScript para React](https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/08066b9a50f2a050e1c1e095700a705057456e67/semana06_imagenes/typescript/ts_tipado_basico.png)
![Componente TSX con tipado de props](https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/08066b9a50f2a050e1c1e095700a705057456e67/semana06_imagenes/typescript/componente_tsx.png)

> **Comentario:** Empieza tipando **props** y funciones. Más adelante, modela **estado** y **APIs** con interfaces.

---

## Estilos en componentes

### CSS (hojas)
```jsx
// App.jsx
import './App.css'
export default () => <h1 className="title">Hola CSS</h1>
```
![Hojas de estilo CSS en React](https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/08066b9a50f2a050e1c1e095700a705057456e67/semana06_imagenes/estilos/css_hojas.png)

### CSS Modules
```css
/* Card.module.css */
.card { padding: 12px; border: 1px solid #dbeafe; border-radius: 12px }
.title { font-weight: 700 }
```
```jsx
// Card.jsx
import styles from './Card.module.css'
export default function Card({ children }){
  return <div className={styles.card}><h3 className={styles.title}>Card</h3>{children}</div>
}
```
![CSS Modules en componentes React](https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/08066b9a50f2a050e1c1e095700a705057456e67/semana06_imagenes/estilos/css_modules.png)

### Inline styles
```jsx
const box = { background:'#fff', border:'1px solid #e5e7eb', padding:'8px 12px' }
export default () => <div style={box}>Inline</div>
```
![Estilos inline en React](https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/08066b9a50f2a050e1c1e095700a705057456e67/semana06_imagenes/estilos/css_inline.png)

### Tailwind CSS (con Vite)
Instala y configura:
```bash
npm i -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```
![Instalación de Tailwind en un proyecto React/Vite](https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/08066b9a50f2a050e1c1e095700a705057456e67/semana06_imagenes/estilos/tailwind_instalacion.png)

Configura `tailwind.config.js`:
```js
export default {
  content: ['./index.html', './src/**/*.{
    js,ts,jsx,tsx
  }'],
  theme: { extend: {} },
  plugins: []
}
```
![Configuración de rutas de Tailwind](https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/08066b9a50f2a050e1c1e095700a705057456e67/semana06_imagenes/estilos/tailwind_config.png)

Agrega directivas en tu CSS base (p. ej., `src/index.css`):
```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```
![Directivas de Tailwind en el CSS principal](https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/08066b9a50f2a050e1c1e095700a705057456e67/semana06_imagenes/estilos/tailwind_directivas.png)

> **Comentario:** Tailwind acelera prototipado con utilidades. CSS Modules te da **encapsulamiento** semántico por componente. Elige según el **equipo** y el **proyecto**.

---

## Props y Children
**Props** pasan datos desde el **padre** al **hijo**. `children` permite **anidar** contenido dentro de un componente.

```jsx
function Boton({ children, tipo = 'button', onClick }){
  return <button type={tipo} onClick={onClick} className="btn">{children}</button>
}

export default function Ejemplo(){
  return (
    <Boton onClick={() => alert('Hola!')}>Click aquí</Boton>
  )
}
```
![Paso de props desde el padre al hijo](https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/08066b9a50f2a050e1c1e095700a705057456e67/semana06_imagenes/props_children/props_basico.png)
![Uso de children en componentes React](https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/08066b9a50f2a050e1c1e095700a705057456e67/semana06_imagenes/props_children/children_basico.png)

**Composición:** Usamos componentes contenedores que **orquestan** otros componentes.
![Composición de componentes](https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/08066b9a50f2a050e1c1e095700a705057456e67/semana06_imagenes/props_children/composicion_componentes.png)

---

## Composición y comunicación
- **Padre → Hijo:** vía **props**.
- **Hijo → Padre:** elevando estado (*lifting state up*) con **callbacks**.
- **Hermanos:** comparten estado en el **padre** o mediante **context** si es global.

```jsx
import { useState } from 'react'

function Hijo({ onValor }){
  return <input onChange={(e)=> onValor(e.target.value)} placeholder="Escribe..." />
}
function Padre(){
  const [valor, setValor] = useState('')
  return (
    <>
      <Hijo onValor={setValor} />
      <p>Valor recibido: {valor}</p>
    </>
  )
}
```
![Comunicación de padre a hijo con props](https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/08066b9a50f2a050e1c1e095700a705057456e67/semana06_imagenes/comunicacion/parent_to_child.png)
![Comunicación de hijo a padre elevando estado](https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/08066b9a50f2a050e1c1e095700a705057456e67/semana06_imagenes/comunicacion/child_to_parent.png)
![Comunicación entre hermanos via estado en el padre](https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/08066b9a50f2a050e1c1e095700a705057456e67/semana06_imagenes/comunicacion/hermanos_estado_compartido.png)

> **Comentario:** Si la información debe estar disponible para muchos niveles, considera **Context API** (o una librería de estado).

---

## Casos prácticos

### 1) Layout responsivo (desktop/tablet/móvil)
Estructura con componentes `Header`, `Sidebar`, `Main`, `Footer` y utilidades (CSS Modules o Tailwind).

```jsx
export default function Layout(){
  return (
    <div className="grid-layout">
      <Header />
      <Sidebar />
      <Main />
      <Footer />
    </div>
  )
}
```
![Layout responsivo con varios componentes](https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/08066b9a50f2a050e1c1e095700a705057456e67/semana06_imagenes/casos/layout_responsivo.png)

### 2) Tabla de estudiantes
```jsx
const data = [
  { id: 'A01', nombre: 'Ana', ciudad: 'Huancayo', activo: true },
  { id: 'B02', nombre: 'Bruno', ciudad: 'Lima', activo: false }
  // ...
]

function Tabla({ filas }){
  return (
    <table>
      <thead><tr><th>ID</th><th>Nombre</th><th>Ciudad</th><th>Estado</th></tr></thead>
      <tbody>
        {filas.map(r => (
          <tr key={r.id}>
            <td>{r.id}</td>
            <td>{r.nombre}</td>
            <td>{r.ciudad}</td>
            <td>{r.activo ? 'Activo ✅' : 'Inactivo ⛔'}</td>
          </tr>
        ))}
      </tbody>
    </table>
  )
}
```
![Tabla de estudiantes en React](https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/08066b9a50f2a050e1c1e095700a705057456e67/semana06_imagenes/casos/tabla_estudiantes.png)

> **Comentario:** Mantén **datos** y **presentación** desacoplados. La tabla solo renderiza lo que recibe por **props**.

---

## Evidencias (galería)
Estas imágenes documentan los 5 ejercicios desarrollados:

1. `evidencia_01_render_root.jpg` — Montaje inicial con `createRoot` (main.jsx) y vista en el navegador.  
   ![Evidencia: montaje inicial](https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/08066b9a50f2a050e1c1e095700a705057456e67/semana06_imagenes/evidencias/evidencia_01_render_root.jpg)

2. `evidencia_02_componente_funcional_props.jpg` — Componente funcional recibiendo **props** y renderizado.  
   ![Evidencia: componente funcional con props](https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/08066b9a50f2a050e1c1e095700a705057456e67/semana06_imagenes/evidencias/evidencia_02_componente_funcional_props.jpg)

3. `evidencia_03_children_composicion.jpg` — Uso de **children** y **composición** (Layout).  
   ![Evidencia: children y composición](https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/08066b9a50f2a050e1c1e095700a705057456e67/semana06_imagenes/evidencias/evidencia_03_children_composicion.jpg)

4. `evidencia_04_lift_state_child_to_parent.jpg` — **Lifting state** (hijo actualiza estado en el padre).  
   ![Evidencia: hijo a padre elevando estado](https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/08066b9a50f2a050e1c1e095700a705057456e67/semana06_imagenes/evidencias/evidencia_04_lift_state_child_to_parent.jpg)

5. `evidencia_05_list_map_condicional.jpg` — **Listas con `.map()`** + **render condicional** (p. ej., “Activo/Inactivo”).  
   ![Evidencia: map + condicional](https://raw.githubusercontent.com/machaparionaangelyoelver-web/fotosdecuaderno/08066b9a50f2a050e1c1e095700a705057456e67/semana06_imagenes/evidencias/evidencia_05_list_map_condicional.jpg)

> **Sugerencia:** añade breves descripciones bajo cada evidencia en el PR de GitHub para facilitar la revisión.

---

## Conclusiones
- React **desacopla** la UI en **componentes** reutilizables y testeables.  
- El **Virtual DOM** y la **reconciliación** optimizan la actualización del DOM real.  
- Con **JSX** y **hooks** los componentes de función son el estándar actual.  
- **Props/children/composición** y **lifting state** son la base de la **comunicación** y el **flujo de datos**.  
- **TypeScript** añade seguridad y autocompletado; empieza por **props**.  
- Para estilos, evalúa **CSS Modules** (encapsulamiento) o **Tailwind** (rapidez). Elige según tu equipo.

---

## Referencias
- React Docs: https://react.dev/  
- React DOM Client (`createRoot`): https://react.dev/reference/react-dom/client/createRoot  
- JSX: https://react.dev/learn/writing-markup-with-jsx  
- Hooks (useState): https://react.dev/reference/react/useState  
- TypeScript + React: https://www.typescriptlang.org/docs/handbook/react.html  
- Vite: https://vitejs.dev/  
- Tailwind CSS: https://tailwindcss.com/docs/installation
