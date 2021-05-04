<template>
  <v-app :dark="true">
    <core-toolbar />
    <v-container>
        <router-view />
    </v-container>

    <core-footer />
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
  background-image: linear-gradient( rgba(0, 0, 0, 0.3), rgba(0, 0, 0, 0.3) ),url(assets/background.jpg);
  min-height: 100%;
  background-position: center;
  background-size: cover;
  text-align: center;
  font-size: 11pt;
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

.footer {
  text-align: center
}
</style>
