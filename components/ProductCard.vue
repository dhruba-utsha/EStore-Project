<template>
  <div class="card">
    <NuxtLink :to="`/products/${product.id}`">
      <img :src="`${product.image}`" class="h-[180px] w-[180px] mx-auto text-center mb-[30px]" />
    </NuxtLink>
    <span class="bg-green-100 text-green-700 text-[12px] font-bold px-[20px] py-[10px] rounded-md mb-[30px]">Up to 35% off</span>
    <NuxtLink :to="`/products/${product.id}`">
      <p class="text-[20px] font-semibold text-gray-700 my-[30px] truncate hover:text-green-700">{{ product.title }}</p>
    </NuxtLink>

    <div class="flex items-center mb-[20px]">
      <span class="text-yellow-500 text-[20px] mr-[15px]">
        ★★★★☆
      </span>
      <span class="text-gray-500 text-[18px]">{{ product.rating.rate }} ({{ product.rating.count }})</span>
    </div>

    <div class="flex text-[16px] space-x-[30px] text-gray-500">
      <span class="bg-gray-100 py-[10px] px-[20px] rounded">Fast Delivery</span>
      <span class="bg-gray-100 py-[10px] px-[20px] rounded">Best Price</span>
    </div>

    <div class="flex justify-between items-center pb-[10px] mt-[20px]">
      <p class="text-[24px] font-bold text-green-700 ">${{ product.price }}</p>
      <button class=" bg-green-700 text-white rounded-md py-[10px] px-[20px] hover:bg-green-500">
        Add to Cart
      </button>
    </div>
  </div>
</template>

<script setup>
  const { product } = defineProps(['product'])
</script>

