<script>
    import AppHeader from './components/AppHeader.vue';
    
    
    import AppFooterTop from './components/AppFooterTop.vue';
    
    export default {
      components:{
        AppHeader,
        
      
        AppFooterTop,
        
      } 
    }
</script>
<template>
  <div>
    <AppHeader/>
    
    <AppFooterTop/>
   
  </div>
</template>
<style lang="scss">
  @use './styles/generals.scss' as *;
  
</style>