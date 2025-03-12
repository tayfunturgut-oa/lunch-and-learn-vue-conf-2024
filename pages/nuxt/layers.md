# Nuxt Layers

You can extend various Nuxt applications to reuse components, utils, and configuration.

## Domain-Driven Design (DDD)

````md magic-move
``` {all|2,5,7}
+- src/
    +- components/ # logic grouped by *concerns*
    |   +- blog/
    |   +- home/
    +- content/
    |   +- blog/
    +- pages/
    |   +- blog.vue
    |   +- index.vue
    +- ...
```

```{2,7|all}
+- src/
    +- blog/ # logic grouped by *domains*
    |   +- components/
    |   +- content/
    |   +- pages/
    |       +- blog.vue
    +- home/
    |   +- components/
    |   +- pages/
    |       +- index.vue
    +- ...
```
````

---
layout: two-cols-header
---

# Nuxt Layer vs. Module / Package

::left::

## Module/Package

- <u>Lower level</u> and more specific.

- Integrating <u>external</u> libraries.

- Requires additional knowledge to author libraries.

::right::

## Nuxt Layer

- Higher level and more <u>abstract</u>.

- Internal and just like writing another standard Nuxt app.

---
layout: two-cols-header
---

## Nuxt Live Coding (...sort of)

::left::

### A whitelabel Nuxt app

<br>

<img alt="Nuxt App" src="/nuxt-app.png" width=400 />

::right::

### Base Layers

<br>

- `bmv` app: A database of books, music, and videos. Similar to TMDB and Discogs.

- Design system: A personal design system and library, containing UI components and utilities.

### Final App

<br>

- A watchlist app collecting my favorite films.

---
layout: cover
---

# Thank You 🍀
