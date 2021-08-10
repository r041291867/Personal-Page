<template>
  <v-btn
    color="teal"
    :href="$attrs.href"
    text
  >
    <span class="teal--text text--darken-2 font-weight-bold">
      <slot />
    </span>
  </v-btn>
</template>