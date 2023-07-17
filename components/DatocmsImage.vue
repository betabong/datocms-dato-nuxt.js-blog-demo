<script setup lang="ts">
import { Image, ResponsiveImageType } from 'vue-datocms'

const props = defineProps<{
  data: ResponsiveImageType
}>()
</script>

<template>
  <Image :data="props.data" />
</template>
