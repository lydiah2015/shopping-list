# shopping-list

## Lessong Learnt In Chapter1

-Creating and running a vue project
-Using CDN
-Create Basic Vue Components
-Using vue's unique directives
-Looping Over data and Controlling DOM states
-Data props and v-model binding
-Vue Lifecycle

## Instruction to build the shopping List

This activity aims to leverage knowledge thus far about the basic features of an SFC, such asexpressions, loops, two-way binding, and event handling.
This application should let users create and delete individual list items and clear the total list in one click.

-Build an interactive form in one component using an input bound to v-model.
-Add one input field to which you can add shopping list items. Allow users to add items by using
the Enter key by binding a method to the @keyup.enter event.
-Users can expect to clear the list by deleting all the items or removing them one at a time. To
facilitate this, you can use a delete method, which can pass the array position as an argument,
or simply overwrite the whole shopping list data prop with an empty array, [].

## Recommended IDE Setup

[VSCode](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (and disable Vetur) + [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin).

## Customize configuration

See [Vite Configuration Reference](https://vitejs.dev/config/).

## Project Setup

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Compile and Minify for Production

```sh
npm run build
```
