<template>
  <div class="bg-slate-700 fixed h-full md:w-[200px] text-white p-5 top-[75px]">
    <ul class="flex flex-col gap-5">
      <li v-for="(data, index) in sidebarList" :key="index">
        <NuxtLink class="block hover:bg-slate-500 rounded-lg p-2" :to="data.link">{{data.name}}</NuxtLink>
      </li>
    </ul>
  </div>
</template>

<script>
import sidebarList from '../../utils/sidebar.json'

export default{
  data(){
    return{
      sidebarList: sidebarList
    }
  }
}
</script>
