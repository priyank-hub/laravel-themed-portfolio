<template>
  <div class="">
    <div class="">  
        <h1 class="font-weight-bold">
            <span class="">
                <span class="">
                    About Me
                </span>
            </span>
        </h1>
    </div>
    <div class="container my-4 text-left about my-5">
        <div class="row align-itmes-center">
            <!-- <div class="col-3 text-center image">
                <div class="row align-items-center justify-content-center h-100">
                    <img class="col-6" src="/assets/programmer-red.png" alt="">
                </div>
            </div> -->
            <div class="col-12 col-lg-12">
                <p class="px-3">
                    Hello, my name is Priyank Patel, and I'm a Full Stack web developer with <span class="text-laravel"> 2 Years </span> of experience. 
                    I have a Bachelor's degree in <span class="text-laravel"> Computer Science </span> from <span class="text-laravel">York University</span> in Toronto, Canada. 
                    I'm always eager to learn new programming languages and enjoy the challenge of building solutions that meet my clients' needs. 
                    As a developer, I have experience with a variety of technologies, including <span class="text-laravel"> React.js, Vue.js, Node.js, PHP Laravel, MySQL, and NoSQL. </span>

                    I take pride in my work and am passionate about delivering high-quality projects that exceed my clients' expectations. 
                    I'm comfortable working on both Front-End and Back-End development, and I'm always eager to take on new challenges. 
                    When I'm not coding, I enjoy exploring new technologies and learning about the latest trends in web development.
                </p>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomePage',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.about {
    font-size: 1.1rem;
    line-height: 2.5rem;
    color: black;
}

@media screen and (max-width: 768px) {
    .image {
        display: none !important;
    }
}

h1 {
    font-size: 3rem;
} 
</style>
