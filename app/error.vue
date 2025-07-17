<script setup lang="ts">
import type { NuxtError } from '#app'

defineProps<{ error: NuxtError }>()

useSeoMeta({
  title: 'Page not found',
  description: 'We are sorry but this page could not be found.',
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
