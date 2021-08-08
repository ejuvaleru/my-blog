<template>
  <div>
    <the-header class="my-1"></the-header>
    <v-card class="rounded-lg py-2 px-2" color="primary">
      <v-chip class="mr-1">todos</v-chip> <v-chip>desarrollo</v-chip>
    </v-card>
    <blog-card v-for="entry in entries" :blog="entry" :key="entry.path" class="my-1"></blog-card>
  </div>
</template>
<script>
import BlogCard from "~/components/UI/BlogCard.vue";

export default {
  head() {
    return {
      script: [{ src: 'https://identity.netlify.com/v1/netlify-identity-widget.js' }],
    };
  },
  components: {
    BlogCard,
  },
  data() {
    return {}
  },
  async asyncData ({ $content }) {
    const entries = await $content('blog').only(['title', 'description', 'slug','createdAt']).fetch()

    return {
      entries
    }
  }
};
</script>
