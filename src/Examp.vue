<script setup>
// import Activity from './components/Activity.vue'
import Exampp from './components/Exampp.vue'
</script>


<template>
    <!-- <Activity /> -->
    <!-- <Exampp name="John" course="Mathematics" /> -->

    <Exampp
        BookName="Harry Potter and the Sorcerers Stone"
        Author="J. Rowling" :isSold="false"
        />
    <Exampp
        BookName="Harry Potter: The Goblet of Fire"
        Author="J. Rowling" :isSold="true"
        />

    <Exampp
        BookName="Harry Potter: Deathly Hallows"
        Author="J. Rowling" :isSold="false"
        />



</template>