<template>
  <div>
    <v-navigation-drawer
        app
        v-model="drawer"
        class="white lighten-2"
        dark
        disable-resize-watcher
    >
      <v-toolbar-title class="name">Oise <span style="color:#FA2021">Télécom</span></v-toolbar-title>

      <v-list nav dense>
        <v-list-item-group color="secondary">
          <v-list-item v-for="(items,item) in drawerItems" :key="item">
            <v-list-item-content>
              <v-list-item-title>
                <router-link :to="items.link">
                  {{ items.name}}
                </router-link>
              </v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list-item-group>
      </v-list>
      <v-spacer></v-spacer>
    </v-navigation-drawer>
    <v-app-bar
        prominent
        height="100px"
        dense
        class="align-center"



    >
      <v-app-bar-nav-icon
          class="hidden-md-and-up"
          @click.stop="drawer = !drawer"
      >

      </v-app-bar-nav-icon>

      <v-toolbar-title class="align-self-center">Oise <span style="color:#FA2021">Télécom</span></v-toolbar-title>

      <v-spacer></v-spacer>
      <div>
        <v-btn  depressed class="hidden-sm-and-down mt-8" text v-for="(navItem, elt) in drawerItems" :key="elt"
        >
          <router-link :to="navItem.link">
            {{ navItem.name }}
          </router-link>
        </v-btn>

      </div>

    </v-app-bar>
  </div>
</template>

<script>

export default {
  name: "AppHeader",
  components: {},
  data : function (){
    return{
      drawer: false,
      drawerItems : [
        {name: "Accueil", link: "/"},
        {name: "Nos boutiques", link: "/Boutiques"},
        {name: "Services", link: "/Services"},
        {name: "Reconditionné", link: "/Reconditionné"},
        {name: "Contact", link: "/Contact"}
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
@import "src/styles/variables.scss";

a{
  text-decoration: none;
  color: $black !important;
  transition: all 300ms ease-in-out;

  &:hover{
    color: $red-custom !important;
    transform: scale(1.1);
  }
}



</style>
