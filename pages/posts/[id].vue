<template>
  <MainHeader />
  <MobileHeader />
  <!-- <div>
    {{ route.params.id }}
  </div> -->
  <div
    class="w-full md:w-[70%] mx-auto dark:bg-zinc-700 bg-zinc-200 md:rounded-[32px] md:my-10 shadow-md"
  >
    <div class="flex flex-col items-center gap-x-5"> 
      <img
        :src="post.attributes.imglink_post"
        class="md:rounded-[32px]"
        alt="img"
      />
      <span class="font-[moraba] text-[17px] md:text-[20px] my-4 md:my-6">{{
        post.attributes.title_post
      }}</span>
    </div>
    <p class="text-[16px] md:text-[19px] mt-2 my-4 md:my-4 mx-4 md:mx-8 leading-loose text-wrap">{{ post.attributes.body_post }}</p>
    <div>
      <span class="text-[14px] md:text-[17px] m-2">ایجاد شده</span>
      <span class="text-[14px] md:text-[17px] m-2">{{ post.attributes.createdAt }}</span>
    </div>
    <div class="pb-4">
      <span class="text-[14px] md:text-[17px] m-2">منتشر شده</span>
      <span class="text-[14px] md:text-[17px] m-2">{{ post.attributes.publishedAt }}</span>
    </div>
  </div>
  <MainFooter />
</template>

<script setup lang="ts">
import MainFooter from "~/components/Footers/ManinFooter/MainFooter.vue";
import MainHeader from "~/components/Headers/MainHeader/MainHeader.vue";
import MobileHeader from "~/components/Headers/MobileHeader/MobileHeader.vue";
const route = useRoute();
const { data: posts } = await useAsyncData(() =>
  $fetch(`http://localhost:1337/api/posts/${route.params.id}`)
);
const post = posts.value.data;
// const numbers = post;
// for (let i = 0; i < numbers.length; i++);
</script>
