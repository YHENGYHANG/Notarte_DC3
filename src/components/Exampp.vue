<script setup>
    defineProps({
        BookName: String,
        Author: String,
        isSold: Boolean
    })
</script>

<template>
    <div class="card">
        <h2 :class="{red:isSold}">Book: {{ BookName }}</h2>
        <h3>Author: {{ Author }}</h3>
        

    </div>
</template>

<style>
.red {
    color: red;
    font-weight: bold;
}

</style>