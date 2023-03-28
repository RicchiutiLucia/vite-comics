<script>
import AppHeader from './components/AppHeader.vue';
import AppJumbo from './components/AppJumbo.vue'
import AppMain from './components/AppMain.vue';
import BlueSection from './components/BlueSection.vue';
import AppFooter from './components/AppFooter.vue';


export default {
  name: "App",
  components: {
    AppHeader,
    AppMain,
    BlueSection,
    AppFooter,
    AppJumbo
  }
}

</script>

<template>

    <AppHeader></AppHeader>
    <AppJumbo></AppJumbo>
    <AppMain></AppMain>
    <BlueSection></BlueSection>
    <AppFooter></AppFooter>
    
 
</template>


<style lang="scss">
@use "./styles/partials/variables" as *;
@use "./styles/generals.scss" as *;
</style>
