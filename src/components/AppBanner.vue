<script lang="ts">
export default {
    props: {
        data: Object
    }
    
}
</script>
<template lang="">
    <div id="banner">    
            <p>{{data.title}}</p>
            <p>{{data.preTitle}}</p>
    </div>
</template>
<style lang="scss">
#banner{
    display: flex;
    flex-direction: column;
    background-color: lightgray;
    color: #3b3d3f;
    padding: 150px;
    align-items: center;
}
    
</style>