<template>
  <header>
    <v-card
      elevation="0"
      class="d-flex flex-column justify-center align-center"
    >
      <v-card-title>
        <h2 class="text-uppercase">Luis Garcia</h2>
      </v-card-title>
      <v-card-subtitle>
        <h3 class="mt-2">Desarrollador Web</h3>
      </v-card-subtitle>
      <v-avatar>
        <img src="https://cdn.vuetifyjs.com/images/john.jpg" alt="John" />
      </v-avatar>
      <v-card-text class="d-flex flex-column justify-center">
        <div class="d-flex justify-center align-center mb-3">
          <span class="mr-1 text--primary">Escrito por </span>
          <v-chip color="primary">@guevara_codes</v-chip>
        </div>
        <div class="d-flex justify-center align-center">
          <v-chip outlined class="mr-1">LinkedIn</v-chip
          ><v-chip outlined>GitHub</v-chip>
        </div>
      </v-card-text>
    </v-card>
  </header>
</template>