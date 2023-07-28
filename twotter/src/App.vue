<template>
  <div id="app">
    <nav>
      <RouterLink to="/">
        <div class="navigation__logo">Twooter</div>
      </RouterLink>
      <div class="navigation__user">
        {{ user.username }}
      </div>
    </nav>
    <router-view></router-view>
  </div>
</template>

<script>
import { RouterLink } from "vue-router";

export default {
  name: "App",
  data() {
    return {
      user: {
        username: "Jan Kowalski",
      },
    };
  },
  components: { RouterLink },
};
</script>

<style lang="scss">
* {
  margin: 0;
  text-decoration: none;
}

#app {
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  text-align: center;
  color: #2c3e50;
  min-height: 100vh;
  background-color: #f3f5fa;

  nav {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 10px 5%;
    background-color: deeppink;
    color: white;

    .navigation__logo {
      font-weight: bold;
      font-size: 24px;
      color: white;
    }

    .navigation__user {
      font-weight: bold;
    }
  }
}
</style>
