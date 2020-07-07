<template>
<section class="hero is-medium has-text-centered">
<div class="hero-body">
<div class="container">
    
    <h1 class="title is-1 has-text-link">Company Name</h1>
    <div class="is-divider" data-content="company tag line"></div>

<vue-typed-js :strings="['awesome', 'brilliant']" :loop="true" @onComplete="doSmth()">
  <p class="subtitle has-text-centered">We are a <span class="typing"></span> company!</p>
</vue-typed-js>

</div>
</div>
</section>
</template>

<script>
/*if (process.browser) {
  var VueTyper = require('vue-typer').VueTyper
}*/
import { VueTypedJs } from 'vue-typed-js'
export default {
    components: {
        VueTypedJs
    }
}
</script>

<style scoped>
.is-divider[data-content]::after, .is-divider-vertical[data-content]::after {
    color: #7a7a7a;
    font-size: 1.25rem;
    transform: translateY(-1.5rem);
    font-variant: small-caps;
}
.is-divider, .is-divider-vertical {
    border-top: .1rem solid #ededed;
    margin: 1rem 0;
}
strong {
    font-weight: 500;
}
.title.is-1 {
    font-size: 3.25rem;
}
.typed-element {
    justify-content: center;
}
</style>