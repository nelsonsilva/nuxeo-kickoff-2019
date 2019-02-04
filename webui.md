---
customTheme : "kickoff"
transition: "convex"
highlightTheme: "darkula"
---

![](logo.png) <!-- .element: style="max-width: 50%; float: left" -->

# Kickoff 2019
<br>
## WebUI
### What's the plan?
<br>
Nelson Silva

---

## Web UI
### Where we are 📍  <!-- .element: class="fragment" -->
### "Times They Are A-Changin" 🔮 <!-- .element: class="fragment" -->
### What's the plan? 🗺 <!-- .element: class="fragment" --> 

---

## Kickoff 2017 ☀️ 🇵🇹
### Webcomponents 

- Custom Elements
- Templates
- HTML Imports
- Shadow DOM

## 👏 🍻 <!-- .element: class="fragment" --> 

---

## Q2 2017

### WebUI 1.0 🎉 

- Polymer 1
  - Custom elements V0
  - "Shady" DOM V0
  - Templates
  - HTML Imports

---

## Configurable
Layout elements <!-- .element: class="fragment" -->

## Pluggable <!-- .element: class="fragment" -->
Slots <!-- .element: class="fragment" -->

### View Designer 🎉 <!-- .element: class="fragment" -->

---

## Q2 2017

### Polymer 2

- Custom elements V1 <!-- .element: class="fragment" -->
  - `registerElement(...)` <!-- .element: class="fragment strike" -->
  - `customElements.define(...)` <!-- .element: class="fragment" -->
- Shadow DOM V1 <!-- .element: class="fragment" -->
  - `<content>` <!-- .element: class="fragment strike" -->
  - `<slot>` <!-- .element: class="fragment" -->
- ES6 class based elements <!-- .element: class="fragment" -->

---

## Q4 2017

### Web UI 2.1.3 🎉 (9.3) <!-- .element: class="fragment" -->

- Polymer 2
  - Custom Elements V1
  - Shadow DOM V1
  - Template
  - HTML Imports

- ES6 elements

---

## Q2 2018

### Polymer 3 <!-- .element: class="fragment" -->

<p>
<span>Bower</span><!-- .element: class="fragment strike" -->
<span>npm</span> <!-- .element: class="fragment" -->
</p> <!-- .element: class="fragment" -->
<p>
<span>HTML imports</span> <!-- .element: class="fragment strike" -->
<span>😱 ES modules</span> <!-- .element: class="fragment" -->
</p> <!-- .element: class="fragment" -->

---

## HTML Imports
```
<link rel="import" href="nuxeo-doc-view-layout.html">
```

## ES Modules
```
import 'nuxeo-doc-view-layout.js'
```

### Elements as JS only <!-- .element: class="fragment" -->
`mv *.html *.js 😱` <!-- .element: class="fragment" -->

### No dynamic imports yet! <!-- .element: class="fragment" -->

---

## Q2 2018 - Polymer 3 plan 🗺 

1. Move to npm 👏 <!-- .element: class="fragment" -->
2. Migrate to Polymer 3 👏 <!-- .element: class="fragment" -->
3. Keep HTML imports (polyfill) 🤔 <!-- .element: class="fragment" -->

### Move to proper build! <!-- .element: class="fragment" -->

```js
import MyComponent from 'MyComponent.vue'
import CSS from 'style.css'
import PolymerComponent from 'my-component.html'
```  
<!-- .element: class="fragment" -->

---

## But...

> for new projects, we suggest you use ... <!-- .element: class="fragment" -->

### LitElement  <!-- .element: class="fragment" -->

---

## Polymer 3 plan ✋ 

> "we'll continue to support the Polymer 3.x APIs with maintenance releases for the foreseeable future"

### Polymer's not dead! <!-- .element: class="fragment" -->
(yet) <!-- .element: class="fragment" -->

---

## Web UI stack plan 🗺 

Polymer 3 <!-- .element: class="fragment strike" -->

<em>Not worth breaking changes!</em><!-- .element: class="fragment" -->

<p>🎯 JSF feature parity and migration</p> <!-- .element: class="fragment" -->
<p>👬 support Polymer 2 and migration</p> <!-- .element: class="fragment" -->
<p>🔮 LitElement</p><!-- .element: class="fragment" -->

---

### LitElement

```js
static get template() {
  return html`
    <span>[[text]]</span>
  `;
}
```
<!-- .element: class="fragment strike" -->

```js
render() {
  return html`
    <span>${this.text}</span>
  `;
}
```
<!-- .element: class="fragment" -->

---

## Q4 2018

### Product workshop

- ***Web*** development
- Low code
- Cloud first

---

## Web @ Nuxeo today

### Doing JS in a Java world 🙃

<p>mvn ⇒ ant ⇒ npm</p> <!-- .element: class="fragment" -->
<p>`src/main/js` ⇒ `target/classes`</p> <!-- .element: class="fragment" -->
<p>📦 npm ⇒ <span style="font-size: 1.5em">📦 JAR</span> ⇒ <span style="font-size: 2em">📦 ZIP</span></p><!-- .element: class="fragment" -->

### sharing JS pain with Java crowd 🤬 <!-- .element: class="fragment" -->

---

## Web @ Nuxeo - plan 🗺

### Decouple Web UI ⚮

- Separate repositories
- **npm** packaging 📦
- Static / node.js hosting
- OAuth

---

## Web @ Nuxeo - plan 🗺

### UI templates 📐

- DM / DAM / CM / ...
- "Proper" frameworks (ie Vue.js)
- Richer element library
- Server ..* UI
- Configurable in Studio

---

## Low code

- Not no code! 👷 <!-- .element: class="fragment" -->
- Transparent upgrades 🤔 <!-- .element: class="fragment" -->
- Continuous delivery 😰 <!-- .element: class="fragment" -->

---

## Low code - plan 🗺

```html
<dom-module id="nuxeo-file-edit-layout">
    <nuxeo-input role="widget"
                 label="[[i18n('title')]]"
                 value="{{document.properties.dc:title}}">
    </nuxeo-input>
</dom-module>
```

```js
{
  id: "nuxeo-file-edit-layout"
  label: "title",
  field: "dc:title"
}
```
<!-- .element: class="fragment" -->

---

## Low code - plan 🗺

- Persist metamodel
- Actual build 💪
  - ```import 'my-layout.json'```
- meta 🚧 no-meta

---

## Cloud first ☁️

### Our cloud 🌈 <!-- .element: class="fragment" -->

- Deploy <!-- .element: class="fragment" -->

- Configure <!-- .element: class="fragment" -->

- Develop <!-- .element: class="fragment" -->

- Build <!-- .element: class="fragment" -->

- Test <!-- .element: class="fragment" -->

---

## UI development @ ☁️

### Typical flow 🖥️

- Checkout code
- Start dev server
- Edit
- Reload

---

## UI development @ ☁️

### Cloud flow 🌈 

- Go to Studio
- Launch dev sandbox
- Edit
- Reload

---

## UI development @ ☁️

### Build 

- Web UI + addons + project code & deps
- Build Docker image
- Push to registry

---

## UI development @ ☁️

### Dev sandbox 

- Web UI + addons code & deps
- Dev server (watch)
- Synched Studio workspace
- Reload

---

## Thank you

### Questions?
(5 mins)

### More questions? <!-- .element: class="fragment" --> 
Unconference <!-- .element: class="fragment" -->

### Even more questions? <!-- .element: class="fragment" --> 
🍺 🥃 <!-- .element: class="fragment" -->

