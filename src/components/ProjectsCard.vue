<template>
    
    <div class="main-container">
        <div class="project-card" v-for="(items, index) in projectData.ProjectsArray" v-bind:key="items">
            <h2>{{ projectData.ProjectsArray[index].Title }}</h2>
            <img :src="projectData.ProjectsArray[index].Image" alt="">
            <p>{{ projectData.ProjectsArray[index].About }}</p>
            <div class="links">
                <a :href="projectData.ProjectsArray[index].Link1" target="blank">Project Link</a>
                <a :href="projectData.ProjectsArray[index].Link2" target="blank">GitHub Link</a>
            </div>
        </div>
    </div>

</template>

<script>
import jsonData from "/projects.json"
export default {
    data() {
        return {
            projectData: jsonData
        }
    }
}
</script>

<style scoped>
.main-container{
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
}

.project-card{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width:60%;
    margin: 10px;
    flex-wrap: 0 0 40%;
    background-color: white;
    border-radius: 25px;
    box-shadow: rgba(0,0,0,0.24) 0px 3px 8px;
}

.project-card img {
    height: 10rem;
}

.links{
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
}

.links a{
    margin: 5px;
}
</style>