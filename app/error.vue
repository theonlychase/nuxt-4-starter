<script setup lang="ts">
defineProps<{ error: NuxtError }>()

useHead({
  htmlAttrs: {
    lang: 'en'
  }
})

useSeoMeta({
  title: 'Page not found',
  description: 'We are sorry but this page could not be found.'
}, {
  mode: 'server'
})
</script>

<template>
  <UApp>
    <Header />

    <UMain>
      <UContainer>
        <UPage>
          <UError :error="error" />
        </UPage>
      </UContainer>
    </UMain>

    <Footer />
  </UApp>
</template>


