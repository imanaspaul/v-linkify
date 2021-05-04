# Installation
```js
npm i vue-linkify-v2
```
# Install globally
```
import Vue from 'vue';
import vLinkify from 'vue-linkify-v2'; 
 
Vue.use(vLinkify)
```
# Use it in your component

```js
import vLinkify from 'vue-linkify-v2'; 
export default {
  components:{
    vLinkify,
  },
}
```
```
<v-linkify :html="your-data"/>
```

# Props
* html (type : String, required: true)