<template>
    <button @click="handleClick('Rikkei Academy')">Get param</button>
</template>

<script setup>
    const handleClick = (str) => {
        console.log(str);  
    }
</script>

<style>

</style>