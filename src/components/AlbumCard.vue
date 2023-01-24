<script>
export default {
    name: 'albumCard',
    props: {
        singleCard: Object
    }
}
</script>
<template>
    <div class="album-card">
        <div class="album-image">
            <img :src="singleCard.thumb" :alt="singleCard.series">
        </div>
        <h4>{{singleCard.series}}</h4>
    </div>
</template>
<style lang="scss">

</style>