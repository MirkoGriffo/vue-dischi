<template>
  <div class="album-card">
    <img :src="info.poster" :alt="info.title" />
    <h3 class="white">{{ info.title }}</h3>
    <p>{{ info.author }}</p>
    <p>{{ info.year }}</p>
    <p class="white">{{ info.genre }}</p>
  </div>
</template>

<script>
export default {
  name: "Album",
  props: ["info"],
};
</script>

<style scoped>
.album-card {
  height: 400px;
  width: 200px;
  background-color: #2e3a46;
  margin: 12px;
  text-align: center;
}
img {
  width: 80%;
  margin: 25px;
}

.white {
  color: white;
}

h3 {
  text-transform: uppercase;
}
p {
  color: gray;
  font-size: 18px;
  margin: 10px;
}
</style>