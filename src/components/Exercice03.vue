<template>
    <input :disabled="isDisable" :value="handleChange" type="text">
  </template>
  
  <script setup>
  const isDisable = false;  
  const handleChange = "Cho phép nhập";  
  </script>
  
  <style>
  </style>
  