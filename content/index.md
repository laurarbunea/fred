---
title: 'Hello, '
alias: 'Yo, dawg!'
template: 'index.html'
weight: 0
hide_from_nav: false
---
## Code structure
To keep Fred happy we have organised our front end code into sections (based on a [ITCSS architecture](https://www.xfive.co/blog/itcss-scalable-maintainable-css-architecture/) ).

Those sections are as follows:

1. **settings** – used with preprocessors and contain font, colors definitions, etc.
2. **tools** – globally used mixins and functions. It’s important not to output any CSS in the first 2 layers.
3. **generic** – reset and/or normalize styles, box-sizing definition, etc. This is the first layer which generates actual CSS.
4. **elements** – styling for bare HTML elements (like H1, A, etc.). These come with default styling from the browser so we can redefine them here.
5. **objects** – class-based selectors which define undecorated design patterns, for example media object known from OOCSS
6. **components**  – specific UI components. This is where majority of our work takes place and our UI components are often composed of Objects and Components
7. **utilities** – utilities and helper classes with ability to override anything which goes before in the triangle, eg. hide helper class
8. **theming** – website themes


## How the Code is documented
To document our code we use an NPM package [mark-down-styleguide-generator](https://www.npmjs.com/package/markdown-styleguide-generator) 
This tool will search all your style files (your .css, .scss _partial.scss, .whatever) for comments and create a html file living style guide for your developers to use!



