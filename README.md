# vue-visibility-trigger

> Vue component that emits an event when scrolled into view

[![vue-visibility-trigger demo](https://codesandbox.io/static/img/play-codesandbox.svg)](https://codesandbox.io/s/qkyolorn6w?module=%2Fsrc%2FApp.vue)

## Installation

Install the package from npm by running

```
$ yarn add vue-visibility-trigger
```

or

```
$ npm i vue-visibility-trigger
```

## Usage

Import, register and place the component in your Vue app. Attach a function to react to the 'scrolledIn' event with 'v-on:scrolledIn="..."' or '@scrolledIn="..."'.

```
<template>
  ...
    <VueVisibilityTrigger @scrolledIn="doSomething" />
  ...
</template>

<script>
import VueVisibilityTrigger from 'vue-visibility-trigger'

export default {
  ...
  components: {
    VueVisibilityTrigger
  }
};
</script>
```

## Dev

Running dev and example scripts require @vue/cli and @vue/cli-service-global to be installed. Install globally by running `npm i --g @vue/cli @vue/cli-service-global` or `yarn add global vue/cli @vue/cli-service-global`
