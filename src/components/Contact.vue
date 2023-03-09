<template>
  <div class="row mx-0 justify-content-center align-items-center" style="min-height: 100vh">
    <div>
        <div class="d-flex flex-row align-items-center mx-0 px-3">
            <div class="font-size-xl text-left font-weight-bold">
                <span class="text-black">
                    Get In Touch
                </span>
            </div>
            <div class="line-bar"></div>
        </div>

        <div class="container my-5 text-left">
            <div class="row mx-0 justify-content-center">
                <div class="col-12 col-lg-6">
                    <div class="mb-4">
                        <label for="" class="font-size-sm text-laravel">Name</label>
                        <div class="mt-2">
                            <input class="w-100" style="font-size-15px" v-model="form.name">
                        </div>
                    </div>

                    <div class="form-group mb-4">
                        <label for="" class="font-size-sm text-laravel">Email</label>
                        <div class="mt-2">
                            <input class="w-100" style="font-size-15px" v-model="form.email">
                        </div>
                    </div>

                    <div class="form-group mb-4">
                        <label for="" class="font-size-sm text-laravel">Message</label>
                        <div class="mt-2">
                            <textarea name="" class="w-100" id="" rows="3" style="font-size-15px" v-model="form.message"></textarea>
                        </div>
                    </div>

                    <div class="d-flex flex-row">
                        <a href="" class="text-decoration-none text-white" style="border: 1px solid #FF2C1F">
                            <div class="hover bg-laravel p-2 px-3">
                                <i class="fas fa-paper-plane"></i>
                                <span class="mx-2">
                                    Submit
                                </span>
                            </div>
                        </a>
                    </div>
                </div>
            </div>
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
            email: null,
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
    color: black;
}

a:hover .hover {
  translate: -0.25rem -0.25rem !important;
}

input, textarea {
    border-radius: 0px;
    border-top: none;
    border-left: none;
    border-right: none;
    border-bottom: 1px solid #d8d8d8;
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