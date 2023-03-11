<template>
  <div class="">
    <!-- <h1 class="font-weight-bold">Portfolio</h1> -->

    <div class="container">
        <div class="d-flex flex-row align-items-center mx-0 reveal">
            <div class="font-size-xl text-left font-weight-bold">
                <span class="" :class="mode == 'dark' ? 'text-white' : 'text-black'">
                    Some Things I've Built
                </span>
            </div>
            <div class="line"></div>
        </div>

        <div class="row mx-0">
            <div class="col-12 card-item px-0 reveal">
                <div class="row mx-0 align-items-center justify-content-between project-item">
                    <div class="col-12 col-xl-6 text-left px-0">
                        <!-- content -->
                        <h3 class="fw-bold" :class="mode == 'dark' ? 'text-white' : 'text-black'">Spotify Data Visualizer</h3>
                        <div class="text-muted">
                            <p>
                                To visualize Spotify data on the web, including playlists, top artists, top tracks, and track information. 
                                Technologies used for this project are <span class="text-laravel">Node.js</span> for the backend, <span class="text-laravel">Vue.js</span> for the frontend, <span class="text-laravel">Bootstrap</span> for css, and various Spotify APIs for data retrieval.
                            </p>
                            <p>
                                Key features includes:
                                <ul class="m-0">
                                    <li>User authentication: Users can log in with their Spotify account to access their data.</li>
                                    <li>A dashboard, top tracks, top artists and playlists screens that shows an overview of the user's spotify account.</li>
                                    <li>The UI is designed to be responsive and adapt to different screen sizes and devices.</li>
                                </ul>
                            </p>

                            <div class="d-flex flex-row mt-4 social">
                                <a href="https://github.com/priyank-hub/spotify-profile-frontend" target="_blank" class="border-laravel text-decoration-none text-white">
                                    <div class="hover bg-laravel p-2 px-3">
                                        <i class="fas fa-code"></i>
                                        <span class="mx-2">
                                            Repository
                                        </span>
                                    </div>
                                </a>

                                <a href="https://spotify-profile-frontend.vercel.app/" target="_blank" class="border-laravel text-decoration-none text-white mx-2">
                                    <div class="hover bg-laravel p-2 px-3">
                                        <i class="fas fa-external-link-alt"></i>
                                        <span class="mx-2">
                                            View
                                        </span>
                                    </div>
                                </a>
                            </div>
                        </div>
                    </div>

                    <div class="col-12 col-xl-5 mb-5 d-md-none d-xl-block">
                        <img src="/assets/portfolio/spotify-3.png" class="" width="100%" style="border-radius: 0px" alt="">
                    </div>
                </div>
            </div>

            <div class="col-12 card-item px-0 reveal">
                <div class="row mx-0 align-items-start justify-content-between project-item">
                    <div class="col-12 col-xl-5 mb-5 d-md-none d-xl-block">
                        <img src="/assets/portfolio/gitfinder.png" class="" width="100%" style="border-radius: 0px" alt="">
                    </div>
                    <div class="col-12 col-xl-6 text-left px-0">
                        <h3 class="fw-bold" :class="mode == 'dark' ? 'text-white' : 'text-black'">GitFinder</h3>
                        <div class="text-muted">
                            <p>
                                GitFinder is a web application that allows users to search for any GitHub username and get basic information about their profile. 
                                The application uses the <span class="text-laravel">GitHub User API</span> to fetch data such as the user's followers, repository details, and other relevant information. 
                                The project is built using modern web frameworks such as <span class="text-laravel">Vue.js</span>, <span class="text-laravel">Vuetify</span>, <span class="text-laravel">JavaScript</span> and the GitHub User API. 
                            </p>

                            <div class="d-flex flex-row mt-4 social">
                                <a href="https://github.com/priyank-hub/github_users_search" target="_blank" class="border-laravel text-decoration-none text-white">
                                    <div class="hover bg-laravel p-2 px-3">
                                        <i class="fas fa-code"></i>
                                        <span class="mx-2">
                                            Repository
                                        </span>
                                    </div>
                                </a>

                                <a href="https://mygitfinder.vercel.app/" target="_blank" class="border-laravel text-decoration-none text-white mx-2">
                                    <div class="hover bg-laravel p-2 px-3">
                                        <i class="fas fa-external-link-alt"></i>
                                        <span class="mx-2">
                                            View
                                        </span>
                                    </div>
                                </a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <div class="col-12 card-item px-0 reveal">
                <div class="row mx-0 align-items-center justify-content-between project-item">
                    <div class="col-12 col-xl-6 text-left px-0">
                        <!-- content -->
                        <h3 class="fw-bold" :class="mode == 'dark' ? 'text-white' : 'text-black'">E-Commerce Bookstore Project</h3>
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
                                <a href="https://github.com/priyank-hub/Charizard-4413-FrontEnd" target="_blank" class="border-laravel text-decoration-none text-white">
                                    <div class="hover bg-laravel p-2 px-3">
                                        <i class="fas fa-code"></i>
                                        <span class="mx-2">
                                            Repository
                                        </span>
                                    </div>
                                </a>

                                <a href="https://charizard-4413-front-end-charizard4413.vercel.app/" target="_blank" class="border-laravel text-decoration-none text-white mx-2">
                                    <div class="hover bg-laravel p-2 px-3">
                                        <i class="fas fa-external-link-alt"></i>
                                        <span class="mx-2">
                                            View
                                        </span>
                                    </div>
                                </a>
                            </div>
                        </div>
                    </div>
                    <div class="col-12 col-xl-5 mb-5 d-md-none d-xl-block px-0">
                        <img src="/assets/portfolio/bookstore.png" class="" width="100%" style="border-radius: 0px" alt="">
                    </div>
                </div>
            </div>

            <div class="col-12 px-0 my-4">
                <div class="d-flex flex-row mx-0 justify-content-center align-items-center mb-4 reveal">
                    <div class="line-accent"></div>
                    <div class="fw-bold font-size-xl mx-4" :class="mode == 'dark' ? 'text-white' : 'text-black'">Some Other Projects</div>
                    <div class="line-accent"></div>
                </div>
                <div class="row">
                    <div class="col-12 col-mg-6 col-lg-4 mb-3 reveal" :class="mode == 'dark' ? 'ui-card' : 'ui-card-light'">
                        <div :class="mode == 'dark' ? 'bg-dark-grey' : 'bg-light-grey'" class="d-flex flex-column justify-content-between p-4 h-100">
                            <div class="mb-4">
                                <div class="d-flex flex-row justify-content-between w-100" style="font-size: 18px">
                                    <a href="https://github.com/priyank-hub/nft-preview-card" target="_blank" class="text-decoration-none text-secondary">
                                        <i class="fas fa-folder"></i>
                                    </a>

                                    <a href="https://nft-preview-card-five-hazel.vercel.app/" target="_blank" class="text-decoration-none text-secondary">
                                        <i class="fas fa-external-link-alt"></i>
                                    </a>
                                </div>
                            </div>
                            <div class="text-left">
                                <div class="">
                                    <h5 class="fw-bold">NFT Preview Card</h5>
                                </div>
                                <p class="text-muted font-size-sm mt-3">
                                    Towards the begining of my developer journey, I had an opportunity to practice my Frontend skills on Frontendmentor.io. 
                                    This was one of the UI component I challenged myself to complete it.
                                </p>
                            </div>
                            <div class="text-left font-size-sm">
                                <ul class="list-tech">
                                    <li>Vue.js</li>
                                    <li>Bootstrap-Vue</li>
                                </ul>
                            </div>
                        </div>
                    </div>

                    <div class="col-12 col-mg-6 col-lg-4 mb-3 reveal" :class="mode == 'dark' ? 'ui-card' : 'ui-card-light'">
                        <div :class="mode == 'dark' ? 'bg-dark-grey' : 'bg-light-grey'" class="d-flex flex-column justify-content-between p-4 h-100">
                            <div class="mb-4">
                                <div class="d-flex flex-row justify-content-between w-100" style="font-size: 18px">
                                    <a href="https://github.com/priyank-hub/e-commerce-product-page" target="_blank" class="text-decoration-none text-secondary">
                                        <i class="fas fa-folder"></i>
                                    </a>

                                    <a href="https://e-commerce-product-page-g39t.vercel.app/" target="_blank" class="text-decoration-none text-secondary">
                                        <i class="fas fa-external-link-alt"></i>
                                    </a>
                                </div>
                            </div>
                            <div class="text-left">
                                <div class="">
                                    <h5 class="fw-bold">E-Commerce Product Page</h5>
                                </div>
                                <p class="text-muted font-size-sm mt-3">
                                    This UI component features a beautiful E-commerce product page. It details the product name, description, price, images.
                                    Also, opening a lightbox gallery to give a closer look at product images with image carousel.
                                </p>
                            </div>
                            <div class="text-left font-size-sm">
                                <ul class="list-tech">
                                    <li>Vue.js</li>
                                    <li>Bootstrap-Vue</li>
                                    <li>JavaScript</li>
                                </ul>
                            </div>
                        </div>
                    </div>
                    
                    <div class="col-12 col-mg-6 col-lg-4 mb-3 reveal" :class="mode == 'dark' ? 'ui-card' : 'ui-card-light'">
                        <div :class="mode == 'dark' ? 'bg-dark-grey' : 'bg-light-grey'" class="d-flex flex-column justify-content-between p-4 h-100">
                            <div class="mb-4">
                                <div class="d-flex flex-row justify-content-between w-100" style="font-size: 18px">
                                    <a href="https://github.com/priyank-hub/REST_countries_API" target="_blank" class="text-decoration-none text-secondary">
                                        <i class="fas fa-folder"></i>
                                    </a>

                                    <a href="https://rest-countries-api-jade-iota.vercel.app/#/" target="_blank" class="text-decoration-none text-secondary">
                                        <i class="fas fa-external-link-alt"></i>
                                    </a>
                                </div>
                            </div>
                            <div class="text-left">
                                <div class="">
                                    <h5 class="fw-bold">REST Countries API</h5>
                                </div>
                                <p class="text-muted font-size-sm mt-3">
                                    By putting my Javascript and API skills to test, I built this project to display all countries and 
                                    also view more about the country by pulling data from <span class="text-laravel">REST Countries API</span>.
                                    It has a switch for light/dark modes.
                                </p>
                            </div>
                            <div class="text-left font-size-sm">
                                <ul class="list-tech">
                                    <li>Vue.js</li>
                                    <li>Vuetify</li>
                                    <li>JavaScript</li>
                                </ul>
                            </div>
                        </div>
                    </div>

                    <div class="col-12 col-mg-6 col-lg-4 mb-3 reveal" :class="mode == 'dark' ? 'ui-card' : 'ui-card-light'">
                        <div :class="mode == 'dark' ? 'bg-dark-grey' : 'bg-light-grey'" class="d-flex flex-column justify-content-between p-4 h-100">
                            <div class="mb-4">
                                <div class="d-flex flex-row justify-content-between w-100" style="font-size: 18px">
                                    <a href="https://github.com/priyank-hub/weatherinfo" target="_blank" class="text-decoration-none text-secondary">
                                        <i class="fas fa-folder"></i>
                                    </a>

                                    <a href="https://priyank-hub.github.io/weatherinfo/event.html" target="_blank" class="text-decoration-none text-secondary">
                                        <i class="fas fa-external-link-alt"></i>
                                    </a>
                                </div>
                            </div>
                            <div class="text-left">
                                <div class="">
                                    <h5 class="fw-bold">WeatherInfo</h5>
                                </div>
                                <p class="text-muted font-size-sm mt-3">
                                    Weather Info is a 
                                    web application designed to keep track of live weather forecast in any city around the world using the 
                                    <span class="text-laravel">OpenWeather API</span>.
                                </p>
                            </div>
                            <div class="text-left font-size-sm">
                                <ul class="list-tech">
                                    <li>HTML</li>
                                    <li>CSS (Sass)</li>
                                    <li>JavaScript</li>
                                </ul>
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
  name: 'Portfolio',
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
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

h3 {
    font-size: 2rem;
    font-weight: 700;
}

a:hover .hover {
  translate: -0.25rem -0.25rem !important;
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

@media screen and (max-width: 768px) {
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

    .line-accent {
        display: none !important;
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

.line {
    min-width: 25vw;
    max-width: 40vw;
    height: 1px;
    background: #FF2C1F;
    margin-left: 20px;
}

.line-accent {
    width: 40vw;
    height: 1px;
    background: #FF2C1F;
}

.list-tech {
    display: flex;
    align-items: flex-end;
    -webkit-box-flex: 1;
    flex-grow: 1;
    flex-wrap: wrap;
    padding: 0px;
    margin: 20px 0px 0px;
    list-style: none;
}

.list-tech li:not(:last-of-type) {
    margin-right: 15px;
}

.ui-card, .ui-card-light, i, h5, ul {
    transition: 0.3s all;
}

.ui-card:hover, .ui-card-light:hover {
    translate: -5px -5px;
}

.ui-card i:hover, .ui-card-light i:hover {
    color: #FF2C1F;
}

.ui-card:hover h5, .ui-card:hover ul, .ui-card:hover p {
    color: #fff !important;
}
</style>
