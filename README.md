# Forked library from: https://github.com/riophae/vue-treeselect

## All rights reserved to https://github.com/riophae/vue-treeselect

### Added Feature

- Input mask

### Getting Started

It's recommended to install vue-treeselect via npm, and build your app using a bundler like [webpack](https://webpack.js.org/).

```bash
npm install --save vue-treeselect-mask
```

This example shows how to integrate vue-treeselect with your [Vue SFCs](https://vuejs.org/v2/guide/single-file-components.html).

```vue
<!-- Vue SFC -->
<template>
  <div id="app">
    <Treeselect
      v-model="value"
      inputMask="+7(###)###-####"
      :multiple="true"
      :options="options"
    />
  </div>
</template>

<script>
// import the component
import Treeselect from "vue-treeselect-mask";
// import the styles
import "vue-treeselect-mask/dist/vue-treeselect.css";

export default {
  // register the component
  components: { Treeselect },
  data() {
    return {
      // define the default value
      value: null,
      // define options
      options: [
        {
          id: "a",
          label: "a",
          children: [
            {
              id: "aa",
              label: "aa",
            },
            {
              id: "ab",
              label: "ab",
            },
          ],
        },
        {
          id: "b",
          label: "b",
        },
        {
          id: "c",
          label: "c",
        },
      ],
    };
  },
};
</script>
```
