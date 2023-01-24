<script>
    import AppHeader from './components/AppHeader.vue';
    import AppMain from './components/AppMain.vue';
    
    import AppFooterTop from './components/AppFooterTop.vue';
    
    export default {
      components:{
        AppHeader,
        AppMain,
        
      
        AppFooterTop,
        
      } 
    }
</script>
<template>
  <div>
    <AppHeader/>
    <AppMain/>
    
    <AppFooterTop/>
   
  </div>
</template>
<style lang="scss">
  @use './styles/generals.scss' as *;
  
</style>