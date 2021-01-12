<template>
  <div class="container">
    <loading v-if="load" />
    <card
      v-for="post in posts"
      :key="post.id"
      :title="post.title"
      :body="post.body"
    />
  </div>
</template>

<script>
import Card from "./Card.vue";
import axios from "axios";
import Loading from "./Loading.vue";

export default {
  components: { Card, Loading },
  data: () => ({
    posts: null,
    load: true,
  }),
  mounted() {
    this.getPost();
  },
  methods: {
    async getPost() {
      this.load = true;
      const { data } = await axios.get(
        "https://jsonplaceholder.typicode.com/posts"
      );

      this.posts = data;
      this.load = false;
    },
  },
};
</script>

<style scoped>
.container {
  display: flex;
  border: 1px solid #ddd;
  border-radius: 4px;
  box-shadow: 1px 1px 4px rgba(0, 0, 0, 0.5);
  flex-wrap: wrap;
  justify-content: center;
  margin: 0 8px;
  overflow: hidden;
}
</style>