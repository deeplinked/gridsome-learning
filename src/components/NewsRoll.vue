<template>
      <section class="section">
        <div class="container">
        <div class="tile is-ancestor columns is-multiline">
            <div v-for="notification in $page.allNotification.edges" :key=notification.id class="tile column is-4 is-parent">
                <div class="tile is-child notification" :class='notification.node.type'>
                   <p>{{ notification.node.date }}</p>
                   <h2 class="subtitle is-5">
                    <g-link :to="notification.node.path">
                        {{ notification.node.title }}
                    </g-link>
                    </h2>
                    <p>{{ notification.node.excerpt }}</p>
                </div>
            </div>
        </div>
        </div>
      </section>
</template>

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

<script>
export default {
    
}
</script>