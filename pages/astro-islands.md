---
class: flex flex-col
transition: fade
---

# Astro Islands

<style>
  h2 {
    font-size: 2.8rem;
    line-height: 3.2rem;
  }
</style>

<v-click at="+1">
<div class="text-center my-auto">

## Un Composant UI dynamique est un Island

</div>
</v-click>

<v-click at="+1">

### Définitions

Composant UI : Composant provenant d'un framework ou d'une bibliothèque web

</v-click>

<!--
[click]

[click]
- Exemples : Composant React, composant Vue
-->

---
class: flex flex-col
transition: fade
---

# Astro Islands

<AstroIslands />

<!--
- Header : élément dynamique et clé
- Image carousel : élément dynamique et décoratif
- Autres : éléments statiques
-->

---
transition: fade
---

# Astro Islands

`./src/pages/index.astro`

````md magic-move
```astro {*|11}
---
import { Layout } from "./Layout.astro";
import { Header } from "./Header.jsx";
import { Sidebar } from "./Sidebar.astro";
import { Footer } from "./Footer.astro";
import { Details } from "./Details.svelte";
import { ImageCarousel } from "./ImageCarousel.vue";
---

<Layout>
  <Header />
  <Sidebar />
  <main>
    <Details />
    <ImageCarousel />
  </main>
  <Footer />
</Layout>
```

```astro {11|15}
---
import { Layout } from "./Layout.astro";
import { Header } from "./Header.jsx";
import { Sidebar } from "./Sidebar.astro";
import { Footer } from "./Footer.astro";
import { Details } from "./Details.svelte";
import { ImageCarousel } from "./ImageCarousel.vue";
---

<Layout>
  <Header client:load />
  <Sidebar />
  <main>
    <Details />
    <ImageCarousel />
  </main>
  <Footer />
</Layout>
```

```astro {15|11,15|*}
---
import { Layout } from "./Layout.astro";
import { Header } from "./Header.jsx";
import { Sidebar } from "./Sidebar.astro";
import { Footer } from "./Footer.astro";
import { Details } from "./Details.svelte";
import { ImageCarousel } from "./ImageCarousel.vue";
---

<Layout>
  <Header client:load />
  <Sidebar />
  <main>
    <Details />
    <ImageCarousel client:visible />
  </main>
  <Footer />
</Layout>
```
````

<!--
- Tous les composants UI seront rendus statiques

[click]

[click]
- Header devient un Island dont le script JS sera chargé au chargement de la page

[click]

[click]
- Image carousel devient un Island dont le script JS sera chargé lorsque l'élément sera proche de devenir visible à l'utilisateur

[click]
- Les scripts JS des deux Islands seront chargés en parallèle (si l'Image carousel est visible dès le chargement de la page)
-->

---

# Astro Islands

<v-clicks at="+1">

- Composant UI statique par défaut
- Directive `client:*` pour convertir en Island
- Contrôle fin sur le rendu client
- Chargement parallélisé
- Isolation
- Partage d'états via props ou stores

</v-clicks>

<!--
[click]

[click]

[click]

[click]

[click]
- Possibilité d'avoir plusieurs Islands de framework différent sur la même page sans conflit

[click]
- nanostores : Bibliothèque de stores atomiques avec de nombreuses intégrations (Vanilla JS, Angular, React, Vue, Svelte, ...)
-->
