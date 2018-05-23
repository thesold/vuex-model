# X-Model

[![npm](https://img.shields.io/npm/v/@thesold/x-model.svg?style=for-the-badge)](https://www.npmjs.com/package/thesold/x-model)

Authors:

* [Marco Mark](mailto:m2de@outlook.com)

## Overview

Vue.js renderless component to work with Vuex when v-model is not suitable because changes should be commited via mutations. X-model will disconnect the v-model passed in and make it non-reactive allowing you to listen to the updated event to commit changes to your Vuex Store.

### Installation

```sh
npm install @thesold/x-model
```

```js
import XModel from '@thesold/x-model'

Vue.component(XModel)
```

### Usage

```html
<x-model :value="reactiveProp" @input="updateModel">
    <template slot-scope="{ frozenValue }">
        <!-- input/updateModel will be fired when frozenValue is changes, however reactiveProp will not receive any updates from the component -->
    </template>
</x-model>
```
