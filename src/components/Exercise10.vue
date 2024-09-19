<template>
    <input 
      @keydown="handleKeydown"
      :value="valueInput"
      @input="handleChange"
      type="text"
    >
  </template>
  
  <script setup>
  import { ref } from 'vue';
  
  const valueInput = ref("");
  const handleChange = (event) => {
    valueInput.value = event.target.value;
  }
  
  const handleKeydown = (event) => {
    if (event.key === 'Enter') {
      if (event.shiftKey) {
        submit();
      } else {
        alert('Bạn cần ấn Shift + Enter');
      }
    }
  }
  
  const submit = () => {
    alert(valueInput.value);
  }
  </script>
  
  <style>
  </style>
  