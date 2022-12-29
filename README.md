# select-unselect

This template should help get you started developing with Vue 3 in Vite.

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
# Two types of Vue API
 ## Option API & Composition API (Modern)
In Option API- Both has export default and here data() method return an object. 
  ## example 
```sh 
<script>
export default {
    data(){
        return{
            courseName: 'Laravel with Vue Js',
            instructor: 'Rasel Ahamed',
            count: 0,
        }
    }
}
</script>
```
On the other hand, Composition API setup() method return all variable as an object.For result reactivity,finally must have to the return all variable as an object. 
Firstly, have to import the ref object from the vue  after scripts and all the variable value wrap with ref("value") function.
```sh
<script>
import { ref } from 'vue'
 export default {
  setup(){
    const courseName = ref('Laravel with vue js')
    const instructor = ref('Md Rasel Ahmed')
    let count = ref(0)
    return {courseName, instructor, count}
  }
  
 }
</script>
```
Another composition API (updated) is scripts setup way. <script setup> it’s easy to use and reduce the code. Just import the ref object and wrap the variable value into ref(”value”) and it’s no need to return for reactivity and no need to export default.

```sh
<!-- -->
<script setup>
import { ref } from 'vue';
    const courseName = ref('Laravel with vue js')
    const instructor = ref('Md Rasel Ahmed')
    let count = ref(0)
</script>
```
