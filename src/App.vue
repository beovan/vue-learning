<script setup>
const message = 'hello world';
const rawHtml = '<span style="color: red">This should be red.</span>';
const buttonId = 'button-id';
  const buttonClass = 'btn btn-rounded';
  const isButtonDisabled = true;
  const objectOfAttrs = {
  id: 'container',
  class: 'wrapper'
}
</script>

<template>
  <div>
    <h1>Syntax</h1>
    <p>
      Message: {{ message }}
    </p>
    <span v-html="rawHtml">
    </span>
    <button  :id="buttonId" :class="buttonClass" :disabled="isButtonDisabled" >Click here</button>
    <button v-bind="objectOfAttrs">Click here!!!</button>
 </div>
</template>