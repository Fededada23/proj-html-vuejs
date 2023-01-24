<script lang="ts">
export default {
    
}
</script>
<template lang="">
    <div id="feature">    
            <p>FEATURED ARTICLE</p>
            <h3>Cras Malesuada Et Orci Eget Pharetra</h3>
            <p>In quis lectus sed leo elementum faucibus in dapibus dictum. Nullamolestie tortor nec lectus venenatis, sed blandit dui, dolor at bibendum sadips ets ipsums dolores ficilis uns leo lectus.</p>
            <button class="button-xlarge">READ MORE</button>
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
    .button-xlarge{
        @include button;
        background-color:black;
        color:white
    }
}
    
</style>