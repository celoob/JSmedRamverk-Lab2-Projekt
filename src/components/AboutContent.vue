<script setup></script>

<template>
  <article class="about-wrapper">
    <div class="about-txt">
      <h2>Who am I?</h2>
      <p>
        Hi, I'm Emil Loob, a 29-year-old Front-end Developer with a passion for graphic design and
        UX.
      </p>
      <p>I bring creativity and functionality together to build engaging online experiences.</p>
      <p>
        In my free time, I cherish the memories of my beloved dog, who brought joy and inspiration
        to my life.
      </p>
      <h6>Generic bio courtesy of ChatGPT3.5.</h6>
    </div>
    <div id="about-img">
      <img src="../assets/bild.jpg" alt="profilbild" />
    </div>
  </article>
</template>

<style scoped>
/* about */
.about-wrapper {
  display: flex;
  flex-direction: row;
  justify-content: center;
  background-color: #121212;
  margin-top: 5vh;
}

/* about image */
.about-wrapper {
  display: flex;
  flex-direction: row;
  justify-content: center;
  background-color: #121212;
  min-height: 60vh;
}

/* image */
.about-img {
  width: 50vw;
  text-align: center;
  background-color: #f1f1f1;
}
.about-wrapper img {
  max-width: 48vw;
  max-height: 48vh;
  margin-top: 4vh;
  margin-bottom: 4vh;
  margin-left: 1vw;
  border-radius: 50%;
}

/* text */
.about-txt {
  width: 25vw;
  max-height: 40vh;
  margin-top: 4vh;
  margin-bottom: 4vh;
  text-align: left;
  background-color: #222222;
  color: #f1f1f1;
  margin-right: 1vw;
  position: relative;
  display: flex;
  flex-direction: column;
}
.about-wrapper h2 {
  margin: 3vh 1vw 1vh 1vw;
  padding-bottom: 1vh;
  border-bottom: 2px solid #1c1c1c;
}
.about-wrapper p {
  margin: 1vh 0vw 1vh 1vw;
  min-height: 3.5vh;
}
.about-txt h6 {
  margin: 1vh 1vw 3vh 1vw;
  margin-top: auto;
  padding-top: 1vh;
  border-top: 2px solid #1c1c1c;
}
@media only screen and (max-width: 1000px) {
  .about-wrapper {
    display: flex;
    flex-direction: column;
  }
  .about-txt {
    width: 90vw;
    margin: 5vh 5vw 5vh 5vw;
    text-align: left;
    background-color: #222222;
    border-radius: 0vh 0vh 0vh 0vh;
    color: #ffffff;
    max-height: 90vh;
  }
  .about-wrapper h2 {
    margin: 3vw;
    padding-bottom: 2vh;
    border-bottom: 2px solid #1c1c1c;
  }
  .about-wrapper p {
    margin: 3vw;
  }
  .about-txt h6 {
    margin: 3vw;
    padding-top: 2vh;
    border-top: 2px solid #1c1c1c;
  }
  .about-img {
    max-width: 40vw;
    text-align: center;
    background-color: #f1f1f1;
  }
  .about-wrapper img {
    max-width: 60vw;
    max-height: 60vh;
    margin-top: 0;
    margin-bottom: 5vh;
    margin-left: 20vw;
  }
}
</style>
