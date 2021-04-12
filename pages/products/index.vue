<template>
    <div>
        <Nav />
        <div class="container">
            <large-card-display
            v-for="largeInfo in largeCardInfo"
            :key="largeInfo.id"
            :tittle="largeInfo.title"
            :snippet="largeInfo.snippet"
            :cards="largeInfo.cards"
        />
        <small-card-display
            v-for="smallInfo in smallCardInfo"
            :key="smallInfo.id"
            :tittle="smallInfo.title"
            :cards="smallInfo.cards"
        />
        </div>
    </div>
</template>

<script>
import { largeCardSections , smallCardSections } from '@/assets/data.js'
import LargeCardDisplay from '../../components/LargeCardDisplay.vue'
import SmallCardDisplay from '../../components/SmallCardDisplay.vue'
export default {
    components: { LargeCardDisplay, SmallCardDisplay },
    data() {
        return {
            largeCardInfo: largeCardSections,
            smallCardInfo: smallCardSections,
        }
    }
}
</script>

<style scoped>

</style>