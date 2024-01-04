<template>
  <header class="py-2 border border-x-0 border-t-0 sticky top-0 bg-white z-30">
    <div class="container">
      <div class="flex justify-between items-center">
        <h2>
          <NuxtLink href="/">daffadmr</NuxtLink>
        </h2>
        <button class="flex flex-col gap-[6px] md:hidden" :class="showNav ? 'show-nav' : ''"
          @click="() => showNav = !showNav">
          <span class="hamburger-line origin-top-left transition duration-500 ease-in-out"></span>
          <span class="hamburger-line transition duration-300 ease-in-out"></span>
          <span class="hamburger-line origin-bottom-left transition duration-500 ease-in-out"></span>
        </button>
        <nav
          class="bg-white border md:border-0 absolute right-5 top-12 max-w-[250px] w-[80vw] py-0 shadow-lg rounded-lg md:flex md:static md:bg-transparent md:shadow-none md:py-0 md:justify-end"
          :class="showNav ? '' : 'hidden'">
          <div class="flex flex-col-reverse md:flex-row gap-5 p-2 pb-5 md:p-0">
            <ul class="flex flex-col md:flex-row gap-3 md:items-center nav-home">
              <li v-for="(page, index) in pages" :key="index" class="inline-block hover:bg-gray-300 px-[5px] rounded">
                <NuxtLink class="block" :href="page.link">
                  {{ page.name }}
                </NuxtLink>
              </li>
            </ul>
          </div>
        </nav>
      </div>
    </div>
  </header>
</template>

<script>
import nav from "../utils/nav.json"

export default {
  data() {
    return {
      showNav: false,
      pages: nav
    }
  }
}
</script>