<script lang="ts">
export default {
    props: {
        data: Object
    }
}
</script>
<template lang="">
    <div id="title">    
            <p v-if="data.preTitle">{{data.preTitle}}</p>
            <h2>{{data.title}}</h2>
    </div>
</template>
<style lang="scss">
#title{
    display: flex;
    flex-direction: column;
    background-color: white;
    color: black;
    align-items: center;
    padding-top:100px
}
    
</style>