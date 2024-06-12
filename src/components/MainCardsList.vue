<script>
import MainSingleCard from './MainSingleCard.vue';
import { store } from '../store.js'
export default{
    data() {
        return{
            store,
        }
    },
    components:{
        MainSingleCard,
    }
}
</script>

<template>
    <div>
        <MainSingleCard v-for="card in store.cards" :key="card.id" :card="card" />
    </div>
</template>

<style scoped>
div{
    display: flex;
    flex-wrap: wrap;
    background-color: white;
    padding: 5rem;      
}
</style>