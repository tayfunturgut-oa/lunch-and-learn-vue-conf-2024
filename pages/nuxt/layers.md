# Nuxt Layers

You can extend various Nuxt applications to reuse components, utils, and configuration.

## Domain-Driven Design (DDD)

````md magic-move
```
+- src
    +- components
    |   +- blog
    |   |   +- ...
    |   +- home
    |       +- ...
    +- content
    |   +- blog
    |       +- ...
    +- pages
    |   +- blog.vue
    |   +- index.vue
    +- ...
```

```
+- src
    +- blog
    |   +- components
    |   |   +- ...
    |   +- content
    |   |   +- ...
    |   +- pages
    |       +- blog.vue
    +- home
    |   +- components
    |   |   +- ...
    |   +- pages
    |       +- index.vue
    +- ...
```
````

---

## Nuxt Layer vs. Module vs. Package

---

## Layer
