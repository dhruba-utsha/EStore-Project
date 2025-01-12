<template>
    <div class="flex justify-between items-center py-[30px]">
        <div>
            <h1 class="text-[50px] font-bold"><span class="text-green-700">Estore</span><br> Discover Your Next Favorite Find! </h1>
            <p class="text-gray-400 text-[26px]">Explore a world of unique products, handpicked just for you.</p>
        </div>
        <div>
            <img src="assets\images\banner-2.jpg" alt="banner" width="1000px">
        </div>
    </div>

    <div class="grid grid-cols-3 gap-5 mt-[30px]">
      <div v-for="item in products">
        <ProductCard :product="item" />
      </div>
    </div>
</template>

<script setup>
  const { data: products } = await useFetch('https://fakestoreapi.com/products')
</script>

