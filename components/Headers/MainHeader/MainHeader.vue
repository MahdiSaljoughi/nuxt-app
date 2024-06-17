<template>
  <header
    class="hidden md:block sticky top-0 w-full bg-zinc-100 dark:bg-zinc-800 shadow-md"
  >
    <div class="flex items-center justify-between mx-5 py-4">
      <div class="flex items-center gap-x-4">
        <div @click="openSaidbar" class="cursor-pointer">
          <span>
            <svg
              class="w-6 h-6"
              aria-hidden="true"
              xmlns="http://www.w3.org/2000/svg"
              width="24"
              height="24"
              fill="none"
              viewBox="0 0 24 24"
            >
              <path
                stroke="currentColor"
                stroke-linecap="round"
                stroke-width="2"
                d="M5 7h14M5 12h14M5 17h14"
              />
            </svg>
          </span>
        </div>
        <div>
          <nuxt-link to="/">
            <img src="/public/img/favicon.ico" alt="Logo" width="37px" />
          </nuxt-link>
        </div>
        <div class="flex items-center gap-x-4">
          <div>
            <nuxt-link to="/" class="flex items-center gap-x-2">
              <span>
                <svg
                  class="w-6 h-6"
                  aria-hidden="true"
                  xmlns="http://www.w3.org/2000/svg"
                  width="24"
                  height="24"
                  fill="none"
                  viewBox="0 0 24 24"
                >
                  <path
                    stroke="currentColor"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="m4 12 8-8 8 8M6 10.5V19a1 1 0 0 0 1 1h3v-3a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1v3h3a1 1 0 0 0 1-1v-8.5"
                  />
                </svg>
              </span>
              <span>صفحه اصلی</span>
            </nuxt-link>
          </div>
          <div>
            <nuxt-link to="/posts" class="flex items-center gap-x-2">
              <span>
                <svg
                  class="w-6 h-6"
                  aria-hidden="true"
                  xmlns="http://www.w3.org/2000/svg"
                  width="24"
                  height="24"
                  fill="none"
                  viewBox="0 0 24 24"
                >
                  <path
                    stroke="currentColor"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M19 7h1v12a1 1 0 0 1-1 1h-2a1 1 0 0 1-1-1V5a1 1 0 0 0-1-1H5a1 1 0 0 0-1 1v14a1 1 0 0 0 1 1h11.5M7 14h6m-6 3h6m0-10h.5m-.5 3h.5M7 7h3v3H7V7Z"
                  />
                </svg>
              </span>
              <span>پست ها</span>
            </nuxt-link>
          </div>
        </div>
      </div>
      <!-- search -->
      <!-- <div>
                <div>
                    <input type="text" placeholder="search">
                </div>
            </div> -->
      <div class="flex items-center gap-x-4">
        <div>
          <nuxt-link to="/cart" class="flex items-center gap-x-2">
            <span>
              <svg
                class="w-6 h-6"
                aria-hidden="true"
                xmlns="http://www.w3.org/2000/svg"
                width="24"
                height="24"
                fill="none"
                viewBox="0 0 24 24"
              >
                <path
                  stroke="currentColor"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M5 4h1.5L9 16m0 0h8m-8 0a2 2 0 1 0 0 4 2 2 0 0 0 0-4Zm8 0a2 2 0 1 0 0 4 2 2 0 0 0 0-4Zm-8.5-3h9.25L19 7H7.312"
                />
              </svg>
            </span>
            <span>سبدخرید</span>
          </nuxt-link>
        </div>
        <div>
          <nuxt-link to="/auth" class="flex items-center gap-x-2">
            <span>
              <svg
                class="w-6 h-6"
                aria-hidden="true"
                xmlns="http://www.w3.org/2000/svg"
                width="24"
                height="24"
                fill="none"
                viewBox="0 0 24 24"
              >
                <path
                  stroke="currentColor"
                  stroke-width="2"
                  d="M7 17v1a1 1 0 0 0 1 1h8a1 1 0 0 0 1-1v-1a3 3 0 0 0-3-3h-4a3 3 0 0 0-3 3Zm8-9a3 3 0 1 1-6 0 3 3 0 0 1 6 0Z"
                />
              </svg>
            </span>
            <span>ورود | ثبت نام</span>
          </nuxt-link>
        </div>
      </div>
    </div>
  </header>
  <MainSaidbar />
</template>

<script setup>
import MainSaidbar from "~/components/MainSaidbar/MainSaidbar.vue";

function openSaidbar() {
  const saidebar = document.getElementById("saidebar");
  saidebar.classList.toggle("hidden");
}
</script>
