<script>
     export default {
        data(){
            return{
                headerLinks:[
                    {
                        label:'Home',
                        url:'#',
                        active:false
                    },
                    {
                        label:'Apple',
                        url:'#',
                        active:false
                    },
                    {
                        label:'Microsoft',
                        url:'#',
                        active:false
                    },
                    {
                        label:'Android',
                        url:'#',
                        active:false
                    },
                    {
                        label:'Forums',
                        url:'#',
                        active:false
                    },
                    {
                        label:'Contact us',
                        url:'#',
                        active:false
                    },
                ]
            }
        }
    }
</script>
<template lang="">
    <header>
        <a href="/" class="brand">
            <img :src="`/images/logo-2x.png`">
        </a>
        <nav>
            <ul>
                <li v-for="(link,index) in headerLinks" :key="index">
                    <a :href="link.url" :class="link.active ? 'active' :''">
                        {{link.label}}
                    </a>
                </li>
                <button class="header-button">JOIN US</button>
            </ul>
        </nav>

    </header>    
</template>
<style lang="scss">
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins' as *;
    header{
        /*width: 100%;
        top: 0;
        position: fixed;*/
        min-height: 65px;
        text-align: center;
        @include center;
        justify-content: space-around;
        background-color:#27aabe;
        img{
            width: 70%;
        }
        
        ul{
            list-style-type: none;
            margin: 2rem 1rem;
            @include center;
            li a{
                
                display: inline-block;
                padding: 1rem;
                text-decoration: none;
                font-weight: 600;
                transition: background-color 0.3s;
                &.active, &:hover{
                    border-bottom: 4px solid $secondaryColor;
                }
                color: white;
                text-transform: uppercase;
                font-size: .8rem;
                
            }
    
        }
        .header-button{
            background-color: black;
            color: white;
            font-weight: bold;
            text-transform: uppercase;
            text-align: center;
            text-decoration: none;
            padding: 11px 23px;
            line-height: 16px;
            font-size: 13px;
        }
    }

    
</style>