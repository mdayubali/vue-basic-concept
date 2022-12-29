<script setup>
import {ref,reactive} from 'vue'
    // non reactive way  
    const title = 'It comes from Databinding Component' 
    // ref reactive way with primitive data
    const CourseInstructor = ref("Eng. Ibrahim")
    let count = ref(0)
     // reactive reactive way with non-primitive data
    let courseDetails = reactive({
        CourseName: 'Laravel with vue Js',
        Duration: '72hours',
        price : 300
    })
    courseDetails.CourseName = "Larave & Vue Js"
</script>
<template>
    <div class="container text-center border shadow p-4 mt-8"> 
        <h1 class="text-xl font-semibold py-3">{{ title }}</h1>
        <button @click="count++" class="text-3xl font-bold inline py-2 px-4 bg-gray-200 shadow">+</button>
        <h1 class="font-bold text-3xl">Count Number: {{ count }}</h1>
        <input v-model="count" type="text" class="border w-1/2 p-3"> <br> 
        <h2 class="text-2xl text-center">Put Your Number in box</h2>
    <button v-if="count > 0" @click="count--" class="text-3xl font-bold inline py-2 px-4 bg-gray-300 shadow">-</button>
        <hr>
        <h1 class="text-2xl font-semibold py-3">Instructor Name: {{ CourseInstructor }}</h1>
        <table class="table-auto">
            <thead>
                <tr>
                    <th>Instructor Name</th>
                    <th>Course Name</th>
                    <th>Course duration</th>
                </tr>
            </thead>
            <tbody class="bg-white">
                <tr>
                    <td>{{ CourseInstructor }}</td>
                    <td>{{ courseDetails.CourseName }}</td>
                    <td>{{ courseDetails.Duration }}</td>
                </tr>
            </tbody>
           
        </table>
    </div>
</template>
<style scoped>
    .container{
        width: 850px;
    }

</style>