<script lang="ts">

  let menu;

  const burgerHandle = () => {
    if (menu.classList.contains('hidden')){
      menu.classList.remove('hidden');
    } else {
      menu.classList.add('hidden');
    }
  }
</script>

<div class="grid md:grid-cols-3">
  <div class="md:col-span-1 md:flex md:justify-end">
    <nav class="text-right">
      <div class="flex justify-between items-center">
        <h1 class="font-bold uppercase p-4 border-b border-gray-100">
          <a href="/" class="hover:text-gray-700">Food</a>
        </h1>
        <div class="px-4 cursor-pointer md:hidden" on:click={burgerHandle}>
          <svg xmlns="http://www.w3.org/2000/svg" class="w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
            <path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16M4 18h16" />
          </svg>
        </div>
      </div>
      <ul class="text-sm mt-6 hidden md:block" bind:this="{menu}">
        <li class="text-gray-700 font-bold py-1">
          <a href="#" class="px-4 flex justify-end border-r-4 border-rose-500">
            <span>Home</span>
            <svg xmlns="http://www.w3.org/2000/svg" class="w-5 ml-2" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
              <path stroke-linecap="round" stroke-linejoin="round" d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6" />
            </svg>
          </a>
        </li>
        <li class="py-1">
          <a href="#" class="px-4 flex justify-end border-r-4 border-white">
            <span>About</span>
            <svg xmlns="http://www.w3.org/2000/svg" class="w-5 ml-2" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
              <path stroke-linecap="round" stroke-linejoin="round" d="M8.228 9c.549-1.165 2.03-2 3.772-2 2.21 0 4 1.343 4 3 0 1.4-1.278 2.575-3.006 2.907-.542.104-.994.54-.994 1.093m0 3h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z" />
            </svg>
          </a>
        </li>
        <li class="py-1">
          <a href="#" class="px-4 flex justify-end border-r-4 border-white">
            <span>Contect</span>
            <svg xmlns="http://www.w3.org/2000/svg" class="w-5 ml-2" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
              <path stroke-linecap="round" stroke-linejoin="round" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
            </svg>
          </a>
        </li>
      </ul>
    </nav>
  </div>

  <main class="px-16 py-6 bg-gray-100 md:col-span-2">
    <div class="flex justify-center md:justify-end">
      <a href="#" class="text-rose-500 btn border-rose-500 md:border-2 hover:bg-rose-500 hover:text-white transition ease-out duration-500">Log in</a>
      <a href="#" class="text-rose-500 ml-2 btn border-rose-500 md:border-2 hover:bg-rose-500 hover:text-white transition ease-out duration-500">Sign up</a>
    </div>

    <header>
      <h2 class="text-gray-700 text-6xl font-semibold">Recipes</h2>
      <h2 class="text-2xl font-semibold">For Ninjas</h2>
    </header>

    <div>
      <h4 class="font-bold mt-12 pb-2 border-b border-gray-200">Latest Recipes</h4>

      <div class="mt-8 lg:grid grid-cols-3 gap-10">
        <!-- cards go here -->
        <div class="card hover:drop-shadow-lg">
          <img src="/img/stew.jpg" alt="stew" class="w-full h-32 sm:h-48 object-cover">
          <div class="m-4">
            <span class="font-bold">5 Bean Chilli Stew</span>
            <span class="block">Recipe by Mario</span>
          </div>
          <div class="badge">
            <svg xmlns="http://www.w3.org/2000/svg" class="w-5 inline-block" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
              <path stroke-linecap="round" stroke-linejoin="round" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
            </svg>
            <span>25 mins</span>
          </div>
        </div>
        <div class="card hover:drop-shadow-lg">
          <img src="/img/noodles.jpg" alt="noodles" class="w-full h-32 sm:h-48 object-cover">
          <div class="m-4">
            <span class="font-bold">Veg Noodles</span>
            <span class="block">Recipe by Mario</span>
          </div>
          <div class="badge">
            <svg xmlns="http://www.w3.org/2000/svg" class="w-5 inline-block" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
              <path stroke-linecap="round" stroke-linejoin="round" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
            </svg>
            <span>25 mins</span>
          </div>
        </div>
        <div class="card hover:drop-shadow-lg">
          <img src="/img/curry.jpg" alt="curry" class="w-full h-32 sm:h-48 object-cover">
          <div class="m-4">
            <span class="font-bold">Tofu Curry</span>
            <span class="block">Recipe by Mario</span>
          </div>
          <div class="badge">
            <svg xmlns="http://www.w3.org/2000/svg" class="w-5 inline-block" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
              <path stroke-linecap="round" stroke-linejoin="round" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
            </svg>
            <span>25 mins</span>
          </div>
        </div>
      </div>

      <h4 class="font-bold mt-12 pb-2 border-b border-gray-200">Most Popular</h4>
      <div class="mt-8">
        <!-- card go here -->
      </div>

      <div class="flex justify-center">
        <div class="btn bg-amber-200 text-gray-500 hover:shadow-inner transform hover:scale-125 hover:bg-opacity-50 transition ease-out duration-300">Load more</div>
      </div>
    </div>
  </main>
</div>
<style>
    .card{
        @apply bg-white rounded overflow-hidden shadow-md relative;
    }

    .badge{
        @apply bg-amber-200 text-gray-500 text-xs uppercase font-bold rounded-full p-2 absolute top-0 ml-2 mt-2;
    }

    .btn {
        @apply rounded-full py-2 px-3 uppercase text-xs font-bold cursor-pointer tracking-wider;
    }
</style>