<template>
    <a :href="href" @click="handleClick">Link</a>
  </template>
  
  <script setup>
  const href = "https://www.google.com/?hl=vi";
  const handleClick = (event) => {
    if (!href.startsWith('https://')) {
      event.preventDefault(); 
      alert('URL không hợp lệ. Phải bắt đầu với "https://".'); 
    }
  }
  </script>
  
  <style>
  </style>
  