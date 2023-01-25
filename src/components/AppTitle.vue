<script lang="ts">
export default {
    props: {
        data: Object,
        small: Boolean
    }
}
</script>
<template lang="">
    <div id="title" :class="{ small: small }">   
            <p v-if="data.preTitle">{{data.preTitle}}</p>
            <h2>{{data.title}}</h2>
            <div class="fusion-separator">
                <div class="fusion-separator-border "></div>
            </div>
    </div>
</template>
<style lang="scss">
#title{
    display: flex;
    flex-direction: column;
    background-color: white;
    color: black;
    align-items: center;
    padding-top:100px;
    .fusion-separator{
        align-self: center;
        margin-left: auto;
        margin-right: auto;
        margin-top: 15px;
        margin-bottom: 70px;
        width: 100%;
        max-width: 90px;
        display: flex;
        align-items: center;
        clear: both;
        
        .fusion-separator-border{
            flex-grow: 2;
            border-bottom-style: solid;
            border-top-style: solid;
            border-top-width: 2px;
            border-color: orange
        }

    }
    &.small{
        padding-top: 0;
        align-items: baseline;
        .fusion-separator{
            align-self: flex-start;
            margin-right: auto;
            margin-bottom: 43px;
            width: 100%;
            max-width: 90px;
            margin-left: 0;
        }
    }
}
    
</style>