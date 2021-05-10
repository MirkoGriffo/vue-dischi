<template>
  <main>
    <div><Select /></div>
    <div v-for="album in albumList" :key="album.id">
      <Album :info="album" />
    </div>
  </main>
</template>

<script>
import axios from "axios";
import Album from "@/components/Album.vue";
import Select from "@/components/Select.vue";
export default {
  name: "Main",
  components: {
    Album,
    Select,
  },
  data() {
    return {
      apiUrl: "https://flynn.boolean.careers/exercises/api/array/music",
      albumList: [],
    };
  },
  created() {
    this.getAlbum();
  },
  methods: {
    getAlbum() {
      axios

        .get(this.apiUrl)
        .then((res) => {
          console.log(res.data.response);
          this.albumList = res.data.response;
        })

        .catch((error) => {
          console.log("error", error);
        });
    },
  },
};
</script>

<style scoped>
main {
  padding: 50px;
  height: 100%;
  background-color: #1d2d3c;
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  align-content: center;
}
</style>