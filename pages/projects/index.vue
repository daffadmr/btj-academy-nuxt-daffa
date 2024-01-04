<template>
  <div class="container">
    <div class="about-body-projects flex flex-col gap-6 items-center">
      <h2 class="font-bold text-2xl">My Projects</h2>
      <div class="cards flex items-center justify-center flex-wrap gap-12">
        <div v-for="(project, index) in projects" :key="index"
          class="card-project flex flex-col items-center rounded-lg bg-primary-100 max-w-[300px] sm:min-w-[400px] shadow-lg">
          <div class="card-image-container relative w-full h-[200px]">
            <img :src="project.img" :alt="project.name" class="absolute object-cover w-full h-full rounded-t-lg" />
          </div>
          <div class="card-text-container flex flex-col gap-5 w-full min-h-[152px] py-7 px-5 max-w-[400px]">
            <div class="card-text-header flex justify-between items-center">
              <h3 class="text-xl sm:text-xl font-bold">{{ project.name }}</h3>
              <a :href="project.link" target="_blank">
                <svg width="20px" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <g id="Interface / External_Link">
                    <path id="Vector"
                      d="M10.0002 5H8.2002C7.08009 5 6.51962 5 6.0918 5.21799C5.71547 5.40973 5.40973 5.71547 5.21799 6.0918C5 6.51962 5 7.08009 5 8.2002V15.8002C5 16.9203 5 17.4801 5.21799 17.9079C5.40973 18.2842 5.71547 18.5905 6.0918 18.7822C6.5192 19 7.07899 19 8.19691 19H15.8031C16.921 19 17.48 19 17.9074 18.7822C18.2837 18.5905 18.5905 18.2839 18.7822 17.9076C19 17.4802 19 16.921 19 15.8031V14M20 9V4M20 4H15M20 4L13 11"
                      stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                  </g>
                </svg></a>
            </div>
            <p>{{ project.desc }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import projects from "../../utils/projects.json"

export default {
  data() {
    return {
      projects: projects
    }
  }
}
</script>