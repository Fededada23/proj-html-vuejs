<script>
    export default {
        data(){
            return{
                avadaLinks: [
                {
                    text: 'Sed semper, nisl id feugiat eleifend, erat est digssim felis, quis auctor elit enim nec ante. Cras et nibh risus. Pellentesque non mi sit amet mi intermentum.',
                    url: '#',
                    current: false,
                },
                
            ],
            topicLinks: [
                {
                    text: 'Morbi vitae dui euismod vulputate sollicitudin',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Morbi vitae dui euismod vulputate sollicitudin',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Morbi vitae dui euismod vulputate sollicitudin',
                    url: '#',
                    current: false,
                },
            ],
            postLinks: [
                {
                    text: 'Morbi vitae dui euismod vulputate sollicitudin',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Morbi vitae dui euismod vulputate sollicitudin',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Morbi vitae dui euismod vulputate sollicitudin',
                    url: '#',
                    current: false,
                },
               
            ],
            latestLinks: [
                {
                    text: 'Dario Pineda on Morbi vitae dui euismod vulputate sollicitudin',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Dario Pineda on Morbi vitae dui euismod vulputate sollicitudin',
                    url: '#',
                    current: false,
                },
            ],
            social: [
                {
                    logo: 'footer-facebook.png',
                },
                {
                    logo: 'footer-pinterest.png',
                },
                {
                    logo: 'footer-twitter.png',
                },
                {
                    logo: 'footer-youtube.png',
                },
            ]
        }
    },
    methods: {
        getImagePath: function (img) {
            return `/images/${img}`
        }
    }
};
</script>
<template>
    <div id="footer-top">
        <div class="footer-top-content">
            <div class="row d-flex pt-5">
                <div class="col">
                    <h4>AVADA TECH FORUM</h4>
                    <ul>
                        <li class="my-2"  v-for="(link, index) in avadaLinks" :key="index">
                            <a :href="link.url">{{link.text}}</a>
                        </li>
                    </ul>
                </div>
                <div class="col">    
                    <h4>POPULAR TOPICS</h4>
                    <ul>
                        <li class="my-2" v-for="(link, index) in topicLinks" :key="index">
                            <a :href="link.url">{{link.text}}</a>
                        </li>
                    </ul>
                </div>
                <div class="col">
                    <h4>RECENT POSTS</h4>
                    <ul>
                        <li class="my-2" v-for="(link, index) in postLinks" :key="index">
                            <a :href="link.url">{{link.text}}</a>
                        </li>
                    </ul>
                </div>
                <div class="col">
                    <h4>LATEST REPLIES</h4>
                    <ul>
                        <li v-for="(link, index) in latestLinks" :key="index">
                            <a :href="link.url">{{link.text}}</a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
    <div class="social">
            <div class="col-but">
                <span>Copyright 2012 - 2023 | Avada Theme by ThemeFusion | All Rights Reserved | Powered by WordPress</span>
            </div>
            <div class="icon">
                <ul>
                    <li v-for="(object, index) in social" :key="index">
                        <a href="#"><img :src="getImagePath(object.logo)" alt="loghi"></a>
                    </li>
                </ul>
            </div>
        </div>
</template>
<style lang="scss">
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

    #footer-top{
    height: 20rem;
    
    color: gray;
    max-width: 1440px;
    margin: 0 auto;
    }
    .footer-top-content{
        h4{
            font-size: 18px;
            color:black;
            padding-top: 10px;
        }
        ul{
            padding-left: 0;
            
            li a{
                font-size: 15px;
                color:grey
            }
        }
    };

    .social {
    height: 150px;
    background-color: white;
    align-items: center;
    display: flex;
    justify-content: space-around;
    
    color: gray;
        .span{
            font-size: 10px;
        }
        .icon {
            display: flex;
            align-items: center;
            @include upbold;
            ul {
                display: flex;
                gap: .5em;
            }
            li {
                display: flex;
                color: $white;
                list-style: $listnone;
                &:hover {
                    filter: brightness(100);
                }
            }
            .follow {
                @include upbold;
                color: #0282f9;
                padding-right: .5em;
            }
        }
    }
    .footer-button {
        @include button;
        &:hover {
            font-size: 15px;
            cursor: pointer;
            filter: brightness(1.2);
        }
}
    
</style>      