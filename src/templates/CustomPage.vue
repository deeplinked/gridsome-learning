<template>
    <Layout>
        <section class="section">
        <div class="container">
        <div class="columns">

            <div class="column">
                <div class="pricing-table">
                    <div class="pricing-plan">
                        <div class="plan-header">
                            {{$page.custompage.branch}}
                        </div>
                        <div class="is-through is-size-5 has-text-centered has-text-weight-medium">
                            {{$page.custompage.fee}}
                        </div>
                        <div class="plan-price">
                            <span class="plan-price-amount has-text-success">
                            <span class="plan-price-currency">₹</span>
                            {{$page.custompage.discounted}}</span>
                        </div>
                        <div class="plan-items">
                        <div v-if="$page.custompage.timings" class="plan-item">
                            <span class="has-text-weight-light">timings</span>
                            <p>{{$page.custompage.timings}}</p>
                        </div>
                        <div v-if="$page.custompage.duration" class="plan-item">
                            <span class="has-text-weight-light">duration</span>
                            <p>{{$page.custompage.duration}}</p>
                        </div>
                        <div v-if="$page.custompage.venue" class="plan-item">
                            <span class="has-text-weight-light">venue</span>
                            <p>{{$page.custompage.venue}}</p>
                        </div>
                        </div>
                        <div class="plan-footer">
                        {{$page.custompage.date}}
                        </div>
                    </div>
                </div>
            </div>

            <div class="column is-8">
            <h1>
                {{$page.custompage.title}}
            </h1>
            <div v-html="$page.custompage.content" />
            </div>

        </div>
        </div>
        </section>
    </Layout>
</template>

<page-query>
query custompage($path: String!){
  custompage: customPage(path: $path){
    title
    branch
    timings
    duration
    fee
    discounted
    date
    venue
    content
  }
}
</page-query>

<script>
export default {
    metaInfo() {
        return {
            title: this.$page.custompage.title
        }
    }
}
</script>

<style scoped>
.is-through {
    text-decoration: line-through;
}
</style>