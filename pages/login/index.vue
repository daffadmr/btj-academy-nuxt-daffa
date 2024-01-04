<template>
  <div class="container min-h-screen flex flex-col gap-8 items-center justify-center align-middle">

    <div class="form-container rounded-lg shadow-lg max-w-xs sm:min-w-[480px]">
      <div class="form-head bg-slate-700 px-10 py-8 rounded-t-lg">
        <h1 class="text-white font-semibold text-center text-3xl">Login</h1>
      </div>
      <form class="form-body flex flex-col p-10 gap-5">
        <input type="text" placeholder="Username"
          class="focus:border-black border rounded-lg px-4 py-2 focus:ring-0 placeholder:font-medium" />
        <input type="password" placeholder="Password"
          class="focus:border-black border rounded-lg px-4 py-2 focus:ring-0 placeholder:font-medium" />
        <label for="remember" class="flex items-center gap-2 text-sm"><input type="checkbox" name="remember" id="remember"
            class="border-slate rounded-sm text-slate focus:ring-offset-0 focus:ring-0" />Remember me</label>
        <input class="bg-slate-700 py-[10px] rounded-lg text-white hover:cursor-pointer hover:bg-slate-600" type="button"
          value="Sign In" @click="()=> navigateTo('dashboard')"/>
        <a href="#" class="text-center text-sm">Forgot your Password?</a>
        <div class="sign-up flex justify-between items-center">
          <p class="text-sm tracking-wide">
            Don't have an account? Create now!
          </p>
          <input
            class="w-[94px] bg-slate-700 text-white text-center py-2 border-2 rounded-lg text-sm border-slate text-slate hover:cursor-pointer"
            type="button" value="Sign Up" />
        </div>
      </form>
    </div>
    <NuxtLink class="flex items-center underline underline-offset-4 text-lg" to="/">&larr; Back to Home</NuxtLink>
  </div>
</template>

<script>
definePageMeta({
  layout: false
})
</script>