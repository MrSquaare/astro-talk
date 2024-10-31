# Syntaxe de template

<style>
  .shiki {
    font-size: 0.6rem !important;
    line-height: 0.8rem !important;
  }
</style>

```astro {*|1-4|6-9|11-15|17-24|*}
---
const title: string = "Hello, Astro!";
const alertMessage: string = "This is an alert message!";
---

<div>
  <h1>{title}</h1>
  <button id="clickMe" data-alert-message={alertMessage}>Click me</button>
</div>

<style>
  h1 {
    color: red;
  }
</style>

<script>
  const button: HTMLButtonElement = document.querySelector("#clickMe");
  const alertMessage: string = button.dataset.alertMessage;

  button.addEventListener("click", () => {
    alert(alertMessage);
  });
</script>
```

<!--
[click]
- Frontmatter
- JavaScript
- Côté serveur
- Déclarations pas partagées avec le client
- Déclarations sérialisées
- TypeScript supporté

[click]
- HTML
- Standard
- Expressions comme JSX

[click]
- CSS
- Standard
- Scope composant par défaut
- Scope global via `is:global`
- Bundle par défaut (Inline si > 4 Ko)
- Brut via `is:inline`
- Inclus une seule fois si plusieurs éléments

[click]
- Script
- JavaScript
- Côté client
- Déclaration pas partagées avec le serveur
- Bundle par défaut
- Brut via `is:inline`
- TypeScript supporté
- Inclus une seule fois si plusieurs éléments

[click]
-->
