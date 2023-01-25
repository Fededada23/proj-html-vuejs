<script lang="ts">
export default {
    props: {
        data: Object
    }
    
}
</script>
<template lang="">
    <div id="jumbotron">    
            <h1>{{data.title}}</h1>
            <p>{{data.preTitle}}</p>
            <button class="button-xlarge">START WITH AVADA</button>
    </div>
</template>
<style lang="scss">
@use '../styles/partials/mixins' as *;
#jumbotron{
    padding: 140px 20px;
    h1{
        font-size: 110px
    }

    .button-xlarge{
            @include button;
            margin-top:50px;
            background-color:#27aabe;
            color:white
        }
}
    
</style>