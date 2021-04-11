<template>
  <div>
    <Hero/>
    <large-card-display
      v-for="info in largeCardInfo"
      :key="info.id"
      :tittle="info.title"
      :snippet="info.snippet"
      :cards="info.cards"
    />
  </div>
</template>

<script>
import LargeCardDisplay from '../components/LargeCardDisplay.vue'
import { largeCardSections } from '@/assets/data.js'
export default {
  components: { LargeCardDisplay },
  data() {
    return {
      largeCardInfo: largeCardSections,
    }
  }
}
</script>

<style>
</style>