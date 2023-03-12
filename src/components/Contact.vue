<template>
  <div class="row mx-0 justify-content-center align-items-center" style="min-height: 90vh">
    <div>
        <div class="d-flex flex-row align-items-center mx-0 px-3 reveal">
            <div class="font-size-xl text-left font-weight-bold">
                <span class="" :class="mode == 'dark' ? 'text-white' : 'text-black'">
                    Get In Touch
                </span>
            </div>
            <div class="line-bar"></div>
        </div>

        <div v-if="success" class="mt-5 success">
            <div class="mt-4">
                <img src="/assets/email.png" alt="" width="80px">
            </div>
            <div class="mt-5">
                <!-- <h6 class="">{{ message }}</h6> -->
                <h4 :class="mode == 'dark' ? 'text-white' : 'text-black'">
                    Thank you for reaching out to me.
                </h4>
                <h6 class="" :class="mode == 'dark' ? 'text-white' : 'text-black'">
                    I Appreciate you taking the time to connect with me and for your interest in my work. I will get back to you promptly with a response to your inquiry or to discuss any further details.
                </h6>
            </div>

            <div class="mt-5">
                <b-button class="text-decoration-none text-white p-0" style="border: 1px solid #FF2C1F" @click="success = false">
                    <div class="hover bg-laravel p-2 px-3">
                        <i class="fas fa-paper-plane"></i>
                        <span class="mx-2">
                            Send Again
                        </span>
                    </div>
                </b-button>
            </div>
        </div>

        <div v-else-if="error">
            {{ message }}
        </div>

        <div v-else class="container my-5 text-left">
            <div class="row mx-0 justify-content-center">
                <div class="col-12 col-lg-6">
                    <form @submit.prevent="submit">
                        <div class="mb-4 reveal">
                            <label for="" class="font-size-sm text-laravel">Name</label>
                            <div class="mt-2">
                                <input class="w-100" style="font-size-15px" required v-model="form.name" :class="mode == 'dark' ? 'text-white' : ''">
                            </div>
                        </div>

                        <div class="form-group mb-4 reveal">
                            <label for="" class="font-size-sm text-laravel">How can I get back to you ?</label>
                            <div class="mt-2">
                                <input class="w-100" style="font-size-15px" required v-model="form.email" placeholder="Email / Phone" :class="mode == 'dark' ? 'text-white' : ''">
                            </div>
                        </div>

                        <div class="form-group mb-4 reveal">
                            <label for="" class="font-size-sm text-laravel">Message</label>
                            <div class="mt-2">
                                <textarea name="" class="w-100" id="" rows="3" style="font-size-15px" required v-model="form.message" :class="mode == 'dark' ? 'text-white' : ''"></textarea>
                            </div>
                        </div>

                        <div class="d-flex flex-row reveal">
                            <b-button type="submit" class="text-decoration-none text-white p-0" style="border: 1px solid #FF2C1F">
                                <div class="hover bg-laravel p-2 px-3">
                                    <i class="fas fa-paper-plane"></i>
                                    <span class="mx-2">
                                        Submit
                                    </span>
                                </div>
                            </b-button>
                        </div>
                    </form>
                </div>
            </div>
        </div>
    </div>

    <div v-if="sending" class="row mx-0 justify-content-center align-items-center" 
    style="min-height: 100vh; position: fixed; top: 0; left: 0; z-index: 300" :class="mode == 'dark' ? 'bg-accent-dark' : 'bg-white'">
        <div style="height: 200px">
            <Logo />
        </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
import Logo from '../components/Logo.vue'

export default {
  props: {
    mode: String,
  },
  components: {
    Logo,
  },
  data() {
    return {
        form: {
            name: null,
            email: null,
            message: null,
        },
        success: false,
        error: false,
        message: null,
        sending: false,
    }
  },
  methods: {
    async submit() {
        this.sending = true;

        const headers = { 
            "Access-Control-Allow-Origin": "*"
        };

        await axios.post('https://myportfolio-ackend.herokuapp.com//contact', this.form, { headers })
        .then(response => {
            console.log('res', response);
            this.sending = false;
            if (response.status == 200 && response.data.success == true) {
                this.success = true;
                this.message = response.data.message;
            }
        })
        .catch(err => {
            this.sending = false;
            this.error = true;
            this.message = err;
        });

        this.sending = false;
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
    font-size: 3rem;
    color: black;
}

a:hover .hover {
  translate: -0.25rem -0.25rem !important;
}

.bg-accent-dark {
    background: #171923;
}

input, textarea {
    border-radius: 0px;
    border-top: none;
    border-left: none;
    border-right: none;
    border-bottom: 1px solid #d8d8d8;
    background: transparent;
}

input:focus-visible, textarea:focus-visible {
    box-shadow: none !important;
    outline: none !important;
    transition: all 0.3s ease 0s, left 0.3s ease 0s;
    border-bottom: 2px solid #FF2C1F;
}

.submit {
    width: 130px;
}

.line-bar {
    min-width: 25vw;
    max-width: 40vw;
    height: 1px;
    background: #FF2C1F;
    margin-left: 20px;
}
</style>

<style>
.b-avatar .b-avatar-img img {
    object-fit: contain !important;
}
</style>