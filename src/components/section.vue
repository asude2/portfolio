<template>
  <div>
    <section id="about" :class="isDark ? 'about-dark' : 'about-light'">
      <div class="about-text">
        <h1>HELLO <br> MY NAME IS ASUDE </h1>
        <p>I am a third-year computer engineering student at Karadeniz Technical University.</p>
      </div>
      <img :class="isDark ? 'img-dark' : 'img-light'" src="/public/images/gorsel.jpg" alt="">
    </section>

    <section id="projects" :class="isDark ? 'project-dark' : 'project-light'">
      <h2 class="proj-title text-gray-400 mb-12 ml-20 mt-10 tracking-wide text-4xl" :class="isDark ? 'projectTitle-dark' : 'projectTitle-light'">MY PROJECTS</h2>
      <div class="proj-content">
        <div class="app w-64 bg-gray-200 m-4 p-10 px-10 rounded-[50px] shadow-[0_4px_15px_rgba(0,0,0,1)] flex flex-col justify-between"  :class="isDark ? 'projectContent-dark' : 'projectContent-light'">
          <h2 class="text-xl mb-3 font-bold">Earthquake Rescue Application</h2>
          <p>
            A mobile application designed to quickly share the locations and information of people trapped under debris after an earthquake with authorities and the public. Authorities can track these locations on a map and update the status of rescued individuals.
          </p>
          <p class="tech" :class="isDark ? 'tech-dark' : 'tech-light'">Technology: Flutter</p>
          <button class="border border-gray-400 bg-gray-300 px-2 py-2 rounded-[10px] ml-1 mt-10 mb-0 cursor-pointer" @click="openGithub" :class="isDark ? 'projectButton-dark' : 'projectButton-light'">Github Project</button>
        </div>
        <div class="app w-64 bg-gray-200 m-4 p-10 px-10 rounded-[50px] shadow-[0_4px_15px_rgba(0,0,0,1)] flex flex-col justify-between" :class="isDark ? 'projectContent-dark' : 'projectContent-light'">
          <h2 class="text-xl font-bold">Sigortam.net application interface</h2>
          <p>
            I created the interface of the Sigortam.net application using pure JavaScript.
          </p>
          <p class="tech" :class="isDark ? 'tech-dark' : 'tech-light'">Technology: HTML CSS JavaScript</p>
          <button class="border border-gray-400 bg-gray-300 px-2 py-2 rounded-[10px] ml-1 mt-10 mb-0 cursor-pointer" @click="openGithub2" :class="isDark ? 'projectButton-dark' : 'projectButton-light'">Github Project</button>
        </div>
        <div class="app w-64 bg-gray-200 m-4 p-10 px-10 rounded-[50px] shadow-[0_4px_15px_rgba(0,0,0,1)] flex flex-col justify-between" :class="isDark ? 'projectContent-dark' : 'projectContent-light'">
          <h2 class="text-xl font-bold">Calculator Application</h2>
          <p>  
            This calculator app can calculate all operations. It is written in pure JavaScript.
          </p>
          <p class="tech" :class="isDark ? 'tech-dark' : 'tech-light'">Technology: HTML CSS JavaScript</p>
          <button class="border border-gray-400 bg-gray-300 px-2 py-2 rounded-[10px] ml-1 mt-10 mb-0 cursor-pointer" @click="openGithub3" :class="isDark ? 'projectButton-dark' : 'projectButton-light'">Github Project</button>
        </div>
      </div>
    </section>

    <section id="accounts" :class="isDark ? 'account-dark' : 'account-light'">
      <h2 class="accounts-title">CONTACT & ACCOUNTS</h2>
      <div class="icons">
        <i class="fa-brands fa-github" @click="openGit" :class="isDark ? 'icon-dark' : 'icon-light'"></i>
        <i class="fa-brands fa-linkedin" @click="openLinkedin" :class="isDark ? 'icon-dark' : 'icon-light'"></i>
        <i class="fa-solid fa-envelope" @click="openMail" :class="isDark ? 'icon-dark' : 'icon-light'"></i>
      </div>
    </section>
  </div>
</template>

<script>
export default{
    props: ['isDark'],
    methods:{
        openGithub(){
            window.open('https://github.com/asude2/softwareEngineering_project.git')
        },
        openGithub2(){
            window.open('https://github.com/asude2/sigortamnetArayuz.git')
        },
        openGithub3(){
            window.open('https://github.com/asude2/hesapMakinesi.git')
        },
        openGit(){
            window.open('https://github.com/asude2')
        },
        openLinkedin(){
            window.open('https://www.linkedin.com/in/asude-kalg%C4%B1-826006286/')
        },
        openMail(){
            window.location.href="mailto:asuderuken63@gmail.com";
        }
    }
}
</script>

<style scoped>
/* about section */
#about{
    display: flex;
    flex-wrap: wrap;
}
.about-text{
    margin:7rem 5rem;
    color:rgb(91, 91, 91);
}
#about h1{
    font-size: 40px;
}
#about p{
    font-size: 20px;
    color:rgb(0, 0, 0);
}
#about img{
    height: 300px;
    width: auto;
    margin: 5rem 8rem;
    border-radius: 100%;
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.8);
}


/* project section */
#projects{
    background-color: rgb(65, 65, 65);
    padding:1rem
}

.tech{
    font-weight: 600;
    font-size: 16px;
    color:rgb(69, 69, 69)
}
.app button:hover{
    background-color: rgb(238, 238, 238);
    border:solid 1px rgb(183, 182, 182);
}

.proj-content{
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
}



/*accounts section*/ 
.accounts-title{
    color:rgb(65, 65, 65);
    letter-spacing: 2px;
    font-size: 40px;
    margin-top: 4rem;
    display: flex;
    justify-content: center;
}
.icons{
    font-size: 2rem;
    display: flex;
    margin-top: 3rem;
    margin-bottom: 3rem;
    justify-content: center;
}
.icons i{
    margin:0 2rem;
    transition: transform 0.3s ease;
}
.icons i:hover{
    transform: scale(1.2);
    cursor: pointer;
}




/* -----------dark-light mod----------------- */

/* about mode */
.about-light {
  background-color: rgb(219, 217, 217);
  transition: all 1s ease;
}
.about-dark{
  background-color: #000000;
  transition: all 1s ease;
}
.about-dark * {
  color: white !important;
}
.about-light * {
  color: rgb(86, 86, 86);
}
.about-dark img {
    box-shadow: 0 0 30px 15px rgba(255, 255, 255, 0.2) !important;
}


/* project mode */
.project-dark{
    background-color: rgb(198, 198, 198) !important;
    transition: all 1s ease;
}
.project-light{
    transition: all 1s ease;
}
.projectTitle-dark  {
    color:rgb(255, 255, 255);
}
.projectTitle-light {
  color: rgb(199, 199, 199);
      transition: all 1s ease;
}
.projectContent-dark{
    background-color: #000000;
    color:rgb(255, 255, 255);
    transition: all 1s ease;
}
.projectButton-dark{
    background-color: rgb(231, 231, 231) !important;
}
.tech-dark{
    color:rgb(147, 147, 147)
}


/* account mode */
.account-dark{
    background-color: #000000;
    padding: 0.1px;
    transition: all 1s ease;
}
.account-light{
    transition: all 1s ease;
}
.account-dark *{
    color:rgb(228, 228, 228);
    transition: all 1s ease;
}
.icon-dark{
    color: rgb(255, 255, 255);
}

</style>

