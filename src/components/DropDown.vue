<script>
import {store} from '../store.js';
import axios from 'axios';

export default{
    data() {
        return{
            store,
        }
    },
    methods: {
        SearchArchetype(){
                axios.get('https://db.ygoprodeck.com/api/v7/archetypes.php')
                .then((response) => {
                    this.store.archetypes = response.data;
                })
                .catch(function (error) {
                    // handle error
                    console.log(error);
                })
                .finally(function () {
                    // always executed
                });
        },

        changeSelected(type){
            store.selected = type;
            console.log(store.selected)
        }
    },
    created(){
        this.SearchArchetype();
    },
}
</script>

<template>
    <select name="archetype" id="archetype">
        <option v-for="(archetype) in store.archetypes" :value="archetype.archetype_name" @click="changeSelected(archetype.archetype_name); $emit('search')">
            {{ archetype.archetype_name }}
        </option>
    </select>
    


</template>

<style lang="scss" scoped>

</style>