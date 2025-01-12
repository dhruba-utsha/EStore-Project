<template>
    <div>
      <header class="shadow-sm bg-white">
        <nav class="container mx-auto p-4 flex justify-between items-center">
          <NuxtLink to="/" class="font-bold text-[32px] flex items-center"> <img src="assets\images\nuxt-icon.svg" alt="icon" class= "h-[60px] w-[60px]">EStore</NuxtLink>

          <ul class="flex gap-4 text-gray-600 text-[22px]">
            <li><NuxtLink to="/" > Home</NuxtLink></li>
            <!-- <li><NuxtLink to="/products" class="text-[25px]">Products</NuxtLink></li> -->
            <li><NuxtLink to="/" >Favorite-Products</NuxtLink></li>
            <li><NuxtLink to="/" >Cart</NuxtLink></li>
          </ul>
        </nav>
      </header>
      <div class="container mx-auto p-4">
        <slot />
      </div>
    </div>
</template>
  
<!-- <style scoped>
    .router-link-exact-active {
      color: #12b488;
    }
</style> -->