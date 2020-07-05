<template>
    <Layout>
        <section class="section">
        <div class="container">
        <h1>
            {{$page.notification.title}}
        </h1>
        <div v-html="$page.notification.content" />
        </div>
        </section>
    </Layout>
</template>


<page-query>
query Notification($path: String!){
  notification: notification (path: $path) {
    title
    content
  }
}
</page-query


<script>
export default {
    metaInfo() {
        return {
            title: this.$page.notification.title
        }
    }
}
</script>