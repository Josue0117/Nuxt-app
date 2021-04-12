<template>
    <div class="container">
        <h4 class="header">
            {{ tittle }}
        </h4>
        <p class="snippet">
            {{ snippet }}
        </p>
        <div class="cards-container">
            <large-card
                v-for="cardInfo in cards"
                :key="cardInfo.id"
                :id="cardInfo.id"
                :tittle="cardInfo.title"
                :snippet="cardInfo.snippet"
                :img="cardInfo.image"
            />
        </div>
    </div>
</template>

<script>
import LargeCard from './LargeCard.vue'
    export default {
  components: { LargeCard },
        props: ['tittle' , 'snippet' , 'cards'],
    }
</script>

<style scoped>
    .container {
        margin-top: 2rem;
    }
    .header {
        font-weight: 700;
        font-size: 1.5rem;
    }
    .snippet {
        color: grey;
        margin-bottom: 1.5rem;
    }
    .cards-container {
        display: flex;
        justify-content: space-between;
    }
</style>