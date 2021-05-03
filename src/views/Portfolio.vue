<template>
  <core-section id="portfolio">
    <abstract-3 />
    <core-heading v-text="'What I\'ve done'" />

    <v-carousel
      :height="600"
      class="elevation-0"
      hide-controls
      :cycle="false"
    >
      <v-carousel-item
        v-for="(project, i) in projects"
        :key="i"
      >
        <project :value="project" />
      </v-carousel-item>
    </v-carousel>
  </core-section>
</template>

<script>
export default {
  components: {
    Abstract3: () => import('@/components/Abstract3'),
    Project: () => import('@/components/Project')
  },
  data: () => ({
    projects: [
      {
        name: 'Classic Cafe Rebrand',
        category: 'Logo Design',
        src: 'classic-cafe.png'
      },
      {
        name: 'Flagship',
        category: 'Digital Design',
        src: 'flagship.jpg'
      },
      {
        name: 'Biere Craft Beer',
        category: 'Marketing and Graphic Design',
        src: 'biere.jpg'
      }
    ]
  })
}
</script>

<style>
  .v-carousel__controls {
    background: transparent;
  }
</style>
