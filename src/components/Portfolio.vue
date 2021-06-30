<template>
  <section
    id="features"
    class="grey lighten-3"
  >
    <div class="py-12"></div>

    <v-container class="text-center">
      <h2 class="display-2 font-weight-bold mb-3">PORTFOLIO</h2>

      <v-responsive
        class="mx-auto mb-12"
        width="56"
      >
        <v-divider class="mb-1"></v-divider>

        <v-divider></v-divider>
      </v-responsive>

      <v-row>
        <v-col
          v-for="{title, github, link, img, content} in portfolio"
          :key="title"
          cols="12"
          md="4"
        >
          <v-hover v-slot="{ hover }">
            <v-img
              :aspect-ratio="16/9"
              :src="require(`@/assets/${img}`)"
            >
              <v-overlay
                absolute
                :value="hover"
                color="black"
                opacity="0.6"
              >
                <h3 class="mb-3">{{ title }}</h3>

                <div v-html="content" />

                <div class="mt-3">
                  <v-btn
                    v-if="github"
                    icon
                    :href="github"
                  >
                    <v-icon>mdi-github</v-icon>
                  </v-btn>

                  <v-btn
                    icon
                    :disabled="!link"
                    :href="link"
                  >
                    <v-icon>{{ link? 'mdi-link': 'mdi-link-off' }}</v-icon>
                  </v-btn>
                </div>
              </v-overlay>
            </v-img>
          </v-hover>
        </v-col>
      </v-row>
    </v-container>

    <div class="py-12"></div>
  </section>
</template>

<script>
  export default {
    data: () => ({
      portfolio: [
        {
          title: 'React Practice',
          img: 'portfolio01.png',
          content: 'First practice of ReactJS according to <br>the official documentation.',
          github: '',
          link: 'https://codepen.io/WeiChe/pen/JjWOxGe',
        },
        {
          title: "Gomezjj's Blog",
          img: 'portfolio00.png',
          content: 'My own blog made by myself <br>w/ VueJS and Vuetify.',
          github: '',
          link: 'https://www.gomezjj.com/blog/',
        },
        {
          title: 'E-compliance System',
          img: 'RqhPuBb.png',
          content: 'The system can intelligently manages production compliance and can detect critical part changes immediately to ensure product consistency compliance to improve work efficiency.',
          github: '',
          link: '',
        },
        {
          title: 'NWE System',
          img: 'portfolio02.png',
          content: 'The system can save 40% of production manager\'s time in comparing part number, mold number and plastic pellet, and prevent order omission and manual errors in order arrangement.',
          github: '',
          link: '',
        },
        {
          title: 'Guardian Tales Calculator',
          img: 'portfolio03.png',
          content: 'Practice of VueJS w/ Vuetify and RWD functions.',
          github: 'https://github.com/r041291867/guardian-tales-calculator',
          link: 'https://r041291867.github.io/guardian-tales-calculator/',
        },
        {
          title: 'JPH Admin Dashboard',
          img: 'portfolio04.png',
          content: 'Practice of VueJS w/ Vuetify and Echarts.',
          github: 'https://github.com/r041291867/jphmanage',
          link: 'https://r041291867.github.io/jphmanage/#/',
        }
      ],
    })
  }
</script>