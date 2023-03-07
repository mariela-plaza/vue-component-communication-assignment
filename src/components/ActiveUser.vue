<template>
  <section class="box active-user">
    <h2>{{ username }}</h2>
    <h3>{{ age }}</h3>
  </section>
</template>

<script>
export default {
  props: {
    username: String,
    age: String
  }
}
</script>

<style scoped>
.active-user {
  background-color: rgb(138, 159, 117);
  border: 2px solid darkolivegreen;
}

.active-user h2,
.active-user h3 {
  color: rgb(36, 46, 20);
}
</style>