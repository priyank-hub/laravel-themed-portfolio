<template>
  <div id="app">
    <div class="" style="position: fixed; top: 80px; right: 20px">
      <span class="cursor-pointer">
        <i v-if="mode == 'dark'" class="fas fa-sun text-white" @click="switchMode('light')"></i>
        <i v-else-if="mode == 'light'" class="fas fa-moon" @click="switchMode('dark')"></i>
      </span>
    </div>

    <div class="nav-bar" :class="mode == 'dark' ? 'bg-dark-grey' : 'bg-light-grey'">
      <div class="container-fluid pt-3" :class="isVisible ? '' : 'pb-3'">
        <nav class="desktop">
          <h3 class="mb-0 text-laravel brand">
            <a href="#home" class="text-laravel">
              PP
            </a>
          </h3>
          <ul class="nav-links mb-0">
            <li v-for="(item, index) in menu" :key="index" class="menu">
              <a :href="item.url" class="menu-item" :class="mode == 'dark' ? 'text-white' : 'text-black'">
                {{ item.name }}
              </a>
            </li>
          </ul>
        </nav>  

        <div class="justify-content-between align-items center mobile">
          <div class="col text-left">
            <h3 class="mb-0 text-laravel brand">
              <a href="#home" class="text-laravel">
                PP
              </a>
            </h3>
          </div>
          <div class="col text-right" :class="mode == 'dark' ? 'text-white' : 'text-black'" v-b-toggle.my-collapse>
            <i class="fas fa-bars" v-if="! isVisible"></i>
            <i class="fas fa-times" v-if="isVisible"></i>
          </div>
        </div>

        <b-collapse id="my-collapse" v-model="isVisible">
          <div class="pt-3">
            <ul class="p-0 mb-0">
              <li v-for="(item, index) in menu" :key="index" class="m-0 py-2 border-bottom text-black" style="font-weight: 300; list-style-type: none; text-align: left">
                <a :href="item.url" class="menu-item font-size-sm" :class="mode == 'dark' ? 'text-white' : 'text-black'" @click="isVisible = false">
                  {{ item.name }}
                </a>
              </li>
            </ul>
          </div>
        </b-collapse>
      </div>
    </div>

    <div class="main">
      <section id="home">
        <HomePage :mode="mode"/>
      </section>

      <section id="portfolio" style="padding-top: 90px">
        <Portfolio :mode="mode"/>
      </section>

      <section id="about-me" style="padding-top: 90px">
        <AboutMe :mode="mode"/>
      </section>

      <section id="resume" style="padding-top: 90px">
        <ResumeSection :mode="mode"/>
      </section>

      <section id="contact" style="padding-top: 90px">
        <Contact :mode="mode"/>
      </section>
    </div>


    <div class="d-none d-md-block">
      <div class="links d-flex flex-column align-items-center justify-content-center">
        <div>
          <ul class="p-0 mb-0">
            <li>
              <a href="https://github.com/priyank-hub" target="_blank">
                <span class="icon" :class="mode == 'dark' ? 'text-laravel' : 'text-black'">
                  <i class="fab fa-github"></i>
                </span>
              </a>
            </li>
            <li>
              <a href="https://www.linkedin.com/in/priyank9/" target="_blank">
                <span class="icon" :class="mode == 'dark' ? 'text-laravel' : 'text-black'">
                  <i class="fab fa-linkedin"></i>
                </span>
              </a>
            </li>
            <li>
              <a href="https://twitter.com/p1ku99" target="_blank">
                <span class="icon" :class="mode == 'dark' ? 'text-laravel' : 'text-black'">
                  <i class="fab fa-twitter"></i>
                </span>
              </a>
            </li>
          </ul>
        </div>

        <div class="mt-3" style="height: 20vh">
          <div class="line"></div>
        </div>
      </div>
    </div>

    <div class="d-none d-md-block">
      <div class="links-inverse d-flex flex-column align-items-center justify-content-center">
        <div class="text">
          patelpriyank177@gmail.com
        </div>

        <div class="mt-3" style="height: 20vh">
          <div class="line"></div>
        </div>
      </div>
    </div>

    <div class="">
      <footer>
        <div class="d-md-none">
          <div class="row mx-0 justify-content-center align-items-center p-3">
            <div class="col">
              <a href="https://github.com/priyank-hub" target="_blank">
                <span class="icon">
                  <i class="fab fa-github" :class="mode == 'dark' ? 'text-white' : 'text-black'"></i>
                </span>
              </a>
            </div>
            <div class="col">
              <a href="https://www.linkedin.com/in/priyank9/" target="_blank">
                <span class="icon">
                  <i class="fab fa-linkedin" :class="mode == 'dark' ? 'text-white' : 'text-black'"></i>
                </span>
              </a>
            </div>
            <div class="col">
              <a href="https://twitter.com/p1ku99" target="_blank">
                <span class="icon">
                  <i class="fab fa-twitter" :class="mode == 'dark' ? 'text-white' : 'text-black'"></i>
                </span>
              </a>
            </div>
          </div>
        </div>


        <div class="my-3 text-center">
          <span class="text-muted font-size-sm">
            Design & Built by <span class="text-laravel"> Priyank Patel</span>
          </span>
          <br>
          <span class="text-muted font-size-sm d-md-none">
            patelpriyank177@gmail.com
          </span>
        </div>
      </footer>
    </div>
  </div>
</template>

<script>
import HomePage from './components/HomePage.vue'
import AboutMe from './components/AboutMe.vue'
import Portfolio from './components/Portfolio.vue'
import ResumeSection from './components/ResumeSection.vue'
import Contact from './components/Contact.vue'

export default {
  name: 'App',
  components: {
    HomePage,
    AboutMe,
    Portfolio,
    ResumeSection,
    Contact,
  },

  data() {
    return {
      isVisible: false,
      menu: [
        {
          name: 'Portfolio',
          url: '#portfolio',
        },
        {
          name: 'About',
          url: '#about-me',
        },
        {
          name: 'Resume',
          url: '#resume',
        },
        {
          name: 'Contact',
          url: '#contact',
        }
      ],
      mode: 'light',
    }
  },

  computed: {

  },
  methods: {
    switchMode(mode) {
      this.mode = mode;

      if (mode == 'dark') {
        // var body = document.getElementsByTagName("BODY")[0];
        document.body.style.backgroundColor = '#171923'
      }
      else if (mode == 'light') {
        document.body.style.backgroundColor = 'transparent'
      }
    }
  }
}
</script>

<style>
#app {
  /* font-family: Avenir, Helvetica, Arial, sans-serif; */
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.nav-links li {
  list-style-type: none;
  text-align: left;
}

.desktop, .mobile {
  z-index: 10;
}

.main {
  margin: 0px 10vw;
}

.bg-dark-grey {
  background: #13141D;
}


@media screen and (max-width: 768px) {
  .desktop {
    display: none !important;
  }

  .mobile {
    display: flex !important;
  }

  .main {
    margin: 0px;
  }
}

.mobile {
  display: none;
}

a {
  text-decoration: none !important;
}

.brand a:hover {
  color: #FF2C1F;
}

nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
}

.nav-links {
  display: flex;
  justify-content: space-around;
  width: 600px;
}

.nav-links a {
  position: relative;
  /* text-transform: uppercase; */
  font-size: 0.975rem !important;
  font-weight: 300 !important;
}

.nav-links a::after {
  bottom: -7px;
  content: "";
  height: 3px;
  left: 50%;
  position: absolute;
  background: #FF2C1F;
  transition: width 0.3s ease 0s, left 0.3s ease 0s;
  width: 0;
}

.nav-links a:hover:after {
  width: 100%;
  left: 0;
}

.nav-bar {
  position: fixed; 
  width: 100%;
  z-index: 100;
}

.links {
  position: fixed;
  bottom: 20px;
  left: 15px;
}

.links-inverse {
  position: fixed;
  bottom: 20px;
  right: 15px;
}

.links-inverse .text {
  text-orientation: sideways-right;
  writing-mode: vertical-rl;
  letter-spacing: 2px;
  color: #FF2C1F;
}

.links ul {
  list-style-type: none;
  text-align: left;
}

.links li {
  margin-bottom: 2vh;
}

.icon {
  font-size: 25px;
  transition: 0.3s all;
}

.icon:hover {
  color: #FF2C1F;
}

.line {
  height: 100%;
  width: 1px;
  background: #FF2C1F;
}
</style>
