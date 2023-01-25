<script lang="ts">
export default {
    props: {
        data: Object
    }
    
}
</script>
<template lang="">
    <div id="feature">    
            <p>{{data.preTitle}}</p>
            <h3>{{data.title}}</h3>
            <p>{{data.description}}</p>
            <button class="button-xlarge">{{data.button}}</button>
    </div>
</template>
<style lang="scss">
@use '../styles/partials/mixins' as *;
#feature{
    background-image:url("/images/featured_article_1_bg.jpg") ;
    display: flex;
    flex-direction: column;
    color: white;
    padding: 150px;
    background-size: cover;
    .button-xlarge{
        @include button;
        background-color:black;
        color:white
    }
}
    
</style>