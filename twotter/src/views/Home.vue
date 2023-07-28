<template>
  <div class="home">
    <h1>Home</h1>
    <div class="users-list">
      <RouterLink
        v-for="user in users"
        :to="{ name: 'UserProfile', params: { userId: user.id } }"
        :key="user.id"
      >
        {{ user.username }}
      </RouterLink>
    </div>
  </div>
</template>

<script>
import { RouterLink } from "vue-router";
import { users } from "../assets/users";

export default {
  name: "Home",
  setup() {
    return {
      users,
    };
  },
  components: { RouterLink },
};
</script>

<style lang="scss" scoped>
h1 {
  padding: 50px 5%;
}
.users-list {
  display: flex;
  flex-direction: column;
}
</style>
