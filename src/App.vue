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
import Databinding from './Databinding.vue';
    const courseName = ref('Laravel with vue js')
    const instructor = ref('Md Rasel Ahmed')
    let count = ref(0)
</script>

<template>
  <div class="text-center" > 
    <h2 class="text-xl font-semibold py-5">Course Name: {{ courseName   }}</h2>
    <p class="text-2xl">Instructor: {{ instructor }}</p>

  </div>
  <hr>
  <Databinding></Databinding>
</template>

<style scoped>

</style>
