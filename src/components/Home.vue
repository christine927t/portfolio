<template>
    <div class="container">
        <div class="row">
            <div class="col-12 col-lg-6 main-heading">
               <h1 class="">Hey I'm Christine</h1>
               <h3>A front end web developer</h3>
               <div class="watermark-container">
                   <div class="watermark watermark-1"></div>
                   <div class="watermark watermark-2"></div>
                   <div class="watermark watermark-3"></div>
               </div>
            </div>
        </div>
        <a href="#projects">
            <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" fill="#4c4c4c" class="bi bi-arrow-down" viewBox="0 0 16 16">
                <path fill-rule="evenodd" d="M8 1a.5.5 0 0 1 .5.5v11.793l3.146-3.147a.5.5 0 0 1 .708.708l-4 4a.5.5 0 0 1-.708 0l-4-4a.5.5 0 0 1 .708-.708L7.5 13.293V1.5A.5.5 0 0 1 8 1z"/>
            </svg>
        </a>
        <h3 class="work-heading">Here's some of my work...</h3>
        <div class="row" id="projects">
            <div v-for="(project, i) in projects" :key="i" class="col-12 col-sm-6 col-md-4 col-lg-3 mb-5 each-project">
                {{project.title}}
                <img :src="project.image" alt="project image" />
                <div class="overlay align-items-center justify-content-center flex-column">
                    <a :href="project.demo">
                        <button class="project-btn rounded-pill mb-3">
                            <svg xmlns="http://www.w3.org/2000/svg" width="35" height="35" fill="#FBF7E9" class="bi bi-display pl-2 pr-2" viewBox="0 0 16 16">
                                <path d="M0 4s0-2 2-2h12s2 0 2 2v6s0 2-2 2h-4c0 .667.083 1.167.25 1.5H11a.5.5 0 0 1 0 1H5a.5.5 0 0 1 0-1h.75c.167-.333.25-.833.25-1.5H2s-2 0-2-2V4zm1.398-.855a.758.758 0 0 0-.254.302A1.46 1.46 0 0 0 1 4.01V10c0 .325.078.502.145.602.07.105.17.188.302.254a1.464 1.464 0 0 0 .538.143L2.01 11H14c.325 0 .502-.078.602-.145a.758.758 0 0 0 .254-.302 1.464 1.464 0 0 0 .143-.538L15 9.99V4c0-.325-.078-.502-.145-.602a.757.757 0 0 0-.302-.254A1.46 1.46 0 0 0 13.99 3H2c-.325 0-.502.078-.602.145z"/>
                            </svg>Live Demo
                        </button>
                    </a>
                    <a :href="project.github">
                        <button class="project-btn rounded-pill">
                            <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" fill="#FBF7E9" class="bi bi-code-slash pl-2 pr-2" viewBox="0 0 16 16">
                                <path d="M10.478 1.647a.5.5 0 1 0-.956-.294l-4 13a.5.5 0 0 0 .956.294l4-13zM4.854 4.146a.5.5 0 0 1 0 .708L1.707 8l3.147 3.146a.5.5 0 0 1-.708.708l-3.5-3.5a.5.5 0 0 1 0-.708l3.5-3.5a.5.5 0 0 1 .708 0zm6.292 0a.5.5 0 0 0 0 .708L14.293 8l-3.147 3.146a.5.5 0 0 0 .708.708l3.5-3.5a.5.5 0 0 0 0-.708l-3.5-3.5a.5.5 0 0 0-.708 0z"/>
                            </svg>GitHub Repo
                        </button>
                    </a>
                </div>
            </div>
        </div>
        <div id="#experience">
            <h3>A bit about my experience...</h3>

        </div>
    </div>
</template>

<script>
export default{
    data(){
        return {
            projects: [
                {
                    title: "React full stack 'Courses' app",
                    image: require('../assets/img/project-images/react-app-sq3.png'),

                },
                {
                    title: "React gallery/Flickr app",
                    image: require('../assets/img/project-images/react-gallery-sq.png'),
                    demo: "https://react-gallery-ct.herokuapp.com/mountain",
                    github: "https://github.com/christine927t/react-with-api-gallery",
                },
                {
                    title: "Fetch API requests",
                    image: require('../assets/img/project-images/api-requests-sq.png'),
                    demo: "https://christine927t.github.io/public-API-requests/",
                    github: "https://github.com/christine927t/public-API-requests",
                },
                {
                    title: "JQuery form with validation",
                    image: require('../assets/img/project-images/interactive-jquery-sq.png'),
                    demo: "https://christine927t.github.io/Interactive-jQuery-Form/",
                    github: "https://github.com/christine927t/Interactive-jQuery-Form",
                },
                {
                    title: "Guessing game app",
                    image: require('../assets/img/project-images/guessing-game-sq2.png'),
                    demo: "https://christine927t.github.io/JS-guessing-game-app/",
                    github: "https://github.com/christine927t/JS-guessing-game-app",
                },
                {
                    title: "Student list with pagination & filtering",
                    image: require('../assets/img/project-images/list-filtering-sq.png'),
                    demo: "https://christine927t.github.io/Student-List-Pagination-Filtering/",
                    github: "https://github.com/christine927t/Student-List-Pagination-Filtering",
                },
                {
                    title: "Random quote generator",
                    image: require('../assets/img/project-images/quote-generator-sq.png'),
                    demo: "https://christine927t.github.io/Random-Quote-Generator/",
                    github: "https://github.com/christine927t/Random-Quote-Generator",
                }

            ]
        }
    }
}

</script>
