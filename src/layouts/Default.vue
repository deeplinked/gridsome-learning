<template>
<div>
    <Navbar />
    <transition name="fade" appear>
    <div class="content">
      <slot/>
    </div>
    </transition>
    <Footer />
</div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<script>
import Navbar from '~/components/Navbar.vue'
import Footer from '~/components/Footer.vue'
export default {
  components: {
    Navbar,
    Footer
  }
}
</script>

<style>
.fade-enter-active {
  transition: opacity .5s ease;
}
.fade-enter {
  opacity: 0;
}
</style>
