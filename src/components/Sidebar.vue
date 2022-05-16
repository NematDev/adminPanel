<template>
  <div class="relative flex min-h-screen">
    <!-- Sidebar -->
    <div
      class="bg-cyan-800 
      text-cyan-100 
      w-64 
      space-y-2 
      px-2 
      absolute 
      inset-y-0 
      left-0 
      md:relative 
      md:-translate-x-0 
      transform 
      -translate-x-full 
      tansition 
      duration-200 
      ease-in-out
      "
      :class="{ 'relative -translate-x-0' : showSidebar }"
    >
      <a class="flex py-3 px-4 items-center space-x-2" href="">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="h-10 w-10"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
          stroke-width="2"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M14 10l-2 1m0 0l-2-1m2 1v2.5M20 7l-2 1m2-1l-2-1m2 1v2.5M14 4l-2-1-2 1M4 7l2-1M4 7l2 1M4 7v2.5M12 21l-2-1m2 1l2-1m-2 1v-2.5M6 18l-2-1v-2.5M18 18l2-1v-2.5"
          />
        </svg>
        <span class="text-2xl font-extrabold text-white">Laraveller</span>
      </a>
      <nav>
        <a
          href="/"
          class="group flex items-center py-3 px-4 space-x-2 hover:bg-cyan-900 rounded hover:text-cyan-300"
          ><svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-6 w-6"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
            stroke-width="2"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"
            />
          </svg>
          <span class="text-white group-hover:text-cyan-300">Dashboard</span>
        </a>
        <a
          href="/"
          class="group flex items-center py-3 px-4 space-x-2 hover:bg-cyan-900 rounded hover:text-cyan-300 transition duration-200"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-6 w-6"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
            stroke-width="2"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M12 4.354a4 4 0 110 5.292M15 21H3v-1a6 6 0 0112 0v1zm0 0h6v-1a6 6 0 00-9-5.197M13 7a4 4 0 11-8 0 4 4 0 018 0z"
            />
          </svg>
          <span class="text-white group-hover:text-cyan-300">Team</span>
        </a>
        <a
          class="group flex items-center py-3 px-4 space-x-2 hover:bg-cyan-900 rounded hover:text-cyan-300"
          href="/"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-6 w-6"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
            stroke-width="2"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z"
            />
          </svg>
          <span class="text-white group-hover:text-cyan-300">Projects</span>
        </a>
        <a
          class="group flex items-center py-3 px-4 space-x-2 hover:bg-cyan-900 rounded hover:text-cyan-300"
          href="/"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-6 w-6"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
            stroke-width="2"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z"
            />
          </svg>
          <span class="text-white group-hover:text-cyan-300">Calendar</span>
        </a>
      </nav>
    </div>
    <!-- Main content -->
    <div class="flex-1">
      <!-- header -->
      <div class="bg-white shadow px-2 py-4">
        <button @click="showSidebar =! showSidebar" class="text-cyan-600 font-extrabold">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-10 w-10"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
            stroke-width="2"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M4 6h16M4 12h8m-8 6h16"
            />
          </svg>
        </button>
      </div>
      <!-- content -->
      <div class="p-8 text-cyan-700 font-extrabold">Content</div>
    </div>
  </div>
</template>

<script>
import { ref } from "vue";
export default {
  setup() {
    const showSidebar = ref(false);

    return {
      showSidebar,
    };
  },
};
</script>
