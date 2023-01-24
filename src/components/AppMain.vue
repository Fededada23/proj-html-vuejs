<script>
import AppJumbotron from '../components/AppJumbotron.vue';
import AppBanner from '../components/AppBanner.vue';
import AppTitle from '../components/AppTitle.vue';
import cardsContainer from '../components/cardsContainer.vue';
import AppFeature from '../components/AppFeature.vue';
import AppNews from './AppNews.vue';
export default {
    data: function(){
        return {
            titleOne:{
                title: 'All The Latest News',
                preTitle: 'PHASELLUS EGET METUS'
            },
            titleTwo:{
                title: 'Tutorials & Guides'
            },
            titleThree:{
                title: 'Forum Sections',
                preTitle: 'PHASELLUS EGET METUS'
            },
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
            ],
            albumCardsTwo: [
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
            ],
            feature:{
                title:"FEATURED ARTICLE",
                preTitle:"Cras Malesuada Et Orci Eget Pharetra",
                description:"In quis lectus sed leo elementum faucibus in dapibus dictum. Nullamolestie tortor nec lectus venenatis, sed blandit dui, dolor at bibendum sadips ets ipsums dolores ficilis uns leo lectus.",
                button:"read more",
            }

        }
    },
      components:{
        AppJumbotron,
        AppBanner,
        AppTitle,
        cardsContainer,
        AppFeature,
        AppNews
        
      } 
    }

</script>
<template>
    <div id="main-content">
        <AppJumbotron/>
        <AppBanner/>
        <AppTitle :data="titleOne"/>
        <cardsContainer :data="albumCards"/>
        <AppFeature :data="feature"/>
        <cardsContainer :data="albumCardsTwo"/>
        <AppNews :feature="feature" :title="titleTwo" :cards="albumCards"/>

        
        
    </div>
</template>

<style lang="scss">
@use '../styles/partials/variables' as *;

#main-content{
    background-color: #1c1c1c;
    #jumbotron {
    height: 50rem;
    background-image: url('/images/home_slider_bg.jpg');
    background-size: cover;
    background-attachment: fixed;
    color: white;
        h1{
            margin: 0;
            font-size: 1em;
            text-transform: capitalize;
            font-size: 150px;
            color: white;
        }
        .button-xlarge{
            padding: 17px 40px;
            line-height: 21px;
            font-size: 18px;
        }
    }   
}  
</style>    