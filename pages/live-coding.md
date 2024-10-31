---
layout: cover
class: text-center
background: https://astro.build/assets/wallpapers/desktop/rays.png
transition: slide-up
---

# Live coding

## Construire un blog

---
transition: slide-up
---

# Initialiser le projet

<v-click at="+1">

1. Créer un nouveau projet Astro
```bash
pnpm create astro@latest # ou npm ou yarn
```

</v-click>

<v-click at="+1">

2. Suivre les instructions

</v-click>

<v-click at="+1">

3. Lancer le serveur de développement
```bash
cd ./blog
pnpm dev
```

</v-click>

---
transition: slide-up
---

# Construire le projet

<v-click at="+1">

1. Lancer le script de construction
```bash
pnpn build
```

</v-click>

<v-click at="+1">

2. Lancer le serveur de rendu
```bash
pnpm preview
```

</v-click>

---
transition: slide-up
---

# Ajouter un formulaire de contact

<v-clicks at="+1">

1. Créer le composant `src/components/ContactForm.astro`
2. Créer la page `src/pages/contact.astro`
3. Ajouter le lien vers la page dans la navigation

</v-clicks>

---
transition: slide-up
---

# Ajouter une intégration : Tailwind CSS

<v-click at="+1">

1. Ajouter Tailwind CSS via `astro add`

```bash
pnpx astro add tailwindcss
```

</v-click>

<v-click at="+1">

2. Suivre les instructions

</v-click>

<v-click at="+1">

3. Installer le plugin `@tailwindcss/forms`

```bash
pnpm add -D @tailwindcss/forms
```

</v-click>

<v-click at="+1">

4. Styliser le composant `src/components/ContactForm.astro`

</v-click>

<v-click at="+1">

5. Styliser la page `src/pages/contact.astro`

</v-click>

---
transition: slide-up
---

# Envoyer le formulaire

<v-click at="+1">

1. Lancer Maildev, un serveur SMTP local

```bash
docker run -p 1080:1080 --rm maildev/maildev
```

</v-click>

<v-click at="+1">

2. Ajouter Nodemailer

```bash
pnpm add nodemailer
```

</v-click>

<v-click at="+1">

3. Écouter la méthode POST sur la page `src/pages/contact.astro`

</v-click>

<v-click at="+1">

4. Implémenter la logique d'envoi du mail

</v-click>

---
transition: slide-up
---

# Vérifier les données

<v-clicks>

1. Créer un schéma avec Zod
2. Valider les données du formulaire
3. Afficher les erreurs et restaurer les données saisies

</v-clicks>

---
layout: cover
class: text-center
---

# Tada !