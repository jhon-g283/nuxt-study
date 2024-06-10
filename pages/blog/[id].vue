<template>
  <div>
    <div>
      <nuxt-img :src="data.image" alt="blog-image" format="webp"></nuxt-img>
    </div>
    <div>
      <div>
        <h1>{{ data.title }}</h1>
        <p>{{ data.date }}</p>
        <ContentDoc />
      </div>
    </div>
  </div>
</template>

<script setup>
// useAsyncDataで非同期取得
const { data } = await useAsyncData(useRoute().path, () =>
  // ルートオブジェクト取得、一番最初のコンテンツを取得
  queryContent(useRoute().path).findOne()
);

console.log("data");
console.log(useRoute().path);
</script>
