<script>
import AppHeader from './components/AppHeader.vue';
import AppJumbo from './components/AppJumbo.vue';
import AppMain from './components/AppMain.vue';
import AppForm from './components/AppForm.vue';
import AppFooter from './components/AppFooter.vue';

export default {

  components: { AppHeader, AppJumbo, AppMain, AppFooter, AppForm },

  data() {

    return {
      

    };
  },
}

</script>

<template>

  <AppHeader></AppHeader>

  <AppJumbo></AppJumbo>

  <AppMain></AppMain>

  <AppForm></AppForm>

  <AppFooter></AppFooter>


</template>

<style lang="scss">

</style>
