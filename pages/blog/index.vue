<template>
  <div>
    <!-- {{ data }} -->
    <p>This is Enginere Life</p>
    <div v-for="singleData in data" :key="singleData.id">
      <div>
        <h3>{{ singleData.title }}</h3>
        <p>{{ singleData.excerpt }}</p>
        <p>{{ singleData.date }}</p>
        <NuxtLink :to="singleData._path">Read More</NuxtLink>
      </div>
      <div>
        <nuxt-img :src="singleData.image" alt="blog-image" format="webp" />
      </div>
    </div>
  </div>
</template>

<script setup>
const { data } = await useAsyncData("blogQuery", () =>
  queryContent("/blog").find({ id: -1 })
);
console.log("data");
console.log(data.value);
</script>
<style>
h1 {
  color: red;
}
.text {
  color: green;
  letter-spacing: 20px;
}
</style>
