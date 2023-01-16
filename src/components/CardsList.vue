<script>
import CharacterCard from './CharacterCard.vue';
import { store } from '../store.js'

export default {
    components:{
        CharacterCard
    },
    data(){
        return{
            store
        }
    }
}
</script>
<template lang="">
    <main class="container">
        <div class="row">
            <div class="col">
                <CharacterCard v-for="(item,index) in store.cardsList" ::key="index" :card="item" />
            </div>
        </div>
    </main>
</template>
<style lang="scss">
    @use '../styles/partials/variables' as *;

    main{
        background-color: $white-color;
        margin: 1rem;
    }
    .col{
        display: flex;
        flex-wrap: wrap;
    }
</style>