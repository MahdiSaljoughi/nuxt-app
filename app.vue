<template>
  <Head>
    <Link rel="icon" href="favicon.ico" />
    <title>nuxtApp</title>
  </Head>
    <div class="cursor-default">
      <!-- <ContextProvider> -->
      <nuxtPage />
      <!-- </ContextProvider> -->
    </div>
</template>

<script setup>
import { registerLicense } from "@syncfusion/ej2-base";
// import ContextProvider from "./src/contexts/ContextProvider.vue";
registerLicense(
  "Ngo9BigBOggjHTQxAR8/V1NBaF5cXmZCeExyWmFZfVpgcl9FYFZUQ2YuP1ZhSXxXdkBjXH9Yc3RQTmVfU0w="
);
</script>
