<template>
  <div class="card">
    <div class="grid grid-cols-2 gap-10">
      <div class="p-7">
        <img :src="`${product.image}`" class="mx-auto max-w-[400px] my-7" />
      </div>
      <div class="p-7">
        <h2 class="text-[32px] font-bold my-[30px]">{{ product.title }}</h2>

        <div class="flex items-center mb-[20px] pr-[20px]">
          <p class="text-[26px] font-bold text-green-700 mr-[20px]">Price - ${{ product.price }}</p>
          <span class="text-yellow-500 text-[20px] mr-[15px]">
            ★★★★☆
          </span>
          <span class="text-gray-500 text-[18px]">({{ product.rating.rate }}) {{ product.rating.count }} ratings</span>
        </div>

        <div class="flex text-[18px] space-x-[30px] mb-[30px] cursor-pointer">
          <span class="border-[3px] border-gray py-[5px] px-[20px] rounded-md hover:bg-green-500">Add to Favorite</span>
          <span class="border-[3px] border-gray py-[5px] px-[30px] rounded-md hover:bg-green-500">Add to Cart</span>
        </div>
        
        <h3 class="font-bold text-[28px] border-b-2 mb-4 pb-2">Product description:</h3>
        <p class="text-[18px] text-gray-500 text-justify">{{ product.description }}</p>
      </div>
    </div>
  </div>
</template>

<script setup>
  const { product } = defineProps(['product'])
</script>
