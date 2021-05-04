<template>
  <v-app dark>
    <core-toolbar />
    <v-container>
      <v-img 
      height="100%"
      :src="require('@/assets/background.jpg')">
        <router-view />
      </v-img>
    </v-container>

    <core-footer />>
  </v-app>  
</template>
<script>
export default {
  components: {
    CoreFooter: () => import('@/components/core/Footer'),
    CoreToolbar: () => import('@/components/core/Toolbar')
  }
}
</script>
<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
