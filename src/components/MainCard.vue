<template>
  <div class="wrapper">
    <div class="main-container">
      <div class="container-one">
        <div class="profile">
          <img src="../assets/profile-cute.jpg" alt="profile picture" />
          <h3>Amir Zaman</h3>
          <p>Software Developer</p>
        </div>
        <div class="social-links">
          <div class="link">
            <img src="../assets/github.png" alt="github logo" />
            <a href="https://github.com/avzaman" target="blank">
              <h2>GitHub</h2>
            </a>
          </div>
          <div class="link">
            <img src="../assets/linkedin.png" alt="linkedin logo" />
            <a href="https://www.linkedin.com/in/avzaman/" target="blank">
              <h2>LinkedIn</h2>
            </a>
          </div>
          <div class="link">
            <img src="../assets/leetcode.png" alt="leetcode logo" />
            <a href="https://leetcode.com/u/avzaman/" target="blank">
              <h2>LeetCode</h2>
            </a>
          </div>
        </div>
      </div>
      <div class="container-two">
        <div class="about-me">
          <h1>About Me</h1>
          <p>
            I have a deep passion for programming and studying, 
            finding immense satisfaction in solving complex problems 
            and continuously expanding my knowledge. 
            The logical precision of coding and the endless 
            possibilities of learning new technologies keep me engaged 
            and motivated. Alongside my love for the technical world, 
            I also have a strong appreciation for drawing and art. 
            The creative freedom and expressive nature of art allow 
            me to unwind and explore different perspectives, 
            balancing the analytical rigor of programming with the 
            imaginative flow of artistic creation. This blend of 
            interests enriches my life, providing a harmonious mix of 
            intellectual challenge and creative expression.
          </p>
        </div>
        <div class="technology">
          <h1>Technologies Studied</h1>
          <div class="logos">
            <img src="../assets/python-logo.png" alt="python logo" />
            <img src="../assets/C-logo.png" alt="C logo" />
            <img src="../assets/JavaScript-logo.png" alt="javascript logo" />
            <img src="../assets/html-logo.png" alt="html logo" />
          </div>
        </div>
        <div class="button-container">
          <div class="projects-button">
            <a href="#" @click.prevent="scrollToSection('projects')">My Projects</a>
          </div>
          <div class="projects-button">
            <a href="#" @click.prevent="scrollToSection('resume')">My Resume</a>
          </div>
        </div>
      </div>
    </div>
  </div>
  
</template>

<script>
export default{
  methods:{
    scrollToSection(section){
      this.$emit('scroll-to-section', section)
    }
  }
}
</script>

<style scoped>
.wrapper{
  display: flex;
  justify-content: center;
}

img {
  height: 20px;
}

.main-container {
  display: flex;
  flex-direction: row;
  background-color: #8fa6f0;
  border-radius: 25px;
  width: 90%;
  box-shadow: rgba(0,0,0,0.24) 0px 3px 8px;
}

.container-one {
  background-color: #4973ff;
  padding: 5%;
  width: 30%;
  border-radius: 25px;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  box-shadow: rgba(0,0,0,0.24) 0px 3px 8px;
}

.profile img {
  height: 7rem;
  border-radius: 10%;
  margin-left: 2rem;
  margin-right: 2rem;
}

.link a{
  text-decoration: none;
  color: #000000;
  font-size: 12px;
}

.link img{
  height: 2rem;
}

.container-two {
  margin: 2.5%;
  width: 70%;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
}

.about-me p{
  text-align: left;
  margin-left: 10px;
  margin-right: 10px;
}

.logos img{
  height: 2.5rem;
  margin-left: 5px;
  margin-right: 5px;
}

.button-container{
  margin-top: 5%;
  display: flex;
  flex-direction: row;
  justify-content: center;
}

.projects-button{
  background-color: #ba3ef3;
  border-radius: 15px;
  padding: 5px;
  margin: 5px;
}

.projects-button a{
  text-decoration: none;
  color: #ffffff
}

@media (max-width: 768px) {
  .main-container {
    flex-direction: column;
    width: 100%;
  }

  .container-one,
  .container-two {
    width: 100%;
    margin: 10px 0;
  }

  .profile img {
    height: 5rem;
    margin-left: 0;
    margin-right: 0;
  }

  .about-me p {
    text-align: center;
    margin-left: 5px;
    margin-right: 5px;
  }

  .logos img {
    height: 2rem;
    margin: 5px;
  }

  .button-container {
    flex-direction: column;
  }

  .projects-button {
    width: 80%;
    margin: 10px 0;
  }
}
</style>
