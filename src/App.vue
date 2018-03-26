<template>
  <div id="app">
    <Header/>
    <br/>
    <b-row>
      <LeftSidebar/>
      <b-col sm=7>
        <router-view/>
      </b-col>
      <RightSidebar/>
    </b-row>
  </div>
</template>
<script>
import Header from './components/Header.vue'
import LeftSidebar from './components/LeftSidebar.vue'
import RightSidebar from './components/RightSidebar.vue'

export default {
  components: {
    Header,
    LeftSidebar,
    RightSidebar
  }
}
</script>
<style>
#app {
  max-width: 100%;
  overflow-x: hidden;
}
</style>
