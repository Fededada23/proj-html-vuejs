<script>
import AlbumCard from '../components/AlbumCard.vue';
export default {
    components: {
        AlbumCard
    },
    data: function(){
        return {
            albumCards: [
                {
                    thumb: "/images/post_feat_img_25-320x202.jpg",
                    title: "Morbi vitae dui euismod vulputate sollicitudin",
                    text: "Donec finibus sit amet orci eget ultricies. Praesent posuere ante ut erat fringilla, vestibulum placerat metus mattis. Aenean dictum vitae nisl"
                },
                {
                    thumb: "/images/post_feat_img_24-320x202.jpg",
                    title: "Vivamus pellenteque, felis quis varius",
                    text: "Donec finibus sit amet orci eget ultricies. Praesent posuere ante ut erat fringilla, vestibulum placerat metus mattis. Aenean dictum vitae nisl"
                },
                {
                    thumb: "/images/post_feat_img_23-320x202.jpg",
                    title: "Donec ornare pretium eget scelisque justo",
                    text: "Donec finibus sit amet orci eget ultricies. Praesent posuere ante ut erat fringilla, vestibulum placerat metus mattis. Aenean dictum vitae nisl"
                },
            ]
        }
    }
    
}
</script>
<template lang="">
    <div id="album">
            <AlbumCard v-for="(element, index) in albumCards" :key="index" :singleCard="element"/>
    </div>
</template>
<style lang="scss">
#album{
    background-color: white;
    color: black;
    display: flex;
    justify-content: space-between;
    align-content: center;
}
    
</style>