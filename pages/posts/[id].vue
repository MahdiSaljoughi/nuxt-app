<template>
  <div>
    {{ route.params.id }}
  </div>
  <div
    class="md:w-[70%] dark:bg-zinc-700 bg-zinc-200 shadow-md mx-auto my-10 md:rounded-[32px] px-5 py-10 md:p-10 flex flex-col gap-y-5 items-center"
  >
    <div class="w-full bg-zinc-300 dark:bg-zinc-600 p-6 rounded-[24px]">
      <h1 class="bg-blue-500 inline-block rounded-full py-3 px-5 text-white">
        {{ post.id }}
      </h1>
      <img
        :src="post.attributes.imglink_post"
        class="w-80 rounded-[16px]"
        alt="img"
      />
      <span>{{ post.attributes.title_post }}</span>
      <p>{{ post.attributes.body_post }}</p>
      <div>
        <span>ایجاد شده</span>
        <span>{{ post.attributes.createdAt }}</span>
      </div>
      <div>
        <span>منتشر شده</span>
        <span>{{ post.attributes.publishedAt }}</span>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
const route = useRoute();
const { data: posts } = await useAsyncData(() =>
  $fetch(`http://localhost:1337/api/posts/${route.params.id}`)
);
const post = posts.value.data;
// const numbers = post;
// for (let i = 0; i < numbers.length; i++);
</script>
