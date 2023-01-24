<script>
import AppJumbotron from '../components/AppJumbotron.vue';
import AppBanner from '../components/AppBanner.vue';
export default {
      components:{
        AppJumbotron,
        AppBanner,
        
      } 
    }

</script>
<template>
    <div id="main-content">
        <AppJumbotron/>
        <AppBanner/>
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