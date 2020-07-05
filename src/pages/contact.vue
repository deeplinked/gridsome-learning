<template>
    <Layout>
        <section class="section">
        <div class="container">
        <div class="columns">

        <div class="column is-6">
            <h1>get in touch</h1>
            <p>For any queries please do call us on the mobiles numbers mentioned below or message us on telegram/whatsapp. 
             You can also tag us on Facebook/Twitter or else just fill out this form with your query and we will get back to you asap 
             <i class="far fa-lg fa-hand-point-right is-hidden-mobile"></i> <i class="far fa-lg fa-hand-point-down is-hidden-tablet "></i></p>
            <div class="media">
                <div class="media-left">
                    <span class="icon"><i class="fas fa-lg fa-phone"></i></span>
                </div>
                <div class="media-content">
                    <p>(91) 7777777777, (91) 6666666666</p>
                </div>
            </div>
            <div class="media">
                <div class="media-left">
                    <span class="icon"><i class="fab fa-lg fa-telegram-plane"></i></span>
                </div>
                <div class="media-content">
                    <p>(91) 7777777777</p>
                </div>
            </div>
            <div class="media">
                <div class="media-left">
                    <span class="icon"><i class="fab fa-lg fa-whatsapp"></i></span>
                </div>
                <div class="media-content">
                    <p>(91) 6666666666</p>
                </div>
            </div>
            <div class="media">
                <div class="media-left">
                    <span class="icon"><i class="fas fa-lg fa-envelope"></i></span>
                </div>
                <div class="media-content">
                    <p>info@email.com</p>
                </div>
            </div>
            <div class="media">
                <div class="media-left">
                    <span class="icon"><i class="fas fa-lg fa-map-marker-alt"></i></span>
                </div>
                <div class="media-content">
                    <p>Address, building name, street name, city, state, pin code</p>
                </div>
            </div>
        </div>

        <div class="column is-6">
            <div class="box">
                <form>
                    <div class="field">
                    <label class="label">Name</label>
                    <div class="control">
                        <input class="input" type="text" placeholder="Text input">
                    </div>
                    </div>

                    <div class="field">
                    <label class="label">Email</label>
                    <div class="control">
                        <input class="input" type="email" placeholder="Email input">
                    </div>
                    </div>

                    <div class="field">
                    <label class="label">Subject</label>
                    <div class="control">
                        <div class="select">
                        <select>
                            <option>Select dropdown</option>
                            <option>With options</option>
                        </select>
                        </div>
                    </div>
                    </div>  

                    <div class="field">
                    <label class="label">Message</label>
                    <div class="control">
                        <textarea class="textarea" placeholder="Textarea"></textarea>
                    </div>
                    </div>  

                    <div class="field is-grouped">
                    <div class="control">
                        <button class="button is-link">Submit</button>
                    </div>
                    <div class="control">
                        <button class="button is-link is-light">Cancel</button>
                    </div>
                    </div>

                </form>
            </div><!-- .box -->
        </div>

        </div>
        </div>
        </section>

    </Layout>
</template>

<script>
export default {
    metaInfo: {
        title: "Contact"
    }
}
</script>

<style scoped>
.box {
    box-shadow: none;
    border: 1px solid #ededed;
}
</style>