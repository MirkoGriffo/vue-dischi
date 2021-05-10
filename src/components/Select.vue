<template>
  <div class="select">
    <label>Flilter by genre: </label>
    <select>
      <option value="all">All</option>
      <option value="rock">Rock</option>
      <option value="pop">Pop</option>
      <option value="jazz">Jazz</option>
      <option value="metal">Metal</option>
    </select>
  </div>
</template>

<script>
export default {
  name: "Select",
};
</script>

<style scoped>
.select {
  position: relative;
  bottom: 220px;
  left: 800px;
}
.select label {
  color: #fff;
}
</style>