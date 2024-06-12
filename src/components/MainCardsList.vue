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
    <section>
        <div class="counter">
            <h2>Found {{ store.cards.length }} cards</h2>
        </div>
        <div class="cards">
            <MainSingleCard v-for="card in store.cards" :key="card.id" :card="card" />
        </div>
    </section>
</template>

<style scoped>
section{
    padding: 5rem;     
    background-color: white;

    div.counter{
        background-color: #212529;
        color: white;
        padding: 1rem;
        margin: 0 1rem;
    }
    
    div.cards{
        display: flex;
        flex-wrap: wrap;
    }
}
</style>