<template>
  <v-app>
    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>

export default {
  name: 'App',
  data: () => ({
  }),
  mounted(){
     this.$root.$on('toggleNoScroll', () => {
        document.documentElement.classList.toggle('no-scroll') // add a class named 'no-scroll' to the document element
    })
  }
};
</script>

<style lang="scss">
@import '@/styles/styles.scss';
</style>
