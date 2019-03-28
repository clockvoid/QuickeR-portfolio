<template>
  <div id='app'>
    <Top />
    <Description />
    <Features />
    <Footer />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import Top from './components/Top.vue'
import Description from './components/Description.vue'
import Features from './components/Features.vue'
import Footer from './components/Footer.vue'

@Component({
  components: {
    Top,
    Description,
    Features,
    Footer
  }
})

export default class App extends Vue {
}
</script>

<style lang="scss">
@import "../node_modules/bulma/bulma.sass";
@import url('https://fonts.googleapis.com/css?family=Patua+One');
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
