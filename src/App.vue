<script setup></script>

<template>
  <div class="min-h-screen bg-gray-800">
    <div class="container mx-auto flex flex-col space-y-8 pt-8">
      <h1 class="font-thin text-center text-6xl tracking-tight text-gray-300">My Todo App</h1>
      <input type="text" class="rounded-lg text-center px-4 py-2 text-xl" placeholder="New Todo"/>
      <div class="flex justify-between">
        <div class="w-1/3">
          <h3 class="text-2xl text-center text-blue-400">Pending</h3>
          <ul class="pt-8 space-y-4">
            <li class="bg-gray-300 w-full text-center px-4 py-2 rounded-lg ">
              One
            </li>
            <li>
              Two
            </li>
          </ul>
        </div>
        <div class="w-1/3">
          <h3 class="text-2xl text-center text-green-400">Completed</h3>
          <ul>
            <li>
              Three
            </li>
          </ul>
        </div>
      </div>
      </div>
  </div>
</template>

