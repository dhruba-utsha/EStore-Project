<template>
  <div>
    <div class="grid grid-cols-3 gap-5">
      <div v-for="item in products">
        <ProductCard :product="item" />
      </div>
    </div>
  </div>
</template>


<script setup>
  const { data: products } = await useFetch('https://fakestoreapi.com/products')
</script>


