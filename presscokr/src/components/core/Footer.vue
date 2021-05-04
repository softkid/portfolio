<template>
  <v-footer
    fixed
    class="footer"
    style="opacity: 0.5;"
  >
    <v-flex
      text-xs-center
      xs12
      dark
    >
      @{{ new Date().getFullYear() }} <strong>PRESSCO WEBKIT</strong> FROM KOREA, GIMHAE<!-- social-media small /-->
    </v-flex>
  </v-footer>
</template>

<script>
export default {
  components: {
    // SocialMedia: () => import('@/components/SocialMedia')
  }
}
</script> 