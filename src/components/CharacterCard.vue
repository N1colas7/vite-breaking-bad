<script>
export default {
    props:{
        card:Object
    },
    data(){
        return{
            index: 0
        }
    }
}
</script>
<template lang="">
    <div class="cards-card">
        <div class="card-image">
            <img :src="card.card_images[0].image_url" alt="img">
        </div>
        <div class="card-info">
            <h4>{{ card.name }}</h4>
            <p>{{ card.type }}</p>
        </div>
    </div>
</template>
<style lang="scss">
    @use '../styles/partials/variables' as *;

    img{
        width: 250px;
    }
    .cards-card{
        background-color: $primary-color;
        margin: 5px;
    }
    .card-info{
        text-align: center;
        color: $white-color;
    }
</style>