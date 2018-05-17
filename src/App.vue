<template>
  <div id="app">
   <span v-if="!showLoader"> <nav-bar/>
    <router-view/>
    <footer-bar />
   </span>
   <span v-else>
       <loader/>
   </span>
  </div>
</template>

<script>
import NavBar from '@/components/core/NavBar'
import Loader from '@/components/core/Loader'
import FooterBar from '@/components/core/FooterBar'

const App = {
  name: 'App',
  components:{
    NavBar,
    Loader,
    FooterBar
  },
  data(){
    return {
      showLoader: true
    }
  },
  created(){
    var self = this
    setTimeout(function(){
        self.showLoader = false;
      }, 2000)
  }
}

export default App 
</script>

