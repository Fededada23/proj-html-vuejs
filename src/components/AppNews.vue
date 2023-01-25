<script lang="ts">
import AppFeature from './AppFeature.vue';
import AppTitle from '../components/AppTitle.vue';
import cardsContainer from './cardsContainer.vue';
export default {
    props: {
        feature: Object,
        title: Object,
        cards:Array
    },
    components:{
        AppFeature,
        AppTitle,
        cardsContainer
    }
    
}
</script>
<template lang="">
    <div id="news">   
        <div class="left-components">
            <AppFeature :data="feature"/>
        </div>   
        <div class="right-components"> 
            <AppTitle :data="title"/>
            <div class="d-flex flex-column"><cardsContainer :data="cards"/></div>
            
        </div>    
    </div>
</template>
<style lang="scss">
#news{
    display: flex;
    justify-content: center;
    background-color: lightgray;
    color: white;
    padding: 150px;
    .left-components{
        width: 70%;
    }
    .right-components{
        width: 30%;
        
    }
}
    
</style>