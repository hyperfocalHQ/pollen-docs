# Motivations

Pollen is built on the belief that CSS libraries should encourage consistency, be standards-driven, composable, extensible, unopinionated, functional, and highly performant.

### Consistency

One of the largest problems in modern CSS development is consistency and maintainability. Splitting code into modules and components can help, but only reduces the scope of the problem. Helper and utility classes can also help, but tightly couples styling to markup.

Thankfully CSS now has the same solution to this as other programming languages: variables. [CSS variables](https://developer.mozilla.org/en-US/docs/Web/CSS/--\*) are a new web specification that has already been adopted by all modern browsers, which Pollen relies heavily on. They allow us to create a single source of truth for a whole project. Which means we not only enforce consistency but can also instantly theme and [adapt on a global level](https://github.com/peppercornstudio/pollen-docs/tree/36d276304ba5f5bfcca4045de428c219e3e46302/docs/dynamic-theming/README.md) as well.

### Standards-driven

Libraries and frameworks should be built on top of existing or emerging standards wherever possible, allowing the platform to do the heavy lifting. Pollen is built on the belief that polyfilling functionality for the minority use-case (in this case: \<IE11) is almost always better than compromising performance, code-weight, and maintainability for the majority. The result is a future-facing and highly efficient toolset that only improves with time.

### Composable

Rather than a set of monolithic UI widgets, CSS libraries should provide small focussed tools that can be composed into your own custom components. Pollen takes this concept to the extreme, with a collection of single-purpose variables that can be mixed and matched for any use case. It encourages rapid development without the technical debt.

### Extensible

CSS libraries shouldn’t be constricting or add bloat, they should be a foundation that you can build upon and adapt. Pollen is designed to be extended and customised, used as a framework for creating your own custom design systems from prototype to production.

### Unopinionated

Pollen does not impose a design language or theme. It is a set of style-agnostic tools that can be composed and extended to form your own custom UI. 

### Functional

Pollen is a functional library. It's pure CSS that works in any environment — stylesheets, inline styles, CSS-in-JS, with any framework — without needing a buildstep or dependency chain. Its variables are used in individual properties, with no hidden side-effects or complex behaviour sets. This results in maintainable, scalable, and readable code.

### Performant

The entire Pollen framework weighs less than 1.3kb. Pollen will never grow into a monolithic framework, and you don’t need to worry about stripping it out when moving from prototype to production.
