<script>
import MainSingleCard from './MainSingleCard.vue';
export default{
    data() {
        return{
            
        }
    },
    props:{
        cards: {
            type: Array,
            required: true
        }
    },
    components:{
        MainSingleCard,
    }
}
</script>

<template>
    <div>
        <MainSingleCard v-for="card in cards" :key="card.id" :card="card" />
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