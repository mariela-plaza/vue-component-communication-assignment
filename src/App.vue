<template>
  <section class="root-component">
    <ActiveUser />
    <UserData />
  </section>
</template>

<script>
import ActiveUser from './components/ActiveUser.vue';
import UserData from './components/UserData.vue';

export default {
  components: { ActiveUser, UserData }
}
</script>

<style scoped>
.root-component {
  margin: 2rem auto;
  text-align: center;
}
</style>