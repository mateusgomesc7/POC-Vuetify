<template>
  <div class="d-flex flex-column ga-3">
    <v-card class="mx-auto" prepend-icon="mdi-home" width="400">
      <template v-slot:title>
        {{ `Theme ${theme.global.name.value}` }}
      </template>
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
    <v-card theme="dark" class="mx-auto" prepend-icon="mdi-home" width="400">
      <template v-slot:title> Theme Dark </template>
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
  </div>
</template>

<script setup lang="ts">
import { useTheme } from "vuetify";

const theme = useTheme();

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
]);
</script>
