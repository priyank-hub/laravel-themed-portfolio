<template>
  <div class="">
    <div class="d-flex flex-row align-items-center mx-0 px-3">
        <div class="font-size-xl text-left font-weight-bold">
            <span class="" :class="mode == 'dark' ? 'text-white' : 'text-black'">
                About Me
            </span>
        </div>
        <div class="line"></div>
    </div>

    <div class="container my-4 text-left about">
        <div class="row align-itmes-center">
            <div class="col-12 col-lg-12">
                <p class="text-muted">
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

        <div class="container my-5 position-relative">
            <div class="bar m-auto mb-4"></div>
            <div class="mb-3">
                <h5 class="text-center font-weight-light" :class="mode == 'dark' ? 'text-white' : 'text-black'">Technologies I've worked with</h5>
            </div>
            <div class="mx-0 skill-grid text-center">
                <div class="my-4 skill-item" v-for="(item, index) in skills" :key="index">
                    <a :href="item.website" target="_blank">
                        <img :src="item.url" height="55px" style="object-fit: cover" alt="">
                        <div class="subtitle mt-3" :class="mode == 'dark' ? 'text-white' : 'text-black'">
                            {{ item.name }}
                        </div>
                    </a>
                </div>
            </div>
            <div class="bar m-auto mt-4"></div>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AboutMe',
  props: {
    mode: String
  },
  data() {
    return {
        skills: [
            {
                url: '/assets/skills/html.svg',
                name: 'HTML', 
                website: 'https://www.w3schools.com/html/'
            },
            {
                url: '/assets/skills/css.png',
                name: 'CSS',
                website: 'https://www.w3schools.com/css/'
            },
            {
                url: '/assets/skills/js.png',
                name: 'Javascript',
                website: 'https://www.w3schools.com/js/DEFAULT.asp'
            },
            {
                url: '/assets/skills/laravel.svg',
                name: 'Laravel',
                website: 'https://laravel.com/'
            },
            {
                url: '/assets/skills/sass.svg',
                name: 'Sass',
                website: 'https://sass-lang.com/'
            },
            {
                url: '/assets/skills/vue.svg',
                name: 'Vue',
                website: 'https://vuejs.org/'
            },
            {
                url: '/assets/skills/react.svg',
                name: 'React',
                website: 'https://reactjs.org/'
            },
            {
                url: '/assets/skills/flutter.svg',
                name: 'Flutter',
                website: 'https://flutter.dev/'
            },
            {
                url: '/assets/skills/java.svg',
                name: 'Java',
                website: 'https://www.java.com/en/'
            },
            {
                url: '/assets/skills/dbms.png',
                name: 'DBMS',
                website: 'https://www.javatpoint.com/dbms-tutorial'
            },
            {
                url: '/assets/skills/c++.png',
                name: 'C++',
                website: 'https://www.cplusplus.com/'
            },
            {
                url: '/assets/skills/springboot.svg',
                name: 'Spring',
                website: 'https://spring.io/'
            },
            {
                url: '/assets/skills/c.png',
                name: 'C',
                website: 'https://www.tutorialspoint.com/cprogramming/index.htm'
            },
            {
                url: '/assets/skills/git.png',
                name: 'Git',
                website: 'https://www.tutorialspoint.com/cprogramming/index.htm'
            },
            {
                url: '/assets/skills/Bootstrap.png',
                name: 'Bootstrap',
                website: 'https://www.tutorialspoint.com/cprogramming/index.htm'
            },
            {
                url: '/assets/skills/postman-icon.svg',
                name: 'Postman',
                website: 'https://www.tutorialspoint.com/cprogramming/index.htm'
            }
        ]
    }
  },
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

h3 {
    font-size: 2rem;
    font-weight: 700;
}

.card-item {
    padding: 20px 0px 100px 0px;
}

p {
    line-height: 2;
}

li::marker {
    /* list-style-type: none; */
    color: #FF2C1F;
}

.ui-item {
    transition: 0.3s all;
}

/* .ui-item:hover {
    transform: scale(1.1, 1.1);
} */

@media screen and (max-width: 1024px) {
    .project-item img {
        /* flex-direction: column-reverse; */
        display: none;
    }

    .skill-item {
        border: none !important;
    }
    .skill-grid {
        grid-template-columns: repeat(auto-fill, minmax(90px, 1fr)) !important;
    }

    h3 {
        font-size: 1.5rem;
        font-weight: 700;
    }

    .card-item {
        padding: 40px 0px;
    }

}

.project-item img {
    z-index: -3 !important;
}

.subtitle {
    font-size: 14px;
    font-weight: 300;
}

.skill-grid {
    display: grid;
    /* grid-template-columns: repeat(auto-fill, minmax(130px, 1fr)); */
    grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
    grid-column-gap: 30px;
    grid-row-gap: 25px;
}

.bar {
    width: 100px;
    height: 2px;
    background: rgb(214, 214, 214);
}

.skill-item {
    transition: 0.3s all;
}

.skill-item:hover {
    transform: scale(1.1, 1.1);
}

.line {
    min-width: 25vw;
    max-width: 40vw;
    height: 1px;
    background: #FF2C1F;
    margin-left: 20px;
}
</style>
