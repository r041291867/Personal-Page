<template>
  <div>
    <v-row
      v-for="[title, value] of value"
      :key="title"
      align="center"
      class="mx-auto"
    >
      <v-col
        cols="12"
        xl="11"
      >
        <div class="mb-1">
          {{ title }}
        </div>

        <div class="text-center">
          <v-progress-linear
            color="success"
            background-color="grey"
            background-opacity="0.5"
            rounded
            stream
            :value="value"
            height="6"
          ></v-progress-linear>
        </div>
      </v-col>
    </v-row>
  </div>
</template>

<script>
  export default {
    data: () => ({

    }),

    props: {
      value: Array,
    },
  }
</script>