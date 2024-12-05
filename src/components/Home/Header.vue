<template>
    <header class="bg-[#1B3228]  px-4 md:px-16 py-6 text-white">
      <nav class="container mx-auto flex justify-between items-center">
        <!-- Logo -->
        <div class="flex  items-center space-x-3">
          <div class="flex items-center justify-center w-24 h-12 rounded-lg">
            <img src="../../assets/images/fclogo.png" alt="Logo">
          </div>
          <h1 class="text-lg font-bold uppercase text-[#FFFFFF] text-transparent bg-clip-text">
            Fraser Consulting
           </h1>
        </div>
  
        <!-- Desktop Navigation Links -->
        <ul class="hidden md:flex space-x-6">
          <li><a href="#home" class="hover:text-gray-400 hover:border-b transition">Home</a></li>
          <li><a href="#services" class="hover:text-gray-400 hover:border-b transition">Services</a></li>
          <li><a href="#about" class="hover:text-gray-400 hover:border-b transition">About</a></li>
          <li><a href="#contact" class="hover:text-gray-400 hover:border-b transition">Contact</a></li>
        </ul>
  
        <!-- Desktop Button -->
        <a href="#contact" class="hidden md:block px-4 py-2 border border-white rounded-md hover:bg-[#4e806a] transition">
          Get in touch
        </a>
  
        <!-- Hamburger Menu for Mobile -->
        <button class="md:hidden" @click="toggleSidebar">
          <i class="ri-menu-line text-2xl text-white"></i>
        </button>
      </nav>
  
      <!-- Sidebar for Mobile Navigation -->
      <div
        class="fixed inset-0 bg-black bg-opacity-50 z-40"
        v-if="isSidebarOpen"
        @click.self="closeSidebar"
      >
        <div
          class="w-64 bg-[#1B3228] h-full text-white py-6 px-4 absolute right-0 top-0 transition-transform transform"
          :class="{ 'translate-x-0': isSidebarOpen, 'translate-x-full': !isSidebarOpen }"
        >
          <!-- Close Button -->
          <button @click="closeSidebar" class="absolute top-4 right-4 text-gray-300">
            <i class="ri-close-line text-2xl"></i>
          </button>
  
          <!-- Sidebar Links -->
          <ul class="mt-12 space-y-6">
            <li><a href="#home" class="block hover:text-gray-400 transition" @click="closeSidebar">Home</a></li>
            <li><a href="#services" class="block hover:text-gray-400 transition" @click="closeSidebar">Services</a></li>
            <li><a href="#about" class="block hover:text-gray-400 transition" @click="closeSidebar">About</a></li>
            <li><a href="#contact" class="block hover:text-gray-400 transition" @click="closeSidebar">Contact</a></li>
          </ul>
  
          <!-- Sidebar Button -->
          <a
            href="#contact"
            class="block mt-8 px-4 border border-white py-2 bg-[#1B3228] text-center rounded-md hover:bg-[#1B3228] transition"
            @click="closeSidebar"
          >
            Get in touch
          </a>
        </div>
      </div>
    </header>
  </template>
  
  <script>
  export default {
    name: "Header",
    data() {
      return {
        isSidebarOpen: false,
      };
    },
    methods: {
      toggleSidebar() {
        this.isSidebarOpen = !this.isSidebarOpen;
      },
      closeSidebar() {
        this.isSidebarOpen = false;
      },
    },
  };
  </script>
  
  <style scoped>
  /* Ensure smooth sliding animation */
  .sidebar-enter-active,
  .sidebar-leave-active {
    transition: transform 0.3s ease-in-out;
  }
  .sidebar-enter,
  .sidebar-leave-to {
    transform: translateX(100%);
  }
  </style>
  