<script>

import { store } from '../store.js'

export default {
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
                Character card
            </div>
        </div>
    </main>
</template>
<style lang="scss">
    @use '../styles/partials/variables' as *;

    main{
        background-color: $white-color;
        margin: 3rem;
    }
</style>