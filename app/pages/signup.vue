<template>
  <main class="flex-1 flex items-center justify-center mt-10">
    <div class="bg-white rounded-md shadow-md w-full max-w-md p-8 space-y-6">
      <h2 class="text-2xl font-semibold text-center mb-6 ">
     Sign Up
      </h2>
      <form @submit.prevent="handleLogin">
             <input
          class="w-full border border-gray-300 rounded px-4 py-3 mb-4 focus:outline focus:ring-2 focus:ring-blue-500"
          type="text"
          v-model="name"
          required
          placeholder="Enter your Name"
        />
        <input
          class="w-full border border-gray-300 rounded px-4 py-3 mb-4 focus:outline focus:ring-2 focus:ring-blue-500"
          type="email"
          v-model="email"
          required
          placeholder="Enter email address"
        />
        <input
          class="w-full border border-gray-300 rounded px-4 py-3 mb-4 focus:outline focus:ring-2 focus:ring-blue-500"
          type="password"
          v-model="password"
          required
          placeholder="Enter password"
        />

        <button
        type="submit"
        class="w-full bg-blue-600 text-white py-3 rounded font-medium hover:bg-blue-700 transition">
      Sign Up
        </button>
      </form>
     <p class="text-center text-gray-600 text-sm mt-6">
       Already have an account
        <NuxtLink to="/signin" class="text-blue-600 hover:underline">Sign In</NuxtLink> 
</p>
  
      
    </div>
  </main>
</template>
<script setup>
import { ref } from "vue";

const name = ref("");
const email = ref("");
const password = ref("");

function handleLogin() {
  console.log("Email:", email.value);
  console.log("Password:", password.value);
}
</script>
