<script>
import AlbumCard from '../components/AlbumCard.vue';
export default {
    name: 'cardsContainer',
    components: {
        AlbumCard
    },
    props: {
        data: Array,
        vertical: Boolean
    }
}

</script>
<template lang="">
    <div id="album-cards" :class="{ vertical: vertical }">
        <AlbumCard v-for="(element, index) in data" :singleCard="element"/>
    </div>
</template>
<style lang="scss">
@use '../styles/partials/mixins' as *;
#album-cards{
    color: black;
    display: flex;
    justify-content: space-between;
    align-content: center;
    
    
    &.vertical{
        padding:0;
        flex-direction: column;
        min-height: 1px;
        padding-left: 15px;
        padding-right: 15px;
        margin-bottom: 20px;
        .album-image{
            overflow: hidden;
            float: left;
            margin: 0 20px 5px 0;
            width: 144px;
            img{
                opacity: 1;
                transition: opacity 1s,transform 1s;
                width: 100%;
                max-width: 100%;
                display: block;
                -webkit-user-select: none;
                user-select: none;
                box-shadow: none;
                border-radius: 0;
                margin-bottom: 20px;
            }
        }
        h2{
            margin: 15px 0 3px;
            clear: none;
            font-size: 18px;
            
        }
        p{
            overflow: hidden;
            margin-bottom: 13px;
            padding: 0;
            color: #333;
            font-size: 13px;
        }
    }
}
    
</style>