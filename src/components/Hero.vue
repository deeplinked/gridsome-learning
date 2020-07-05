<template>
<section class="hero is-medium has-text-centered">
<div class="hero-body">
    
    <div class="columns ">
    <div class="column is-offset-3 is-6">
    <h1 class="title is-1 has-text-link">Company Name</h1>
    <div class="is-divider" data-content="company tag line"></div>
    </div>
    </div>
    <p class="subtitle is-4">
        Quality and affordable coaching for 
        <strong>
        <no-ssr>
        <vue-typer 
            :pre-type-delay='100'
            :pre-erase-delay='3000'
            :text='["GATE","PSU","CII-iPATE"]'>
        </vue-typer> 
        </no-ssr>
        </strong>
        aspirants @City, State.
    </p>
</div>
</section>
</template>

<script>
if (process.browser) {
  var VueTyper = require('vue-typer').VueTyper
}
export default {
    components: {
        VueTyper
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
</style>