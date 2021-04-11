<template>
    <div class="container">
        <h3 class="header">
            {{ tittle }}
        </h3>
        <div class="card-container">
            <small-card
                v-for="imageInfo in cards"
                :key="imageInfo.id"
                :img="imageInfo.image"
            />
        </div>
    </div>
</template>

<script>
import SmallCard from './SmallCard.vue'
    export default {
  components: { SmallCard },
        props: ['tittle','cards'],
    }
</script>

<style scoped>
    .container {
        padding: 2rem 0
    }

    .header {
        font-weight: 700;
        font-size: 1.5rem;
        margin-bottom: 2rem;
    }

    .card-container {
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
    }
</style>