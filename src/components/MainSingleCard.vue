<script>
export default{
    data() {
        return{
            
        }
    },
    props:{
        card: {
            type: Object,
            required: true
        }
    }
}
</script>

<template>
    <article>
        <img :src="card.card_images[0].image_url" alt="">
        <div class="info">
        <h3>{{ card.name }}</h3>
        <p>{{ card.archetype }}</p>
        </div>
    </article>
</template>

<style scoped>
 article{
        width: calc((100% / 5));
        padding: 1rem;
        display: flex;
        flex-direction: column;
        
        img{
            width: 100%;
            object-fit: cover;
        }

        div.info{
            padding: 0;
            background-color: #d48f38;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: space-between;
            height: 100%;
        }

        h3{
            padding-top: 1rem;
            text-align: center;
            color: white;
            text-transform: uppercase;
        }

        p{
            padding-top: 1rem;
            font-size: 1.5rem;
        }
            
}       
</style>