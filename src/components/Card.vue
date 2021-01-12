<template>
  <div class="card">
    <strong>{{ title }}</strong>
    <p>
      {{ body }}
    </p>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: {
    title: String,
    body: String,
  },
};
</script>

<style scoped>
.card {
  width: 200px;
  border: 1px solid #eee;
  border-radius: 4px;
  box-shadow: 1px 1px 5px #333;
  margin: 5px;
}

p {
  font-size: 12px;
}
</style>