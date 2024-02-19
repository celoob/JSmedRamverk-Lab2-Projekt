<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <!-- logo -->
    <div>
      <RouterLink to="/"><img src="../assets/logotyp.png" alt="celoob logo" /></RouterLink>
      >
    </div>
    <!-- navbar -->
    <nav>
      <ul>
        <li v-if="$route.path === '/'">
          <RouterLink to="/" class="nav-btn active-view"><strong>Portfolio</strong></RouterLink>
        </li>
        <li v-else>
          <RouterLink to="/" class="nav-btn"><strong>Portfolio</strong></RouterLink>
        </li>

        <li v-if="$route.path === '/about'">
          <RouterLink to="/about" class="nav-btn active-view"><strong>About</strong></RouterLink>
        </li>
        <li v-else>
          <RouterLink to="/about" class="nav-btn"><strong>About</strong></RouterLink>
        </li>
      </ul>
    </nav>
  </header>
  <RouterView />
</template>

<style scoped>
header {
  height: 12vh;
  display: flex;
  align-items: center;
  background-color: none;
}

/* logotyp */
header img {
  width: 250px;
  margin: 3.5vh 0 1.6vh 2.5vw;
}

nav {
  display: flex;
  flex-direction: row;
  flex-grow: 1;
  margin-right: 0.5vw;
  margin-top: 6vh;
  justify-content: flex-end;
}

.nav-btn {
  padding: 2vh;
  display: flex;
}
.active-view {
  border-right: 2px solid white;
  background-color: #00000060;
}

nav li {
  list-style-type: none;
}
nav li a {
  text-decoration: none;
  color: white;
}
header {
  height: 12vh;
  display: flex;
  align-items: center;
  background-color: none;
}

/* logotyp */
header img {
  width: 250px;
  margin: 3.5vh 0 1.6vh 2.5vw;
}

nav {
  display: flex;
  flex-direction: row;
  flex-grow: 1;
  margin-right: 0.5vw;
  margin-top: 6vh;
  justify-content: flex-end;
}

.nav-btn {
  padding: 2vh;
  display: flex;
}
.active-view {
  border-right: 2px solid white;
  background-color: #00000060;
}

nav li {
  list-style-type: none;
}
nav li a {
  text-decoration: none;
  color: white;
}

@media only screen and (max-width: 1000px) {
  /* HEADER */
  header {
    display: flex;
    font-size: 2.5em;
    flex-direction: column;
    height: auto;
  }

  /* logotyp */
  header img {
    width: 70vw;
    margin: 5vh auto 1.6vh auto;
  }

  /* navbar */
  nav {
    width: 50vw;
    text-align: center;
  }
  .active-view {
    border-right: 3px solid white;
  }
}
</style>
