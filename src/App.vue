<script setup>
const message = 'hello world';
const rawHtml = '<span style="color: red">This should be red.</span>';
const buttonId = 'button-id';
  const buttonClass = 'btn btn-rounded';
  const isButtonDisabled = false;
  const objectOfAttrs = {
  id: 'container',
  class: 'wrapper',
  style: {
    color: 'blue'
  }
}
const number = 0;
const listString = "a,b,c,d,e,f,g,h,i,j"
const convertToId = (data) => data.split(',').join('-');
</script>

<template>
  <div>
    <h1>Syntax</h1>
    <p>
      Message: {{ message }}
    </p>
    <span v-html="rawHtml">
    </span>
    <button  :id="buttonId" :class="buttonClass" :disabled="isButtonDisabled" >
      {{ isButtonDisabled  ? "Disable" : "Click Here"  }}
    </button>
  
    <button v-bind="objectOfAttrs">Click here!!!</button>
    <button :id="convertToId(listString)">Number: {{ number + 2 }}</button>

 </div>
</template>