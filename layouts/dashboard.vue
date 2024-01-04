<template>
  <div class="overflow-hidden">
    <DashboardNavbar />
    <DashboardSidebar />
    <main class="min-h-screen overflow-y-scroll py-28 pl-36 md:pl-52">
      <slot />
    </main>
  </div>
</template>