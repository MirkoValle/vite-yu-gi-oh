<script>
import MainCardsList from './MainCardsList.vue';
import Loader from './Loader.vue';
import DropDown from './DropDown.vue';
import axios from "axios";
import { store } from '../store.js'
export default{
    data() {
        return{
            store,
            isLoaded: false,
        }
    },
    components: {
        MainCardsList,
        Loader,
        DropDown,
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
        },
        showArchetype(){
            axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?archetype=' + store.selected)
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
        },
        delay(){
            setTimeout(() => {
                this.isLoaded = true;
            }, 3000);
        }
    },
    created(){
        this.getCards();
        this.delay();
    }
}
</script>

<template>
    <main>
        <DropDown @search="showArchetype"/>
        <MainCardsList v-if="isLoaded == true"/>
        <Loader v-else />
    </main>
</template>

<style scoped>

main{
    background-color: #d48f38;
    padding: 2.5rem 5rem 5rem 5rem;
    min-height: 100vh; 
}
</style>