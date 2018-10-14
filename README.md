# vue-visibility-trigger

> Vue component that emits an event when scrolled into view

## Installation

Install the package from npm by running

```
$ yarn add 'vue-visibility-trigger'
```

or

```
$ npm install --save 'vue-visibility-trigger'
```

## Usage

Import, register and place the component in your Vue app. Attach a function to react to the 'scrolledIn' event with 'v-on:scrolledIn="..."' or '@scrolledIn="..."'.

```
<template>
  ...
    <vue-visibility-trigger @scrolledIn="doSomething" />
  ...
</template>

<script>
import VueVisibilityTrigger from 'vue-visibility-trigger'

export default {
  ...
  components: {
    "vue-visibility-trigger": VueVisibilityTrigger
  }
};
</script>
```

[![vue-visibility-trigger demo](https://codesandbox.io/static/img/play-codesandbox.svg)](https://codesandbox.io/s/qkyolorn6w?module=%2Fsrc%2FApp.vue)
