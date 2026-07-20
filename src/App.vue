<script setup>
import  {ref} from 'vue' //for dynamic data binding
const curse = ref(0);
const name = ref('Juan Dela Cruz');

  function increment() {
  curse.value++;
}
  function decrement() {
  curse.value--;
}
  function reset() {
  curse.value = 0;
}


  const mssg = ref("Hello Idol");

   const img = "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTnKyyWQ9a4qKRZZF6ZpD42YC6Vl-sdA4kOmjzKO9wP9A&s=10"

   const website = "https://www.google.com";

   const isDisabled = true;
   const isEnabled = false;


</script>

<template>
  <HelloWorld />  


   <div>
    <!-- <h2>{{ curse }}</h2>
    <button @click="curse++">Increment</button>
    <button @click="curse--">Decrement</button>
    <button @click="curse = 0">Reset</button>
    <p>User: {{ name }}</p> -->

    <h2>{{ curse }}</h2>
    <button @click="increment">Increment</button>
    <button @click="decrement">Decrement</button>
    <button @click="reset">Reset</button>
    <p>User: {{ name }}</p>


<h2>{{ mssg }}</h2>
<button @click="mssg='love tika Idol'">Change Message</button>

<h2>
  <img :src="img">
</h2>

<a v-bind:href="website ">Google</a>

<h2>
  <button :disabled="isDisabled">Press</button>
</h2>

<h2>
  <p :class="{active: isEnabled}">Sample</p>
</h2>

<p :style="{color: '#9966CC', backgroundColor: '#000000' }">NYAWA</p>

</div>


</template>

<!--Design for isEnabled-->

<style>
.active {
  color: white;
  font-weight: bold;
}
</style>