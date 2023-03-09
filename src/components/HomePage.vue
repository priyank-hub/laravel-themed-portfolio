<template>
  <div class="">
    <div class="container content">
      <div class="gradient"></div>
      <div class="row justify-content-start align-items-center homepage">
        <div class="text-left title">
          <div class="greeting" :class="mode == 'dark' ? 'text-white' : 'text-black'">Hello! My name is</div>
          <div class="name">Priyank Patel.</div>
          <div class="greeting" :class="mode == 'dark' ? 'text-white' : 'text-black'">I'm a Full Stack Web Developer.</div>

          <div class="d-flex flex-row mt-4 social">
            <a href="https://www.linkedin.com/in/priyank9/" target="_blank" class="border-laravel text-decoration-none text-white mx-2">
              <div class="hover bg-laravel p-2 px-3">
                <i class="fab fa-linkedin"></i>
                <span class="mx-2">
                  LinkedIn
                </span>
              </div>
            </a>

            <a href="https://github.com/priyank-hub" target="_blank" class="border-laravel text-decoration-none text-white mx-2">
              <div class="hover bg-laravel p-2 px-3">
                <i class="fab fa-github"></i>
                <span class="mx-2">
                  Github
                </span>
              </div>
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomePage',
  props: {
    mode: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}

a:hover .hover {
  translate: -0.25rem -0.25rem !important;
}

.homepage {
  min-height: 100vh;
}

.gradient {
  position: fixed;
  width: 400px;
  height: 400px;
  opacity: 0.15;
  right: 0;
  top: 0;
  z-index: -1;
  background-image: radial-gradient(50% 50% at 50% 50%,#eb4432 0,hsla(0,0%,100%,0) 100%);
}

@media screen and (max-width: 995px) {
  .content {
    width: 100% !important;
  }

  .greeting {
    font-size: 1.5rem !important;
    font-weight: 600;
  }

  .gradient {
    width: 200px;
    height: 200px;
  }

  .name {
    font-size: 3rem !important;
  }

  button {
    background: #FF2C1F !important;
    color: #fff !important;
  }
}

.greeting {
  font-size: 3.5rem;
  font-weight: 700;
}

.name {
  font-size: 6rem;
  font-weight: 700;
  color: #FF2C1F;
}
</style>
