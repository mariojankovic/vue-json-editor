NOTE: This is a fork and translation of [dirkliu/vue-json-editor](https://github.com/dirkliu/vue-json-editor)

![screenshot](https://i.imgur.com/r1QRchE.png)

# vue-json-editor
A JSON schema editor for Vue.js.

## Dependencies
vue.js

## Properties
**v-model**: required, json object of [json object] component 
**:showBtns**: boolean, whether to display the save button, the default is true 
**@json-change**: fires upon change

# How to use
## 1. Install vue-json-editor using npm
```
npm install vue-json-editor --save
```
## 2. Use vue-json-editor in your vue component
```vue
<template>
  <div>
    <vue-json-editor v-model="json" :show-btns="true" @json-change="onJsonChange"></vue-json-editor>
  <div>
</template>

<script>
  // Import vue-json-editor module
  import vueJsonEditor from 'vue-json-editor'
  export default {
    data () {
      json: {
        msg: 'demo of jsoneditor'
      }
    },

    // Inject vueJsonEditor component
    components: {
      vueJsonEditor
    },

    methods: {
      onJsonChange (value) {
        console.log('value:', value)
      }
    }
  }
</script>
```
