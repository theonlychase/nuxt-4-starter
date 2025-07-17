<script setup lang="ts">
useHead({
  htmlAttrs: { lang: 'en' },
  meta: [
    { charset: 'utf-8' },
    {
      name: 'viewport',
      content: 'width=device-width, initial-scale=1',
    },
  ],
  link: [
    {
      rel: 'icon',
      href: '/favicon.ico',
    },
  ],
})

useSeoMeta(
  {
    title: () => '%title',
    description: () => '%description',
    ogDescription: () => '%description',
    ogTitle: () => '%title',
    twitterTitle: () => '%title',
    twitterDescription: () => '%title',
  },
  { mode: 'server' },
)
</script>

<template>
  <UApp :toaster="{ position: 'top-right' }">
    <NuxtLoadingIndicator />

    <NuxtLayout>
      <NuxtPage />
    </NuxtLayout>
  </UApp>
</template>
