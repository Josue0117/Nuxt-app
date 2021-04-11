<template>
    <div class="container">
        <h4 class="header">
            {{ tittle }}
        </h4>
        <p class="snippet">
            {{ snippet }}
        </p>
        <div class="cards-container">
            la
        </div>
    </div>
</template>

<script>
    export default {
        props: [ 'tittle' , 'snippet' ],
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