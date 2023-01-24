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
          <AppFeature :data="feature"/>
          <AppTitle :data="title"/>
          <cardsContainer :data="cards"/>
    </div>
</template>
<style lang="scss">
#news{
    display: flex;
    flex-direction: column;
    background-color: lightgray;
    color: white;
    padding: 150px;
}
    
</style>