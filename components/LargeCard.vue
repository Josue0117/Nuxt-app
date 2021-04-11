<template>
    <div class="card">
        <img :src="require('@/assets/images/'+img)" class="image">
        <h3 class="header">
            {{ tittle }}
        </h3>
        <p class="snippet">
            {{ snippet }}
        </p>
    </div>
</template>

<script>
    export default {
        props: ['tittle','snippet','img'],
    }
</script>

<style scoped>
    .card {
        width: 31.5%;
        height: 25rem;
        border: none;
        overflow: hidden;
        padding: 0;
        cursor: pointer;
    }
    .image {
        height: 65%;
        border-radius: 0.5rem;
    }
    .header {
        font-size: 1.15rem;
        margin-top: 0.4rem;
    }
    .snippet {
        color: grey
    }

</style>