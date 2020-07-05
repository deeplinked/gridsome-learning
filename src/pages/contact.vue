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
<form
  name="contact"
  method="post"
  v-on:submit.prevent="handleSubmit"
  action="/Success/"
  data-netlify="true"
  data-netlify-honeypot="bot-field"
>
  <input type="hidden" name="form-name" value="contact" />
  <p hidden>
    <label>
      Don’t fill this out: <input name="bot-field" />
    </label>
  </p>
  
    <div class="field">
      <label for="name" class="label" >Your name</label>
      <div class="control">
      <input class="input" type="text" name="name" v-model="formData.name" />
      </div>
    </div>

    <div class="field">
      <label for="email" class="label">Your email</label>
      <div class="control">
      <input class="input" type="email" name="email" v-model="formData.email" />
      </div>
    </div>

      <div class="field">
        <label class="label">Subject</label>
        <div class="control">
            <div class="select">
            <select name="subject" v-model="formData.subject">
                <option>Admission</option>
                <option>Faculty</option>
            </select>
            </div>
        </div>
        </div>

    <div class="message-wrapper field">
    <label for="message" class="label">Message</label>
    <div class="control">
    <textarea class="textarea" name="message" v-model="formData.message"></textarea>
    </div>
    </div>

  <button class="button is-link" type="submit">Submit form</button>
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
    },
    data() {
        return {
        formData: {},
        }
    }, 
    methods: {
        encode(data) {
            return Object.keys(data)
            .map(key => encodeURIComponent(key) + '=' + encodeURIComponent(data[key]))
            .join('&')
        },
        handleSubmit(e) {
            fetch('/', {
            method: 'POST',
            headers: { 'Content-Type': 'application/x-www-form-urlencoded' },
            body: this.encode({
                'form-name': e.target.getAttribute('name'),
                ...this.formData,
            }),
            })
            .then(() => this.$router.push('/Success'))
            .catch(error => alert(error))
        }
    }
}
</script>

<style scoped>
.box {
    box-shadow: none;
    border: 1px solid #ededed;
}
</style>