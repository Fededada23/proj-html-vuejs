<script lang="ts">
export default {
    props: {
        data: Object
    }
    
}
</script>
<template lang="">
    <div id="jumbotron">    
            <h1>TECH FORUM</h1>
            <p>Discuss all the latest technology news and trends</p>
            <button class="button-xlarge">START WITH AVADA</button>
    </div>
</template>
<style lang="scss">
@use '../styles/partials/mixins' as *;
.button-xlarge{
        @include button
    }
    
</style>