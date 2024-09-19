<template>
  <div>
    <img style="width: 200px; height: 150px;" v-bind:src="url" alt="" />
    <br>
    <button @click="changeImage">Change Image</button>
  </div>
</template>

<script setup>
import { ref } from "vue";

const data = [
  "https://media-cdn-v2.laodong.vn/storage/newsportal/2023/8/26/1233821/Giai-Nhi-1--Nang-Tre.jpg",
  "https://images2.thanhnien.vn/528068263637045248/2024/1/25/e093e9cfc9027d6a142358d24d2ee350-65a11ac2af785880-17061562929701875684912.jpg",
  "https://data.webnhiepanh.com/wp-content/uploads/2020/11/21105453/phong-canh-1.jpg",
  "https://media.istockphoto.com/id/517188688/vi/anh/phong-c%E1%BA%A3nh-n%C3%BAi-non.jpg?s=612x612&w=0&k=20&c=WWWaejSo6EWGZMZSK7QK6LCfwd0rL2KB3ImCX2VkW4A=",
];
const getImageRandom = () => {
  const randomIndex = Math.floor(Math.random() * data.length);
  return data[randomIndex];
};
const url = ref("https://media-cdn-v2.laodong.vn/storage/newsportal/2023/8/26/1233821/Giai-Nhi-1--Nang-Tre.jpg");
const changeImage = () => {
    url.value = getImageRandom();
}

</script>

<style></style>
