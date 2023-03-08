<template>
  <div class="row mx-0 justify-content-center align-items-center" style="min-height: 100vh">
    <div>
        <h1 class="font-weight-bold">
            <span class="">
                <span class="">
                    Get In Touch
                </span>
            </span>
        </h1>

        <div class="my-5 text-left">
            <div class="form-group">
                <label for="" class="font-size-sm text-laravel">Name</label>
                <b-form-input class="" style="font-size-15px" v-model="form.name"></b-form-input>
            </div>

            <div class="form-group">
                <label for="" class="font-size-sm text-laravel">Email</label>
                <b-form-input class="" style="font-size-15px" v-model="form.name"></b-form-input>
            </div>

            <div class="form-group">
                <label for="" class="font-size-sm text-laravel">Message</label>
                <b-form-input class="" style="font-size-15px" v-model="form.name"></b-form-input>
            </div>

            <a href="" class="border-laravel text-decoration-none text-white mx-2 my-4 text-right">
                <div class="hover bg-laravel p-2">
                    <i class="fas fa-paper-plane"></i>
                    <span class="mx-2">
                        Submit
                    </span>
                </div>
            </a>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    
  },
  data() {
    return {
        form: {
            name: null,
            subject: null,
            message: null,
        }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
    font-size: 3rem;
}
</style>