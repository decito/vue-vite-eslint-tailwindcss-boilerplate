<script setup lang="ts">
import { useRouter } from 'vue-router'

const router = useRouter().getRoutes()
</script>

<template>
  <header
    class="max-h-screen leading-normal lg:flex lg:place-items-center lg:pr-section"
  >
    <img
      alt="Vue logo"
      class="mx-auto mb-8 block lg:mr-8"
      src="@/assets/logo.svg"
      width="125"
      height="125"
    />

    <div class="lg:flex lg:flex-wrap lg:place-items-start">
      <HelloWorld msg="You did it!" />

      <nav
        class="mt-8 w-full text-center text-xs lg:-ml-4 lg:mt-4 lg:py-4 lg:text-left lg:text-base"
      >
        <RouterLink
          v-for="route in router"
          :key="route.name"
          :to="route.path"
          class="inline-block border-l border-divider-light-2 px-4 capitalize dark:border-dark-2"
        >
          {{ route.name }}
        </RouterLink>
      </nav>
    </div>
  </header>

  <RouterView />
</template>
