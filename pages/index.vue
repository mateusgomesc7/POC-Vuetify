<template>
  <v-card class="mx-auto" prepend-icon="mdi-home" width="400">
    <template v-slot:title> This is a title </template>
    <v-card-text class="d-flex flex-column ga-2">
      <v-btn
        v-for="button in buttons"
        :key="button.color"
        :color="button.color"
      >
        Button
      </v-btn>
    </v-card-text>
  </v-card>
</template>

<script setup lang="ts">
const buttons = ref([
  {
    color: "primary",
  },
  {
    color: "secondary",
  },
  {
    color: "success",
  },
  {
    color: "info",
  },
  {
    color: "warning",
  },
  {
    color: "error",
  },
  {
    color: "dark",
  },
  {
    color: "light",
  },
]);
</script>
