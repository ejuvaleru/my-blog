<template>
  <v-card elevation="0">
    <NuxtLink :to="`/blog/${blog.slug}`">
      <v-card-title> {{ blog.title }} </v-card-title>
      <v-card-subtitle class="py-0"> {{ formatDate(blog.createdAt) }} </v-card-subtitle>
    </NuxtLink>
      <v-card-text>
        {{ blog.description }}
      </v-card-text>
  </v-card>
</template>
<script>
export default {
  name: "BlogCard",
  props: { blog: { type: Object, required: true } },
  methods: {
    formatDate(date) {
      const options = { year: "numeric", month: "long", day: "numeric" };
      return new Date(date).toLocaleDateString("es", options);
    },
  },
};
</script>
<style scoped>
.v-application a {
  text-decoration: none !important;
  padding: 0 !important;
  margin: 0!important;
}
</style>