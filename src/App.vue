<template>
  <v-app dark>
    <core-toolbar />

    <v-content>
      <v-img
        height="100%"
        :src="require('@/assets/background.jpg')"
        gradient="to bottom right, rgba(0, 0, 0, 0.82), rgba(0, 0, 0, 0.42)"
      >
        <router-view />
      </v-img>
    </v-content>

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