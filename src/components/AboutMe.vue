<template>
  <section id="about-me">
    <div class="py-12"></div>

    <v-container class="text-center">
      <h2 class="display-2 font-weight-bold mb-3">ABOUT ME</h2>

      <v-responsive
        class="mx-auto mb-8"
        width="56"
      >
        <v-divider class="mb-1"></v-divider>

        <v-divider></v-divider>
      </v-responsive>

      <v-responsive
        class="mx-auto title font-weight-light mb-8"
        max-width="720"
      >
        I'm a front-end engineer with back-end experience. I enjoy helping others to solve their problems and get a sense of accomplishment from it. I often admire the various graphic and web designs, and I hope that I can become a developer with a sense of beauty and design ability in addition to being an engineer.
      </v-responsive>

      <v-avatar
        class="elevation-12 mb-8"
        size="128"
      >
        <v-img src="@/assets/IMG_5194.jpeg"></v-img>
      </v-avatar>

      <div></div>

      <div
        class="grey--text text--darken-2 font-weight-bold text-uppercase btn-class mb-1"
        text
      >
        Resume
      </div>
      <v-responsive
        class="mx-auto mb-2"
        width="56"
      >
        <v-divider></v-divider>
      </v-responsive>

      <resume-button
        href="https://www.cakeresume.com/s--SnneDe0JAgKLZX5U5n-UIg--/r041291867"
      >
        Chinese
      </resume-button>

      <resume-button
        href="https://www.canva.com/design/DAEjlwa-4H4/view?utm_content=DAEjlwa-4H4&utm_campaign=designshare&utm_medium=link&utm_source=publishsharelink"
      >
        English
      </resume-button>
    </v-container>

    <div class="py-12"></div>
  </section>
</template>

<script>
  export default {
    components: {
      ResumeButton: () => import('./Button'),
    }
  }
</script>

<style scoped>
  .btn-class {
    font: Roboto;
    font-size: 1rem;
    font-weight: 500;
    letter-spacing: .0892857143em;
  }
</style>