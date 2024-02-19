<script setup></script>

<template>
  <section id="hero-txt">
    <h1>Welcome.</h1>
    <p>Check out my past projects below :)</p>
  </section>
  <div class="down-button-wrapper">
    <a href="#to-content-ref"><img src="../assets/down.png" alt="go down" /></a>
  </div>
</template>

<style scoped>
/* hero text */
#hero-txt {
  margin: 58vh auto 0vh 10vw;
  text-align: left;
  font-size: 3vh;
  color: #ffffff;
  display: flex;
  flex-direction: column;
}

h1 {
  font-size: 4em;
}

/* down button */
.down-button-wrapper {
  background-color: #00000000;
  display: flex;
  justify-content: center;
}
.down-button-wrapper a {
  border: 0;
  background-color: #00000000;
}
.down-button-wrapper img {
  max-width: 5vw;
}

@media only screen and (max-width: 1000px) {
  /* hero text */
  #hero-txt {
    margin: 16vh auto 0vh auto;
    text-align: center;
    font-size: 2.5vh;
    color: #ffffff;
    display: flex;
    flex-direction: column;
  }

  /* down button */
  .down-button-wrapper {
    background-color: #00000000;
    display: flex;
    justify-content: center;
  }
  .down-button-wrapper img {
    max-width: 20vw;
  }
}
</style>
