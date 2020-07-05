<template>
  <Layout>
    <Hero />
  <!--hola-->
    <NewsRoll />
  </Layout>
</template>

<script>
import Hero from "~/components/Hero";
import NewsRoll from "~/components/NewsRoll";
export default {
  components: {
    Hero,
    NewsRoll
  },
  metaInfo: {
    title: 'Hello, world!'
  }
}
</script>

<page-query>
query {
  allNotification (limit: 6, sortBy: "date", order: ASC) {
    edges {
      node {
        id
        title
        date
        type
        content
        path
        excerpt
      }
    }
  }
}
</page-query>

<style>
.home-links a {
  margin-right: 1rem;
}
</style>
