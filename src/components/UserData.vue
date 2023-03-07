<template>
  <form class="box user-form" @submit.prevent="submitNewActiveUser">
    <section>
      <label>Username</label>
      <input type="text" name="username" @change="updateUser" :value="user.username" />
    </section>
    <section>
      <label>Age</label>
      <input type="text" name="age" @change="updateUser" :value="user.age" />
    </section>
    <button class="btn btn-light">Submit</button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      user: {
        username: "",
        age: ""
      }
    }
  },
  emits: ['update-active-user'],
  methods: {
    updateUser(e) {
      const { value, name } = e.target
      this.user = { ...this.user, [name]: value }
    },
    resetForm() {
      this.user = {
        username: "",
        age: ""
      }
    },
    submitNewActiveUser() {
      this.$emit('update-active-user', this.user)
      this.resetForm()
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