<template>
  <div class="">
    <!-- <h1 class="font-weight-bold">Portfolio</h1> -->

    <!-- <div class="container mb-5 position-relative">
        <div class="bar m-auto mb-4"></div>
        <div class="mb-3">
            <h4 class="fw-bold text-center">Technologies I've worked with</h4>
        </div>
        <div class="mx-0 skill-grid">
            <div class="my-4 skill-item" v-for="item in skills" :key="item">
                <a :href="item.website" target="_blank">
                    <img :src="item.url" height="55px" style="object-fit: cover" alt="">
                    <div class="subtitle text-muted mt-3">
                        {{ item.name }}
                    </div>
                </a>
            </div>
        </div>
        <div class="bar m-auto mt-4"></div>
    </div> -->

    <div class="container mt-4">
        <div class="row mx-0">
            <div class="col-12 card-item">
                <div class="row mx-0 align-items-center justify-content-between project-item">
                    <div class="col-12 col-lg-12 col-xl-6 text-left">
                        <!-- content -->
                        <h3 class="text-black fw-bold">Spotify Data Visualizer</h3>
                        <div class="text-muted">
                            <p>
                                To visualize Spotify data on the web, including playlists, top artists, top tracks, and track information. 
                                Technologies used for this project are <span class="text-laravel">Node.js</span> for the backend, <span class="text-laravel">Vue.js</span> for the frontend, <span class="text-laravel">Bootstrap</span> for css, and various Spotify APIs for data retrieval.
                            <p>
                                Key features includes:
                                <ul class="m-0">
                                    <li>User authentication: Users can log in with their Spotify account to access their data.</li>
                                    <li>A dashboard, top tracks, top artists and playlists screens that shows an overview of the user's spotify account.</li>
                                    <li>The UI is designed to be responsive and adapt to different screen sizes and devices.</li>
                                </ul>
                            </p>

                            <div class="d-flex flex-row mt-4 social">
                                <b-button class="">
                                    <span>
                                        <i class="fas fa-code mx-2"></i>
                                        Repository
                                    </span>
                                </b-button>

                                <b-button class="mx-3">
                                    <span>
                                        <i class="fas fa-external-link-alt mx-2"></i>
                                        View
                                    </span>
                                </b-button>
                            </div>
                        </div>
                    </div>

                    <div class="col-12 col-lg-12 col-xl-4 mb-5">
                        <img src="/assets/portfolio/spotify-visualizer.png" class="" width="100%" style="border-radius: 20px; transform: rotate(-1deg)" alt="">
                    </div>
                </div>
            </div>

            <div class="col-12 card-item">
                <div class="row mx-0 align-items-center justify-content-between project-item">
                    <div class="col-12 col-lg-12 col-xl-4 mb-5">
                        <img src="/assets/portfolio/bookstore.png" class="" width="100%" style="border-radius: 20px; transform: rotate(-1deg)" alt="">
                    </div>
                    <div class="col-12 col-lg-12 col-xl-6 text-left">
                        <!-- content -->
                        <h3 class="text-black fw-bold">E-Commerce Bookstore Project</h3>
                        <div class="text-muted">
                            <p>
                                Project is about Mom&Pop book store by Brick and Mortar Company, which allows users to browse, search for available books and as well as provide checkout and payment functionality.
                                It uses <span class="text-laravel">React.js</span> to render the frontend while <span class="text-laravel">Java Spring Boot</span> framework to function backend.
                            </p>
                            <p>
                                Key features includes:
                                <ul class="m-0">
                                    <li>Integration with backend APIs that provide access to the data and functionality of the application.</li>
                                    <li>Allows users to browse, search for available books and as well as provide checkout and payment functionality.</li>
                                </ul>
                            </p>

                            <div class="d-flex flex-row mt-4 social">
                                <b-button class="">
                                    <span>
                                        <i class="fas fa-code mx-2"></i>
                                        Repository
                                    </span>
                                </b-button>

                                <b-button class="mx-3">
                                    <span>
                                        <i class="fas fa-external-link-alt mx-2"></i>
                                        View
                                    </span>
                                </b-button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <div class="col-12 card-item">
                <div class="row mx-0 align-items-center justify-content-between project-item">
                    <div class="col-12 col-lg-12 col-xl-6 text-left">
                        <h3 class="text-black fw-bold">Weather Info</h3>
                        <div class="text-muted">
                            <p>
                                Weather Info is a 
                                <span class="text-laravel">HTML</span>,
                                <span class="text-laravel">CSS (Bootstrap)</span>,
                                <span class="text-laravel">JavaScript</span>
                                web application designed to keep track of live weather forecast in any city around the world using the <span class="text-laravel">OpenWeather API</span>.
                            </p>

                            <div class="d-flex flex-row mt-4 social">
                                <b-button class="">
                                    <span>
                                        <i class="fas fa-code mx-2"></i>
                                        Repository
                                    </span>
                                </b-button>

                                <b-button class="mx-3">
                                    <span>
                                        <i class="fas fa-external-link-alt mx-2"></i>
                                        View
                                    </span>
                                </b-button>
                            </div>
                        </div>
                    </div>
                    <div class="col-12 col-lg-12 col-xl-5">
                        <img src="/assets/portfolio/weatherinfo.png" class="" width="100%" style="border-radius: 20px; transform: rotate(1deg)" alt="">
                    </div>
                </div>
            </div>

            <div class="col-12 card-item">
                <div class="row mx-0 justify-content-between">
                    <div class="col-12 col-lg-6 col-xl-4 mb-4 ui-item">
                        <div class="card border-0 box-shadow p-3" style=" border-radius: 15px">
                            <div class="image">
                                <img src="/assets/portfolio/nft.png" width="100%" style="border-radius: 5px; height: 250px; object-fit: cover" alt="">
                            </div>
                            <div class="content mt-5">
                                <h4 class="text-black fw-bold">NFT Preview Card</h4>
                                <div class="text-muted subtitle">
                                    UI Component
                                </div>
                            </div>

                            <div class="d-flex flex-row mt-4 social">
                                <b-button class="">
                                    <span>
                                        <i class="fas fa-code mx-2"></i>
                                        Repository
                                    </span>
                                </b-button>

                                <b-button class="mx-3">
                                    <span>
                                        <i class="fas fa-external-link-alt mx-2"></i>
                                        View
                                    </span>
                                </b-button>
                            </div>
                        </div>
                    </div>

                    <div class="col-12 col-lg-6 col-xl-4 mb-4 ui-item">
                        <div class="card border-0 box-shadow p-3" style=" border-radius: 15px">
                            <div class="image">
                                <img src="/assets/portfolio/products-page.png" width="100%" style="border-radius: 5px; height: 250px; object-fit: cover" alt="">
                            </div>
                            <div class="content mt-5">
                                <h4 class="text-black fw-bold">An E-commerce Products Page</h4>
                                <div class="text-muted subtitle">
                                    UI Component
                                </div>
                            </div>
                            <div class="d-flex flex-row mt-4 social">
                                <b-button class="">
                                    <span>
                                        <i class="fas fa-code mx-2"></i>
                                        Repository
                                    </span>
                                </b-button>

                                <b-button class="mx-3">
                                    <span>
                                        <i class="fas fa-external-link-alt mx-2"></i>
                                        View
                                    </span>
                                </b-button>
                            </div>
                        </div>
                    </div>

                    <div class="col-12 col-lg-6 col-xl-4 mb-4 ui-item">
                        <div class="card border-0 box-shadow p-3" style=" border-radius: 15px">
                            <div class="image">
                                <img src="/assets/portfolio/countries.png" width="100%" style="border-radius: 5px; height: 250px; object-fit: cover" alt="">
                            </div>
                            <div class="content mt-5">
                                <h4 class="text-black fw-bold">Countries Info</h4>
                                <div class="text-muted subtitle">
                                    UI Component
                                </div>
                            </div>
                            <div class="d-flex flex-row mt-4 social">
                                <b-button class="">
                                    <span>
                                        <i class="fas fa-code mx-2"></i>
                                        Repository
                                    </span>
                                </b-button>

                                <b-button class="mx-3">
                                    <span>
                                        <i class="fas fa-external-link-alt mx-2"></i>
                                        View
                                    </span>
                                </b-button>
                            </div>
                        </div>
                    </div>
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
    msg: String
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
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
    font-size: 3rem;
}

h3 {
    font-size: 3rem;
    font-weight: 700;
}

.card-item {
    padding: 20px 0px 100px 0px;
}

p {
    line-height: 1.625;
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
        grid-template-columns: repeat(auto-fill, minmax(100px, 1fr)) !important;
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
    /* background: #FF2C1F; */
    /* box-shadow: 0px 0px 15px 4px rgba(255, 44, 31, 0.1); */
}
</style>