<script lang="ts">
import AppFeature from './AppFeature.vue';
import AppTitle from '../components/AppTitle.vue';
import cardsContainer from './cardsContainer.vue';
export default {
    props: {
        feature: Object,
        title: Object,
        cards:Array,
    
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
            <AppTitle :data="title" :small="true"/>
            <cardsContainer :data="cards" :vertical="true"/>
        </div>    
    </div>
</template>
<style lang="scss">
#news{
    display: flex;
    justify-content: center;
   
    color: white;
    
    .left-components{
        width: 70%;
       
    }
    .right-components{
        width: 30%;
        
        
    }
}
    
</style>