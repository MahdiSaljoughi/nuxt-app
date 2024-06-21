<template>
  <MainHeader />
  <MobileHeader />
  <div
    class="md:w-[70%] dark:bg-zinc-700 bg-zinc-200 shadow-md mx-auto md:my-20 md:rounded-[32px] px-5 py-10 md:p-10 flex flex-col gap-y-5 items-center justify-center"
  >
    <div class="grid grid-cols-1 md:grid-cols-2 xl:grid-cols-3 gap-8">
      <nuxt-link
        :to="`/posts/${postdata.id}`"
        v-for="postdata in numbers"
        :key="postdata.id"
        class="w-full bg-zinc-300 dark:bg-zinc-600 rounded-[24px] text-center pb-6 shadow-md"
      >
        <img
          :src="postdata.attributes.imglink_post"
          class="w-[400px] rounded-[16px] mb-4"
          alt="img"
        />
        <span class="text-[18px] font-[moraba]">{{ postdata.attributes.title_post }}</span>
      </nuxt-link>
    </div>
  </div>
  <MainFooter />
</template>

<script setup lang="ts">
import MainFooter from "~/components/Footers/ManinFooter/MainFooter.vue";
import MainHeader from "~/components/Headers/MainHeader/MainHeader.vue";
import MobileHeader from "~/components/Headers/MobileHeader/MobileHeader.vue";
// const { find, findOne, create, update, delete: remove } = useStrapi()

const { data: posts } = await useAsyncData(() =>
  $fetch("http://localhost:1337/api/posts")
);

const post = posts.value.data;
const numbers = post;
for (let i = 0; i < numbers.length; i++);
// console.log(numbers[i].attributes.title_post);
</script>
