<template>
    <div>
      <img :src="url" alt="Image">
      <div id="app" data-v-app>
        <h1 :id="elementId" :class="elementClass">Heading</h1>
      </div>
    </div>
  </template>
  
  <script setup>
  const elementId = "heading";
  const elementClass = "heading";
  const url = "https://gratisography.com/wp-content/uploads/2024/03/gratisography-funflower-800x525.jpg";
  </script>
  
  <style>
  .heading {
    color: blue;
  }
  #heading {
    background-color: orange;
  }
  </style>
  