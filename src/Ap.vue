<script setup>
import SampleCom from './components/SampleCom.vue'
import {ref} from 'vue'

const name = ref('Juan Dela Cruz');
const course = ref('BS Information Technology');
const yearLvl = ref('2nd Year');

const price = 150;
const quantity = 3;
const total = ref(price * quantity);

const student = ref(0)

const status = ref('Offline');

const img = "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTnKyyWQ9a4qKRZZF6ZpD42YC6Vl-sdA4kOmjzKO9wP9A&s=10";

const website = "https://vuejs"

const isDisabled = false;

const mssg = ref('Light');


function increment() {
  student.value++;
}

function decrement() {
  student.value--;
}

function reset() {
  student.value = 0;
}


</script> 

<template>
    <h3>Student Information:</h3>
    <p>Name: {{ name }}</p>
    <p>Course: {{ course }}</p>
    <p>Year Level: {{ yearLvl }}</p>

    <h3>Task 2:</h3>
    <p>Price: ₱{{ price }}</p>
    <p>Quantity: ₱{{ quantity }}</p>
    <p>Total: ₱{{ total }}</p>

    <h3>Task 3:</h3>
    <h4>Student: {{ student }}</h4>
    <button @click="increment">Add Student</button>
    <button @click="decrement">Remove Student</button>
    <button @click="reset">Reset</button>
    <h4>Status: {{ student }}</h4>

    <h3>Task 4:</h3>
    <h4>Status: {{ status }}</h4>
    <button @click="status = 'Online'">Go Online</button>
    <button @click="status = 'Offline'">Go Offline</button>

    <h4>Status: {{ status }}</h4>

    <h3>Task 5:</h3>

    <img :src="img">

    <h3>Task 6:</h3>
    <a v-bind:href="website">Visit Vue.js</a>

    <h3>Task 7:</h3>
    <button :disabled="isDisabled">[Register]</button> 


 
</template>
