//F                                                           
<script setup>
import {ref, computed, h} from 'vue'

    const sports = ref(['Basketball', 'Volleyball', 'Football', 'Tennis'])

    const showNotice = true

    const score = ref(67)

    const fname = ref('Michael')
    const lname = ref('Jordan')

    const full = computed(() => fname.value + ' ' + lname.value)


</script>

<template>
        <div>
            <h2>1:</h2>
            <ul>
                <li v-for="sport in sports" :key="sport">
                    {{ sport }}
                </li>
            </ul>

            <h2>2:</h2>
            <p v-show="showNotice">Welcome to Dashboard</p>

            <h2>3:</h2>
            <p v-if="score >=90">Excellent!</p>
            <p v-else-if="score >=75">Passed!</p>
            <p v-else>Failed!</p>

            <h2>4:</h2>
            <p>{{ full }}</p>




        </div>





</template>
