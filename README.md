# Vue 3 Code Input

> 🎉A verification code input for vue 3
> This is a fork of zlayine's vue3-verification-code-input with a lot more improvements on the way and active maintainance.

[![NPM](https://img.shields.io/npm/v//@toneflix-code/vue3-code-input.svg)](https://www.npmjs.com/package//@toneflix-code/vue3-code-input) [![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)

[![NPM](https://nodei.co/npm//@toneflix-code/vue3-code-input.png)](https://nodei.co/npm/@toneflix-code/vue3-code-input)

## Demo

![Vue 3 Code Input Demo](https://github.com/toneflix-forks/vue3-code-input/blob/master/public/demo_image.png?raw=true)

## Install

```bash
npm install --save @toneflix-code/vue3-code-input
```

## Usage

```jsx
<template>
  <code-input
    @complete="completed = true"
    :fields="3"
    :fieldWidth="56"
    :fieldHeight="56"
    :required="true"
    v-model="code"
  />
  <button class="btn" :disabled="!completed">
    Continue
  </button>
</template>

<script setup>
import CodeInput from "@toneflix-code/vue3-code-input";
import { ref } from "vue";

const completed = ref(false);
const code = ref('');
</script>
```

## PropTypes

|        Key       |  Type  |              Desc                |
| :--------------: | :----: | :------------------------------: |
|      borders     | string | Borders to show (Default: btlr)  |
|      fields      | number |    The count of characters       |
|     disabled     |  bool  |      Disable the inputs          |
|     required     |  bool  |      require the inputs          |
|    fieldWidth    | number |          input width             |
|    fieldHeight   | number |         input height             |
|       title      | string |       code input title           |
|     className    | string |          class name              |
|   primaryColor   | string |   The main component color       |
|  secondaryColor  | string | The alternate component color    |
|     hasError     |  bool  |    If the input has an error     |
|   errorMessage   | string | The actual error message to show |

## EmitTypes

|   Key    | Type |              Desc               |
| :------: | :--: | :-----------------------------: |
|  change  | func |   Trigger on character change   |
| complete | func | Trigger on all character inputs |

## License

MIT
