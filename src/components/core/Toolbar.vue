<template>
  <v-toolbar
    color="rgba(0, 0, 0, 0.12)"
    fixed
    flat
  >
    <h1 class="headline">
      <span class="font-weight-black hidden-sm-and-down">
        PRESSCO
      </span>
      <span class="font-weight-light">
        WEBKIT
      </span>
    </h1>
    <v-spacer />
    <v-btn
      text
      class="subheading mr-4 hidden-xs-only"
      color="primary"
      href="http://store.pressco.kr"
    >
      Store
    </v-btn>
    <v-avatar>
      <img
        :src="require('@/assets/kakao.png')"
        alt="OpenChat"
        @click="openchat"
      >
    </v-avatar>
  </v-toolbar>
</template>

<script>
// Utilities
import { mapMutations } from 'vuex'

export default {
  name: 'Toolbar',
  data: () => ({
    items: []
  }),
  methods: {
    openchat () {
      window.open('https://open.kakao.com/o/sjFAfxwb', 'mywindow', 'status=1')
    },
    ...mapMutations('app', ['toggleDrawer'])
  }
}
</script>
<style>
.kakaoimg { max-width: 40px; height: auto; object-fit: cover; }
</style>
