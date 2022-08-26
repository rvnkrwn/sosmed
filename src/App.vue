<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header class="h-screen bg-blue-600 top-0 left-0 p-4 w-24 sm:w-96 text-white shadow-inner z-40">
    <div class="text-center text-xl font-semibold tracking-wide mb-5">
      <img src="https://karaktereling.org/wp-content/uploads/2019/03/users-vector-icon-png_260862.jpg" alt="" class="w-16 rounded-2xl mx-auto">
      <div class="userName my-2 flex justify-center text-sm">
        <p class="font-semibold self-center mx-1 hidden sm:block">Revan Kurniawan</p>
        <i class="fal fa-chevron-down self-center mx-1 cursor-pointer" onclick="document.querySelector('.logoutButton').classList.toggle('hidden');"></i>
        <div class="logoutButton absolute translate-y-4 sm:translate-y-6 bg-black text-white hover:text-red-500 px-2 py-3 w-full hidden z-50">
          <a href=""><p class="text-sm font-normal"><i class="fal fa-sign-out"></i><span class="hidden sm:inline"> Logout</span></p></a>
        </div>
      </div>
    </div>
    <hr>
    <nav class="mt-8">
      <RouterLink to="/" class="block p-2 m-2 text-center sm:text-start sm:pl-3"><i class="fal fa-home"></i><span class="hidden sm:inline"> Home</span></RouterLink>
      <RouterLink to="/people" class="block p-2 m-2 text-center sm:text-start sm:pl-3"><i class="fal fa-users"></i><span class="hidden sm:inline"> People</span></RouterLink>
      <RouterLink to="/call" class="block p-2 m-2 text-center sm:text-start sm:pl-3"><i class="fal fa-phone"></i><span class="hidden sm:inline"> Calls</span></RouterLink>
      <RouterLink to="/chat" class="block p-2 m-2 text-center sm:text-start sm:pl-3"><i class="fal fa-comment-alt"></i><span class="hidden sm:inline"> Chats</span></RouterLink>
      <RouterLink to="/setting" class="block p-2 m-2 text-center sm:text-start sm:pl-3"><i class="fal fa-cog"></i><span class="hidden sm:inline"> Setting</span></RouterLink>
    </nav>
  </header>
  <main class="bg-white z-50 shadow-xl shadow-black/80 w-full rounded-l-3xl p-2 h-screen">
    <div class="border-b py-4 px-2">
      <div class="toggle cursor-pointer" onclick="document.querySelector('.toggle').classList.toggle('navOpen'); document.querySelector('header').classList.toggle('hidden'); document.querySelector('main').classList.toggle('rounded-l-3xl');">
        <div class="navButton"></div>
      </div>
    </div>
    <RouterView />
  </main>
</template>