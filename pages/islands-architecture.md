---
class: flex flex-col
transition: fade
---

# Architecture Islands

<style>
  h2 {
    font-size: 2.8rem;
    line-height: 3.2rem;
  }
</style>

<v-click at="+1">
<div class="text-center my-auto">

## Décomposition de la page en éléments isolés, rendus parallèlement et progressivement

</div>
</v-click>

<v-click at="+1">

### Contexte

- Développé et documenté par Jason Miller en 2020

</v-click>

<!--
[click]

[click]
- Première mention par Katie Sylor-Miller en 2019
- Jason Miller : Créateur de Preact
-->

---
class: flex flex-col
---

# Architecture Islands

<SSRHydrationIslands />

<!--
- Header et image carousel : éléments dynamiques
- Autres : éléments statiques
- SSR : Tout est rendu en même temps, prend du temps
- Progressive Hydration (Partial Hydration) : Les éléments clés sont rendus en même temps, améliorant le temps de chargement au détriment des éléments secondaires
- Islands : Rendu parallèlement, chargement des scripts uniquement pour les éléments dynamiques
-->
