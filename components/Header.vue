<template>
  <header>
    <nav class="flex items-center justify-between flex-wrap bg-yellow-500 p-6">
      <div class="flex items-center flex-shrink-0 text-black">
        <!-- <img src="https://bvb-quiniela.web.app/img/bvb-logo.8bb6b939.svg" class="w-20 h-20"> -->
        <nuxt-link class="text-black hover:underline" to="/">
          <span class="font-bold text-gray-800 text-xl text-left">BVB-Quiniela</span>
        </nuxt-link>
      </div>
      <div class="flex items-center flex-shrink-0 text-black">
        <nuxt-link class="text-black hover:underline" to="/">
          English
        </nuxt-link>
        <span>|</span>
        <nuxt-link class="text-black hover:underline" to="/es">
          Español
        </nuxt-link>
      </div>
    </nav>
  </header>
</template>
