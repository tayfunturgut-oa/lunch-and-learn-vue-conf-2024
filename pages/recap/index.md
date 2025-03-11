---
layout: center
---

## Major Updates and Developments in 2024

**End of Vue 2 and Focus on Vue 3:** Vue 2 reached end-of-life as of December 31, 2023, marking 2024 as the first full
year with the community centered on Vue 3.

<sub>
This transition pushed developers to migrate legacy projects and fully
embrace Vue 3’s modern features. All official support and new improvements in 2024 targeted Vue 3, solidifying it as the
default Vue platform.
</sub>

**Vue 3.4 “Slam Dunk” (late 2023):** Released at the very end of 2023, Vue 3.4 brought significant under-the-hood
enhancements that carried into 2024. It introduced a rewritten template compiler that is **2× faster** and a more
efficient reactivity system to reduce unnecessary re-renders. These changes improved compilation speed (benefiting build
tools and IDE integrations) and made data updates more performant, with no breaking changes.

---
layout: center
---

## Vue 3.5 “Tengen Toppa Gurren Lagann” (September 2024)

The **major release of 2024** was Vue 3.5. Although labeled a “minor” update by the team, it delivered substantial
improvements without breaking backwards compatibility. Notable enhancements included:

- **Reactivity Performance Boosts:** A core reactivity refactor improved execution speed and dramatically cut memory
  usage (about **56% less memory** overhead). Large reactive data structures (like big arrays) saw up to **10× faster**
  update handling in certain cases.
- **Server-Side Rendering (SSR) Improvements:** Vue 3.5 introduced features like **lazy hydration** for SSR.
    - <sub>This allows
      delaying or chunking the hydration (activation) of server-rendered DOM, improving load performance for large
      pages.
      Other SSR tweaks (a new `useId()` API and allowing controlled hydration mismatches) enhanced Vue’s ability to
      handle
      modern hydration and streaming patterns.</sub>

---
layout: center
---

**New Minor Features:** Useful additions like reactive destructuring of props (now enabled by default) simplified
component code. For example, using ES destructuring on `defineProps` is now reactive out of the box, eliminating
verbose workarounds in `<script setup>`. Utilities like `useTemplateRef()` and a deferred teleport API were added to
expand Vue’s component capabilities. All these features aimed to streamline development while maintaining Vue’s gentle
learning curve.

````md magic-move
```ts
// Example of ES destructuring with reactive props
const { title, content } = defineProps({
  title: String,
  content: String
});
```

```vue
<template>
  <div>
    <h1 ref="titleRef">Hello, World!</h1>
    <button @click="changeTitle">Change Title</button>
  </div>
</template>

<script setup lang="ts">
import { useTemplateRef } from 'vue';

const titleRef = useTemplateRef('titleRef');

const changeTitle = () => {
  if (titleRef.value) {
    titleRef.value.textContent = 'Title Changed!';
  }
};
</script>
```
````

---
layout: center
---

## Vue Ecosystem and 2024 Developments

Beyond the core library, the **Vue ecosystem** also saw continued refinement in 2024. The official router, state
management (Pinia), and other tooling kept pace with Vue 3 updates, ensuring compatibility and improvements. Vue CLI
usage further gave way to Vite-based build setups, so by 2024 most Vue projects were using faster bundler workflows
out-of-the-box. In sum, 2024’s developments focused on performance and polish: making Vue 3 more robust, efficient, and
convenient for projects of all sizes.

---
layout: center
---

## Adoption Trends in 2024

Vue.js maintained a **strong and growing presence** among front-end developers in 2024, though it continues to sit
behind React in overall usage. Multiple industry surveys and usage reports give insight into Vue’s position:

- **Growing Usage (Surpassing Angular):** By 2023/2024, Vue solidified itself as the **#2 front-end framework** (behind
  React) in many surveys, overtaking Angular in popularity. For example, one report shows React used by ~35.9% of
  developers, Angular by 25.1%, and Vue by about 17.3% (ranked 7th overall among frameworks).
    - <sub>This indicates Vue has
      pulled ahead of Angular in adoption among developers, a trend confirmed by the State of JS 2023 survey.</sub>
- **Web Market Share:** In terms of websites in the wild, Vue still has a niche but notable share. Statistics toward the
  end of 2024 show React used on roughly **4.9% of all websites** (about 6.0% of those using any JS library), whereas
  Vue is used on about **0.8% of all websites** (~1.0% of the JS library market). Another source tracked over **11
  million live sites using React** versus about **2 million using Vue**.

---
layout: center
---

- **Developer Interest and Satisfaction:** Vue.js enjoys a very enthusiastic community, reflected in metrics like GitHub
  stars and “most-loved” rankings. By late 2024, Vue’s repository had amassed around **197k stars on GitHub**, putting
  it on par with React’s stargazer count. In Stack Overflow’s 2024 developer survey, Vue.js again ranked among the **top
  most “wanted” web frameworks**.
- **Community Engagement:** The Vue community in 2024 was very active and supportive, with healthy participation in
  conferences and online forums, and direct core team communication from key contributors.

In summary, **Vue performed well in 2024 in terms of developer interest and community growth**, chipping away at
Angular’s share and solidifying its reputation as a top-tier front-end tool.

---
layout: center
---

## Vue.js vs React in 2024 – Performance Comparison

Both Vue 3 and React 18 are **high-performance frameworks** capable of powering large-scale applications, but they have
different performance philosophies. React relies on a **virtual DOM diffing** algorithm: when state changes, React
re-renders component subtrees and diffs the virtual DOM to update the real DOM efficiently. Vue 3, by contrast, combines
a virtual DOM with a **reactivity system** that tracks fine-grained dependencies, ensuring components only re-run when
the specific reactive data they use has changed. This reactive tracking can reduce unnecessary work and is one reason
Vue often excels at update performance.

In practice, by 2024 the two frameworks showed **comparable real-world performance**, with each having slight edges in
different scenarios. Benchmarks showed near-identical scores on performance metrics, with initial render times on the
order of <1s and millisecond-level UI updates in both frameworks.

---
layout: center
---

## Vue’s Roadmap and Goals for 2025

Looking ahead, the Vue.js core team outlined a vision for **incremental improvements** in 2025:

- **“Vapor Mode” – Pushing Performance Further:** An innovative rendering mode aimed at eliminating virtual DOM overhead
  by compiling components into optimized JavaScript, thus achieving performance akin to compiler-only frameworks.
- **No Imminent Vue 4 – Continued Evolution of Vue 3:** The core team has signaled that there are **no immediate plans
  for a Vue 4 release**, focusing instead on iterative improvements to Vue 3.x.

---
layout: center
---

## Vue’s Roadmap and Goals for 2025

- **Enhanced Developer Experience:** Plans to default to `<script setup>` and TypeScript in single-file components to
  improve the development workflow.
- **Ecosystem Updates (Nuxt, Pinia, Tooling):** Anticipation of Nuxt 4, updates in Pinia v3, and evolving tooling with
  Vite, aligning with Vue’s improvements.
- **Stability and Backward Compatibility:** Commitment to maintaining stability, ensuring that upgrades remain painless
  with minimal breaking changes.
- **Potential New Features and Focus Areas:** Exploration of concepts like **“signals”** for reactivity, improvements in
  server-side rendering, and better integration with emerging web standards.
