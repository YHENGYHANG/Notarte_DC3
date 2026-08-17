<script setup>
import Emits from './components/Emits.vue'
import TryAlert from './components/TryAlert.vue'
import RegistrationForm from './components/RegistrationForm.vue'
import DefineProps from './components/DefineProps.vue'

import { ref } from 'vue'

const message = ref('')

function handleNotify(info) {
  // Update the message when the event is received
  message.value = `Name: ${info.name},
  Age: ${info.age}`
}   

function handleAlert(alert) {
  // Update the message when the alert event is received
  message.value = `${alert.message}`
}

</script>

<template>
  <div>
    <!-- For using basic defineEmits-->
     <h4>DEFINE EMITS</h4>
    <Emits @notify="handleNotify" />
    <p>{{ message }}</p>
    <hr></hr>

    <!--For using Simple Alert using defineEmits-->
    <h4>SIMPLE ALERT USING EMITS</h4>
    <TryAlert @alerts="handleAlert" />
    <hr></hr>

    <!-- For Registration Form-->
     <h4>REGISTRATION FORM</h4>
    <RegistrationForm />

    <hr></hr>

    <!-- For defineProps -->
    <h4>DEFINE PROPS</h4>
    <DefineProps name="Alice" age="25" email="not@gmail.com" />

  </div>
</template>  