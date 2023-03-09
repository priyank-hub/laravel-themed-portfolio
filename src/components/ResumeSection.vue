<template>
  <div class="row mx-0 justify-content-center align-items-center" style="min-height: 80vh">
    <div class="">
      <div class="d-flex flex-row align-items-center mx-0 px-3">
          <div class="font-size-xl text-left font-weight-bold">
              <span class="text-black">
                  Resume
              </span>
          </div>
          <div class="line"></div>
      </div>

      <div class="container my-5">
        <div class="d-flex flex-row justify-content-start">
          <a href="" class="border-laravel text-decoration-none text-white mx-2">
            <div class="hover bg-laravel p-2 px-3">
              <i class="fas fa-eye"></i>
              <span class="mx-2">
                View
              </span>
            </div>
          </a>

          <a href="" class="border-laravel text-decoration-none text-white mx-2">
            <div class="hover bg-laravel p-2 px-3">
              <i class="fas fa-download"></i>
              <span class="mx-2">
                Download
              </span>
            </div>
          </a>
        </div>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  props: {
    
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  font-size: 3rem;
}

a:hover .hover {
  translate: -0.25rem -0.25rem !important;
}

.line {
    min-width: 25vw;
    max-width: 40vw;
    height: 1px;
    background: #FF2C1F;
    margin-left: 20px;
}
</style>