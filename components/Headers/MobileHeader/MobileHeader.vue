<template>
  <header
    class="block md:hidden sticky top-0 w-full bg-zinc-100 dark:bg-zinc-800 shadow-md"
  >
    <div class="flex items-center justify-between mx-5 py-4">
      <div class="flex items-center gap-x-4">
        <div @click="openSaidbarM">
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
            <img src="/public/img/favicon.ico" alt="Logo" width="30px" />
          </nuxt-link>
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
          <nuxt-link to="/cart">
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
          </nuxt-link>
        </div>
        <div>
          <nuxt-link to="/auth">
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
          </nuxt-link>
        </div>
      </div>
    </div>
  </header>
  <MobileSaidbar />
</template>

<script setup>
import MobileSaidbar from "~/components/MainSaidbar/MobileSaidbar.vue";

function openSaidbarM() {
  const saidebarM = document.getElementById("saidebarM");
  saidebarM.classList.toggle("hidden");
}
</script>
