<script>
  import AppHeader from './components/AppHeader.vue';
  import AppMain from './components/AppMain.vue';

  import { store } from './store.js';
  import axios from 'axios';
  
  export default {
    components:{
        AppHeader,
        AppMain,
    },
    data(){
      return{
        store
      }
    },
    created(){
      this.getCardsList();
    },
    methods:{
      getCardList(){
        axios.get(store.url).then((response) => {
          store.cardsList = response.data.data;
        });
      }
    }
  }
</script>

<template>

 <AppHeader />
 <AppMain />

</template>

<style lang="scss">
@use './styles/generals.scss';

</style>
