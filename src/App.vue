<!--
 Option API with data()
-->
<!--
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
-->
<!--
 Composition Api with setup() method
-->
<!-- 
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
-->
<!--
 Composition Api with <script setup>
-->
<!-- -->
<script setup>
import { ref } from 'vue';
    const courseName = ref('Laravel with vue js')
    const instructor = ref('Md Rasel Ahmed')
    let count = ref(0)
</script>

<template>
  <div class="text-center" > 
    <h2 class="text-xl font-semibold py-5">Course Name: {{ courseName   }}</h2>
    <p class="text-2xl">Instructor: {{ instructor }}</p>
    <button @click="count++" class="text-3xl font-bold inline py-2 px-4 bg-gray-200 shadow">+</button>
        <h1 class="font-bold text-3xl">Count Number: {{ count }}</h1>
    <button v-if="count > 0" @click="count--" class="text-3xl font-bold inline py-2 px-4 bg-gray-300 shadow">-</button>
  </div>
</template>

<style scoped>

</style>
