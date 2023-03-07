<template>
  <section class="root-component">
    <ActiveUser v-bind="activeUser" />
    <UserData @update-active-user="updateActiveUser" />
  </section>
</template>

<script>
import ActiveUser from './components/ActiveUser.vue';
import UserData from './components/UserData.vue';

export default {
  components: { ActiveUser, UserData },
  data() {
    return {
      activeUser: {
        username: "Mariela Plaza",
        age: "30"
      }
    }
  },
  methods: {
    updateActiveUser(newUser) {
      this.activeUser = newUser
    }
  }
}
</script>

<style scoped>
.root-component {
  margin: 2rem auto;
  text-align: center;
}
</style>