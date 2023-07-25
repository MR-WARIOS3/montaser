<template>
    <div>
      <div>
        <nav class="container px-6 py-5 mx-auto md:flex md:justify-between md:items-center border-b-2 border-cyan-500">
          <div class="flex items-center justify-between">
            <router-link to="/" class="   text-3xl font-bold text-gray-100 md:text-3xl ">Montaser</router-link>
            <div @click="showMenu = !showMenu" class="flex md:hidden">
              <button type="button" class="text-gray-800  hover:text-gray-400 focus:outline-none focus:text-gray-400 ">
                <svg viewBox="0 0 24 24" class="w-6 h-6 fill-current">
                  <path fill-rule="evenodd" d="M4 5h16a1 1 0 0 1 0 2H4a1 1 0 1 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2z"></path>
                </svg>
              </button>
            </div>
          </div>
          <ul :class="showMenu ? 'flex' : 'hidden'" class=" flex-col mt-8 space-y-4 md:flex  md:space-y-0 md:flex-row md:items-center  md:space-x-10  md:mt-0 ">
            <li class="text-md    text-cyan-600 font-semibold hover:underline hover:underline-offset-4"> Home</li>
            <li class="text-md  font-semibold   hover:underline hover:underline-offset-4">About</li>
            <li class="text-md   font-semibold hover:underline hover:underline-offset-4"> Services</li>
            <li class="text-md  font-semibold hover:underline hover:underline-offset-4 "> Projects</li>
          </ul>
        </nav>
      </div>
    </div>
  </template>
  <script >
  export default {
    data() {
      return {
        showMenu: false,
      };
    },
  };
  </script>
  <style>
      @media  screen and (max-width: 768px) {
          ul{
            margin: 0.3em;
            top: 2.9em;
            border-radius: 10px;
             align-items: center;
             position: absolute;
             left: 0;
             right: 0;
             margin-inline: 2rem;
             background: rgb(43, 43, 43);
          }
      }
 
 </style>