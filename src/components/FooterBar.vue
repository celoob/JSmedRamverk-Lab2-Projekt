<script setup></script>

<template>
  <footer>
    <!-- Shown when screen is 1001px wide or more -->
    <div id="footer-big">
      <p><img src="../assets/namn.png" alt="name" />Emil Loob</p>
      <p><img src="../assets/phone.png" alt="phonenumber" />070-279 69 26</p>
      <p><img src="../assets/mail.png" alt="email" />carlemilloob@gmail.com</p>
      <p>
        <img src="../assets/li.png" alt="linkedin" /><a
          href="https://linkedin.com/in/emil-loob-66222b194/"
          >linkedin.com/in/emil-loob-66222b194/</a
        >
      </p>
    </div>
    <!-- Shown when screen is 1000px wide or less -->
    <div id="footer-small">
      <a><img src="../assets/phone.png" alt="call" /></a>
      <a href="https://mail.google.com/"><img src="../assets/mail.png" alt="email" /></a>
      <a href="https://linkedin.com/in/emil-loob-66222b194/"
        ><img src="../assets/li.png" alt="linkedin"
      /></a>
    </div>
    <a id="backtotop" href="#top">Back to the top!</a>
  </footer>
</template>

<style scoped>
footer {
  background-color: #121212;
  color: lightgray;
  height: 30vh;
}
footer div {
  padding: 3vw;
  background-color: #171717;
}
/* info */
footer div p {
  margin: 1vh;
  padding-bottom: 0.5vh;

  text-align: left;
}
/* icons */
footer div p img {
  margin-bottom: -0.55vh;
  margin-right: 1vh;
}
#footer-small {
  display: none;
}
footer a {
  color: lightgray;
}
footer a:visited {
  color: lightgray;
}
/* back to top */
#backtotop {
  display: flex;
  justify-content: center;

  padding: 1.2vh;

  color: white;
  background-color: #121212;
}
</style>
