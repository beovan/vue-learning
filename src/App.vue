<script setup>
import {
  computed, reactive, ref
} from 'vue';
const firstName = ref('Nguyễn Văn')
const lastName = ref('A');

const fullName = computed({
  get() {
    return firstName.value + ' ' + lastName.value;
  },
  set(newValue){
    [firstName.value ,lastName.value] = newValue.split(',');
  }
  }
);

const changeFullName = () => { 
  fullName.value = 'Nguyễn Văn,B';
}
</script>

<template>
  <div>
    <p id="count">Fullname name: {{ fullName }}</p>
    <p id="count">FirstName name: {{ firstName }}</p>
    <p id="count">LastName name: {{ lastName }}</p>
    <button @click="changeFullName">Change fullName</button>
  </div>
</template>