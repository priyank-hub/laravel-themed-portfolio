<template>
  <div id="app">
    <div class="" style="position: fixed; top: 80px; right: 20px; z-index: 100">
      <label for="night-light-checkbox" class="night-light-label" :class="mode == 'dark' ? 'bg-black' : 'bg-white'">
        <input type="checkbox" id="night-light-checkbox" v-model="checkMode">
        <span class="night-light-ball"></span>
        <svg viewBox="0 0 512 512" class="sun-svg" :class="mode == 'dark' ? 'fill-white' : 'fill-black'">
          <path id="sun-svg" d="M256 160c-52.9 0-96 43.1-96 96s43.1 96 96 96 96-43.1 96-96-43.1-96-96-96zm246.4 80.5l-94.7-47.3 33.5-100.4c4.5-13.6-8.4-26.5-21.9-21.9l-100.4 33.5-47.4-94.8c-6.4-12.8-24.6-12.8-31 0l-47.3 94.7L92.7 70.8c-13.6-4.5-26.5 8.4-21.9 21.9l33.5 100.4-94.7 47.4c-12.8 6.4-12.8 24.6 0 31l94.7 47.3-33.5 100.5c-4.5 13.6 8.4 26.5 21.9 21.9l100.4-33.5 47.3 94.7c6.4 12.8 24.6 12.8 31 0l47.3-94.7 100.4 33.5c13.6 4.5 26.5-8.4 21.9-21.9l-33.5-100.4 94.7-47.3c13-6.5 13-24.7.2-31.1zm-155.9 106c-49.9 49.9-131.1 49.9-181 0-49.9-49.9-49.9-131.1 0-181 49.9-49.9 131.1-49.9 181 0 49.9 49.9 49.9 131.1 0 181z">
          </path>
        </svg>
        <svg viewBox="0 0 512 512" class="moon-svg" :class="mode == 'dark' ? 'fill-white' : 'fill-black'">
          <path id="moon-svg" d="M283.211 512c78.962 0 151.079-35.925 198.857-94.792 7.068-8.708-.639-21.43-11.562-19.35-124.203 23.654-238.262-71.576-238.262-196.954 0-72.222 38.662-138.635 101.498-174.394 9.686-5.512 7.25-20.197-3.756-22.23A258.156 258.156 0 0 0 283.211 0c-141.309 0-256 114.511-256 256 0 141.309 114.511 256 256 256z">
          </path>
        </svg>
      </label>
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
          <div class="">
            <ul class="p-0 mb-0 d-flex flex-column justify-content-around overflow-auto" style="height: 94vh;">
              <li v-for="(item, index) in menu" :key="index" class="m-0 text-center" style="font-weight: 300; list-style-type: none">
                <div class="d-flex flex-row align-items-center justify-content-between">
                  <a :href="item.url" class="menu-item font-size-xl" :class="mode == 'dark' ? 'text-white' : 'text-black'" @click="isVisible = false">
                    {{ item.name }}
                  </a>
                  <div class="line-accent"></div>
                </div>
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
            <li class="">
              <a href="https://github.com/priyank-hub" target="_blank">
                <span class="icon" :class="mode == 'dark' ? 'text-laravel' : 'text-black'">
                  <i class="fab fa-github"></i>
                </span>
              </a>
            </li>
            <li class="">
              <a href="https://www.linkedin.com/in/priyank9/" target="_blank">
                <span class="icon" :class="mode == 'dark' ? 'text-laravel' : 'text-black'">
                  <i class="fab fa-linkedin"></i>
                </span>
              </a>
            </li>
            <li class="">
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
      <footer class="">
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
      mode: this.getMode(),
      checkMode: this.getCheckMode(),
    }
  },

  computed: {

  },
  
  mounted() {
    const darkCheck = document.getElementById('night-light-checkbox');

    darkCheck.addEventListener('click', () => {
      if (darkCheck.checked) {
        this.mode = 'dark';
        localStorage.setItem('mode', 'dark');
        document.body.style.backgroundColor = '#171923'
        // document.body.classList.add('dark');
        // localStorage.setItem('animate-css', 'dark');
      } 
      else {
        this.mode = 'light';
        localStorage.setItem('mode', 'light');
        document.body.style.backgroundColor = 'transparent'
        // document.body.classList.remove('dark');
        // localStorage.removeItem('animate-css');
      }
    })

    window.addEventListener("scroll", () => {
      var reveals = document.querySelectorAll(".reveal");
      for (var i = 0; i < reveals.length; i++) {
        var windowHeight = window.innerHeight;
        var elementTop = reveals[i].getBoundingClientRect().top;
        var elementVisible = 70;

        if (elementTop < windowHeight - elementVisible) {
          reveals[i].classList.add("active");
        } else {
          reveals[i].classList.remove("active");
        }
      }
    });
  },

  methods: {
    getMode() {
      let t = localStorage.getItem('mode');
      if (t == 'dark') {
        document.body.style.backgroundColor = '#171923';
      }
      else if (t == 'light') {
        document.body.style.backgroundColor = 'transparent';
      }
      return t ? t : 'light';
    },

    getCheckMode() {
      let t = localStorage.getItem('mode');

      if (t == 'dark') {
        return true;
      }
      else if (t == 'light') {
        return false;
      }

      return true;
    },

    reveal() {
      
    },
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

.fill-white {
  fill: white;
}

.fill-black {
  fill: black;
}

.bg-black {
  background: black;
}

.night-light-label {
  display: block;
  margin: 20px 0;
  height: 31px;
  width: 60px;
  border: 2px solid #FF2C1F;
  border-radius: 30px;
  position: relative;
  cursor: pointer;
}

.night-light-label #night-light-checkbox {
  position: absolute;
  visibility: hidden;
}

.night-light-label .night-light-ball {
  position: absolute;
  width: 25px;
  height: 25px;
  top: 1px;
  left: 1px;
  border-radius: 50%;
  background: #FF2C1F;
  z-index: 99;
  transition: 300ms;
}

.moon-svg, .sun-svg {
  width: 16px;
  height: 16px;
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
}

.sun-svg {
  left: 5px;
}

.moon-svg {
  right: 5px;
}

.night-light-label #night-light-checkbox:checked + .night-light-ball {
  transform: translateX(28px);
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

.line-accent {
  height: 1px;
  width: 67%;
  background: #FF2C1F;
}
</style>
