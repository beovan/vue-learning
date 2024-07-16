
<script setup>
import { ref, reactive } from "vue";
const users = ref([
  { name: "john", age: 30 , isActive: true },
  { name: "cho", age: 30 , isActive: false },
  { name: "meo", age: 30 , isActive: true },

]);
</script>

<template>
  <div>
   <div>
    <ul>
      <template v-for="(user, index) in users" :key="user.name">
        <li v-if="user.isActive" :key="user.name">
          {{ user.name }}:  {{ user.isActive ? "Active" : "Deactive" }}({{ index }})
        </li>
      </template>
    </ul>
   </div>
</div>
</template>