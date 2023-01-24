<script>
    export default {
        data(){
            return{
                dcComicsLinks: [
                {
                    text: 'Characters',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Comics',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Movies',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Tv',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Games',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Collectibles',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Videos',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Fans',
                    url: '#',
                    current: false,
                },
                {
                    text: 'News',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Shop',
                    url: '#',
                    current: false,
                }
            ],
            shopLinks: [
                {
                    text: 'Shop DC',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Shop DC Collectibles',
                    url: '#',
                    current: false,
                }
            ],
            dcLinks: [
                {
                    text: 'Term of Use',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Privacy policy (New)',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Ad Choices',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Advertising',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Jobs',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Subscriptions',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Talent Workshop',
                    url: '#',
                    current: false,
                },
                {
                    text: 'CPSC Certificates',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Ratings',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Shop Help',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Contact Us',
                    url: '#',
                    current: false,
                }
            ],
            sitesLinks: [
                {
                    text: 'DC',
                    url: '#',
                    current: false,
                },{
                    text: 'MAD Magazine',
                    url: '#',
                    current: false,
                },
                {
                    text: 'DC Kids',
                    url: '#',
                    current: false,
                },
                {
                    text: 'DC Universe',
                    url: '#',
                    current: false,
                },
                {
                    text: 'DC Power Visa',
                    url: '#',
                    current: false,
                },
            ],
            social: [
                {
                    logo: 'footer-facebook.png',
                },
                {
                    logo: 'footer-periscope.png',
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
            <div class="footer-top-content-links">
                <div class="col">
                    <h4>Dc Comics</h4>
                    <ul>
                        <li v-for="(link, index) in dcComicsLinks" :key="index">
                            <a :href="link.url">{{link.text}}</a>
                        </li>
                    </ul>
                    <h4>Shop</h4>
                    <ul>
                        <li v-for="(link, index) in shopLinks" :key="index">
                            <a :href="link.url">{{link.text}}</a>
                        </li>
                    </ul>
                </div>
                <div class="col">
                    <h4>Dc</h4>
                    <ul>
                        <li v-for="(link, index) in dcLinks" :key="index">
                            <a :href="link.url">{{link.text}}</a>
                        </li>
                    </ul>
                </div>
                <div class="col">
                    <h4>Sites</h4>
                    <ul>
                        <li v-for="(link, index) in sitesLinks" :key="index">
                            <a :href="link.url">{{link.text}}</a>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="dc_bg">
                <div class="img_dc_bg">
                </div>
            </div>
        </div>
    </div>
    <div class="social">
            <div class="col-but">
                <button class="footer-button">Sign-up now!</button>
            </div>
            <div class="icon">
                <h3 class="follow">Follow us</h3>
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
    height: 30rem;
    background-image: url(/images/footer-bg.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    }
    .footer-top-content{
        @include container;
        @include d-flex(space-between, '');
        height: 100%;
        &-links{
            width: 50%;
            padding: 1rem 0;
            @include d-flex('', '');
            .col:nth-child(2){
                margin: 0  2rem;
            }
            
            h4{
                text-transform: uppercase;
                color: white;
            }
            ul{
                padding: 1rem 0;
                li{
                    font-size: 15px;
                    a{
                        color: #b4b4b4;
                    }
                }
            }
            
        }
    }
    .dc_bg {
        background-image: url(/images/dc-logo-bg.png);
        background-size: cover;
        background-position: right center;
        width: 600px;
    }

    .social {
    height: 150px;
    background-color: #303030;
    align-items: center;
    display: flex;
    justify-content: space-around;
    @include upbold;
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