<template>
  <div class="about">
    <h1>This is an about page</h1>
    <button @click="getData">获取数据</button>
  </div>
</template>

<script>
import axios from "axios";
export default {
  setup() {
    const getData = async () => {
      const data = await axios.get(
        "http://localhost:3022/comment/music?id=186016&limit=1"
      );
      console.log(data);
    };

    return { getData };
  },
};
</script>

<style>
</style>
