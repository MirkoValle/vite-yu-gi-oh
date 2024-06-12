<script>
import MainCardsList from './MainCardsList.vue';
import axios from "axios";
import { store } from '../store.js'
export default{
    data() {
        return{
            store,
        }
    },
    components: {
        MainCardsList,
    },
    methods: {
        getCards(){
            axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
                .then( (response) => {
                    // handle success
                    this.store.cards = response.data.data;
                })
                .catch(function (error) {
                    // handle error
                    console.log(error);
                })
                .finally(function () {
                    // always executed
                });
        }
    },
    created(){
        this.getCards();
    }
}
</script>

<template>
    <main>
        <MainCardsList/>
    </main>
</template>

<style scoped>

main{
    background-color: #d48f38;
    padding: 5rem;
}
</style>