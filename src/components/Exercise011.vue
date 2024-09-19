<template>
    <div>
        <div class="div" :style="{ backgroundColor: colorDefault }"></div>
        <br>
        <button @click="changeColor">ChangeColor</button>
    </div>
</template>

<script setup>
import { ref } from 'vue';

    const colorDefault = ref("red");
    const listColor = ["red","blue","green","black","yellow"];
    const getRandomColor = () => {
    const randomIndex = Math.floor(Math.random() * listColor.length);
        return listColor[randomIndex];
    };
    const changeColor = () => {
        colorDefault.value = getRandomColor();
    }
</script>

<style>
    .div {
        width: 200px;
        height: 150px;
    }
</style>
