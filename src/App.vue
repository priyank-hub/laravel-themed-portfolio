<template>
  <div id="app">
    <div class="bg-light-grey nav-bar">
      <div class="container-fluid pt-3" :class="isVisible ? '' : 'pb-3'">
        <nav class="desktop">
          <h3 class="mb-0 text-laravel brand">
            <a href="#home" class="text-laravel">
              PP
            </a>
          </h3>
          <ul class="nav-links mb-0">
            <li v-for="item in menu" :key="item" class="menu">
              <a :href="item.url" class="text-black menu-item">
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
          <div class="col text-right" v-b-toggle.my-collapse>
            <i class="fas fa-bars" v-if="! isVisible"></i>
            <i class="fas fa-times" v-if="isVisible"></i>
          </div>
        </div>

        <b-collapse id="my-collapse" v-model="isVisible">
          <div class="pt-3">
            <ul class="p-0 mb-0">
              <li v-for="item in menu" :key="item" class="m-0 py-2 border-bottom text-black" style="font-weight: 300; list-style-type: none; text-align: left">
                <a :href="item.url" class="menu-item text-black font-size-sm" @click="isVisible = false">
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
        <HomePage msg=""/>
      </section>

      <section id="portfolio" style="padding-top: 90px">
        <Portfolio />
      </section>

      <section id="about-me" style="padding-top: 90px">
        <AboutMe />
      </section>

      <section id="resume" style="padding-top: 90px">
        <ResumeSection />
      </section>

      <section id="contact" style="padding-top: 90px">
        <Contact />
      </section>
    </div>


    <div class="d-none d-md-block">
      <div class="links d-flex flex-column align-items-center justify-content-center">
        <div>
          <ul class="p-0 mb-0">
            <li>
              <span class="icon">
                <i class="fab fa-linkedin"></i>
              </span>
            </li>
            <li>
              <span class="icon">
                <i class="fab fa-github"></i>
              </span>
            </li>
            <li>
              <span class="icon">
                <i class="fab fa-instagram"></i>
              </span>
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
      ]
    }
  },

  computed: {

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
  color: black;
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
