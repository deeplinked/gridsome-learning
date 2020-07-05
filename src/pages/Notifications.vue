<template>
    <Layout>
      <section class="section">
        <div class="container">
        <h1 class="title">News / Notifications</h1>
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
        <Pager 
        :info="$page.allNotification.pageInfo"
        linkClass="pagination-link"
        />
        </div>
      </section>
    </Layout>
</template>
<page-query>
query ($page: Int){
  allNotification (sortBy: "date", order: ASC, perPage:9, page: $page) @paginate {
    pageInfo {
      totalPages
      currentPage
    }
    edges {
      node {
        id
        title
        type
        content
        path
        excerpt
        path
        date 
      }
    }
  }
}
</page-query>

<script>
import { Pager } from 'gridsome';
export default {
    components: {
    Pager
  }
}
</script>