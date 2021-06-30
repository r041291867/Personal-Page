<template>
  <section id="stats">
    <v-parallax
      :height="$vuetify.breakpoint.smAndDown ? 700 : 600"
      src="@/assets/photo-1510915228340-29c85a43dcfe.jpeg"
    >
      <v-container>
        <h2 class="display-2 font-weight-bold mb-3 text-center">SKILLS</h2>

        <v-responsive
          class="mx-auto mb-12"
          width="56"
        >
          <v-divider class="mb-1" dark></v-divider>

          <v-divider dark></v-divider>
        </v-responsive>

        <v-row
          class="mx-auto"
          style="max-width: 1024px;"
        >
          <v-col cols="6">
            <skill-stat :value="stats"/>
          </v-col>

          <v-col cols="6">
            <skill-stat :value="stats_b"/>
          </v-col>
        </v-row>

      </v-container>
    </v-parallax>
  </section>
</template>

<script>
  export default {
    components: {
      SkillStat: () => import('./SkillStat.vue'),
    },

    data: () => ({
      stats: [
        ['HTML', '70'],
        ['CSS', '60'],
        ['Javascript', '60'],
        ['VueJS', '80'],
        ['ReactJS', '20'],
      ],
      stats_b: [
        ['Python', '70'],
        ['Docker', '60'],
        ['MySQL', '50'],
      ],
    })
  }
</script>