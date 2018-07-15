# vue-json-to-html

**Status: beta** 

**:tongue: Vue component for generating equal HTML from Json/JS-Object**

## Table of contents

- [Usage](#usage)
- [Component props](#component-props)

## Usage
Install component to your project:
```
npm install vue-json-to-html
yarn add vue-json-to-html
```

Import and include to Vue Instance installed component:
```
import JsonToHtml from 'vue-json-to-html'

export default {
  components: {
    JsonToHtml
  }
  ...
}
```

Use component in template:
```
<template>
  <div id="content">
    <JsonToHtml :json="json" :bem="true" rootClassName="wrapper" rootTagName="section" :inheritClassName="false"/>
  </div>
</template>
```

## Component props

Prop | Type | Default | Description
  --- | --- | --- |---
  json | `Json(JS Object)` | required | DOM will rendered such as object structure. Each elements will have necessary classNames from json keys.
  bem | `Boolean` | false | Generate classNames with BEM methodology.
  inheritClassName | `Boolean` | true | Generate classNames with inherited parent class name. For using BEM must be a `true`. 
  bem | `Boolean` | false | Generate classNames with BEM methodology.
rootClassName | `String` | undefined | ClassName for root element in `<JsonToHtml/>`, using for inherited parent class name from root element 
rootTagName | `String` | 'div' | TagName for root element in `<JsonToHtml/>`.
