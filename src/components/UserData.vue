<template>
  <form class="box user-form">
    <section>
      <label>Username</label>
      <input type="text" name="newUsername" />
    </section>
    <section>
      <label>Age</label>
      <input type="text" name="newAge" />
    </section>
  </form>
</template>

<script>
export default {
  data() {
    return {
      newUsername: "",
      newAge: ""
    }
  }
}
</script>

<style scoped>
.user-form {
  background: whitesmoke;
  border: 2px solid darkolivegreen;
}

.user-form section {
  display: flex;
  flex-direction: column;
  margin-bottom: 1rem;
}

.user-form section label {
  color: rgb(36, 46, 20);
}

.user-form section input {
  border: 2px solid olive;
  border-radius: 5px;
}
</style>