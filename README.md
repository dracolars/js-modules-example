# Codecademy JS Modules ES6 Practice

> I used a python local server to run this.

> `python -m SimpleHTTPServer`

## Concepts
This section focuses on exporting, importing, and separating concerns (logic) in different js files / modules so we can reuse the logic for the same or different projects. 

### Export: 
This can be done in multiple ways. 

---
The most basic one is *named export*. This happens at the end of the file where we add the following sintax:

`export { valueA, valueB, valueC }; `

---
There is also *in-line export*. This happens at the declaration line.

`export const functionA = ... `

---
There is *default export*, which allows us to export without caring for the name of the function.

`export default const functionA = ...`

which can be imported as:

`import someFunction from './functionA.js'; `

---
Or we can define default as a set of variables, then export it.

`const default = { valueA, valueB, valueC } ; `

`export default`

which is the same as:

`export const default = { valueA, valueB, valueC } ; `

---

### Import: 
Examples of *named importing*:

`import { valueA, valueB, valueC } from './myfile.js'; `

`import valueA from './myfile.js'; `

---
Examples of *default importing*:

`import whateverName from './myfile.js'; `

---


### HTML Scirpt

It is very important that scripts that contain modules get the **type** attribute (type="module"):

` <script __type="module"__ src="main.js" defer></script> `

Otherwise, modules will probably get blocked by the browser.
