<template>
<section class="hero is-medium has-text-centered">
<div class="hero-body">
    
    <div class="columns ">
    <div class="column is-offset-3 is-6">
    <h1 class="title is-1 has-text-link">Edu Basics</h1>
    <div class="is-divider" data-content="basics made easy"></div>
    </div>
    </div>
    <p class="subtitle is-4">
        Quality and affordable coaching for 
        <strong>
        <vue-typer 
            :pre-type-delay='100'
            :pre-erase-delay='3000'
            :text='["GATE","PSU","CII-iPATE"]'>
        </vue-typer> 
        </strong>
        aspirants @Warangal, Telangana.
    </p>
</div>
</section>
</template>

<script>
import { VueTyper } from 'vue-typer';
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