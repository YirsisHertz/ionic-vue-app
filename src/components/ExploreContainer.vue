<template>
  <div id="container">
    <h1>Post's</h1>
    <hr />
    <container />
  </div>
</template>

<script lang="ts">
import Container from "./Container.vue";
export default {
  components: { Container },
  name: "ExploreContainer",
};
</script>

<style scoped>
#container {
  text-align: center;
}

#container strong {
  font-size: 20px;
  line-height: 26px;
}

#container p {
  font-size: 16px;
  line-height: 22px;
  color: #8c8c8c;
  margin: 0;
}

#container a {
  text-decoration: none;
}
</style>