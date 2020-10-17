<template>

  <div>
    <v-btn color="#4a4a4b">
      <RouterLink :to="lien" >{{ titre }}</RouterLink>
    </v-btn>
  </div>

</template>

<script>

export default {
name: "Button",
  props:[
      'titre',
      'lien'
  ]
}

</script>

<style lang='scss' scoped>

a{
  text-decoration: none;
  color: white !important;
}
</style>
