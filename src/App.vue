<template>
  <v-app>
    <div class="main_container">
      <AppHeader/>
      <section>
      <router-view />
      </section>
    <AppFooter/>
    </div>
  </v-app>
</template>

<script>


import AppHeader from "@/components/Layout/AppHeader";
import AppFooter from "@/components/Layout/AppFooter";
export default {
  name: 'App',

  components: {
    AppFooter,
    AppHeader

  },

  data: () => ({
    //
  }),
};
</script>
<style lang="scss" scoped>

.main_container{
  display: grid !important;
  grid-auto-rows: 0.2fr 3fr 0.3fr ;
  grid-gap: 5px;
  min-height: 100vh;
}
  body{
    margin: 0;
    padding: 0;
    min-height: 100vh;
  }
</style>
