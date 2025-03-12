# Nuxt Overview

Nuxt is a free and open-source full-stack framework, and it provides an ecosystem:

- Core engine: [nuxt](https://nuxt.com/docs/getting-started/introduction)
- Bundler: [vite](https://vite.dev/)
- Command line interface: [nuxi](https://github.com/nuxt/cli)
- Server engine: [nitro](https://nitro.build/)
- Development kit: [@nuxt/kit](https://nuxt.com/docs/guide/going-further/kit) (for authoring packages)

---

# Nuxt Directory Structure

`Nuxt 3`'s opinionated directory structure:

```md {all|10,13,14|14|2|7|10}
components/
composables/
content/
layouts/
middleware/
modules/
pages/
plugins/
public/
server/
shared/
utils/
app.vue
nuxt.config.ts
```

---
layout: two-cols
---

# Some Nuxt Features

## 🔮 Server Engine

Nuxt 3 comes with `Nitro`, a new open-source server engine based on `unjs/h3`.

- Next gen server with built-in caching and data fetching.
- Minimalistic as in [Unix philosophy](https://en.wikipedia.org/wiki/Unix_philosophy).
- Runtime agnostic: Node.js, bun, deno, etc.
- Built-in support for K/V storage

::right::

<h1 class="invisible">Invisible</h1>

## ✨ Auto-Imports

<br>

````md magic-move {lines: true}
```vue {all|2-3}
<script setup lang="ts">
import { ref } from 'vue';
const counter = ref(0);

const handleClick = () => {
  counter.value++;
};
</script>

...
```

```vue {all|2}
<script setup lang="ts">
const counter = ref(0); // auto-imported

const handleClick = () => {
  counter.value++;
};
</script>

...
```

````

Thanks to its opinionated directory structure, Nuxt can auto-import your `components/`, `composables/` and `utils/`.

<style>
.invisible {
  visibility: hidden;
}
</style>

---

# Server-Side Rendering (SSR)

### Rendering

<br>

- Both the browser and server can *interpret* JavaScript code to turn Vue.js components into *HTML elements*. This step is called **rendering**.

<br>

### Universal Rendering

<br>

- Similar to traditional server-side rendering performed by PHP or Ruby applications. 

<br>

### Client-Side Rendering

<br>

- Out of the box, a traditional `Vue.js` application is rendered in the browser (or client). Then, Vue.js generates HTML elements after the browser downloads and parses all the JavaScript code.

---

## And Many More...

<br>

- Nuxt Layout

- Modules

- `TypeScript` auto-generated types

- `ESLint` support out of the box

<br>

Head out to the [Key Concepts](https://nuxt.com/docs/guide/concepts/) section of [Nuxt's Guide](https://nuxt.com/docs/guide) to learn more.

