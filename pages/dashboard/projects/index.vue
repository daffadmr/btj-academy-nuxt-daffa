<template>
  <div class="container">
    <div class="flex flex-col gap-10">
      <div class="projects-data flex flex-col gap-5">
        <h1>Current Data</h1>
        <div class="cards flex items-center justify-around flex-wrap gap-5">
          <div v-for="(project, index) in projects" :key="index"
            class="card-project flex flex-col items-center rounded-lg bg-primary-100 shadow-lg p-5 min-h-[350px]">
            <div class="card-image-container">
              <img :src="project.img" :alt="project.name" width="150" height="200" />
            </div>
            <div class="card-text-container flex flex-col gap-5 w-full py-5 px-5 max-w-[200px]">
              <div class="card-text-header flex justify-between items-center">
                <h3 class="sm:text-xl font-bold">{{ project.name }}</h3>
              </div>
              <p class="min-h-[80px]">{{ project.desc }}</p>
            </div>
            <div class="flex gap-2">
              <button class="bg-blue-600 text-white py-2 px-5 rounded-lg">Edit</button>
              <button class="bg-red-600 text-white py-2 px-5 rounded-lg">Delete</button>
            </div>
          </div>
        </div>
      </div>
      <div class="edit-form flex flex-col gap-5">
        <h1>Add projects</h1>
        <form class="flex flex-col gap-5 items-start">
          <div class="input-group w-full">
            <input type="text" class="border border-slate-700 rounded-sm p-2 w-full md:w-1/2"
              placeholder="Enter Name">
          </div>
          <div class="input-group w-full">
            <input type="text" class="border border-slate-700 rounded-sm p-2 w-full md:w-1/2"
              placeholder="Enter Description">
          </div>
          <div class="input-group w-full">
            <input type="text" class="border border-slate-700 rounded-sm p-2 w-full md:w-1/2"
              placeholder="Enter Link">
          </div>
          <div class="input-group w-full">
            <input type="file" class="border border-slate-700 rounded-sm p-2 w-full md:w-1/2"
              placeholder="Enter Description">
          </div>
          <button type="button" class="bg-slate-700 text-white px-6 py-2 rounded-lg">Add</button>
        </form>
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
definePageMeta({
  layout: 'dashboard'
})
</script>