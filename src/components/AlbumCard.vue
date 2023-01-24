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
        <h2>{{ singleCard.title }}</h2>
        <p>{{ singleCard.text }}</p>
    </div>
</template>
<style lang="scss">

</style>