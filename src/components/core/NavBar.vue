<template>
<div class="navbar-component" >
  <nav class="navbar">
      <div class="navbar-brand">
        <a class="navbar-item" href="/">
        <strong>  My Company </strong>
        </a>
    
        <div class="navbar-burger" @click="showNav = !showNav" :class="{ 'is-active': showNav }">
          <span></span>
          <span></span>
          <span></span>
        </div>
      </div>

      <div class="navbar-menu" :class="{ 'is-active': showNav }">
        <div class="navbar-end">
          <a class="navbar-item" href="/about">
            About
          </a>
          <a class="navbar-item" href="/path">
            Path
          </a>
          <a class="navbar-item" href="/blog">
            Blog
          </a>
        </div>
      </div>
    </nav>
</div>
</template>
<style lang="scss">
.navbar-component{
    .navbar{
        background-color: #0097A7;
        .navbar-item {
             color:#ffffff !important;     
            }
            .navbar-item:hover{
               background-color: #0c646d !important;
             }
             .navbar-burger{
                color: #ffffff;
             }
           }

        }
@media screen and (max-width: 1087px) {
.navbar-menu {
       background-color: #0097A7;
     }
   }
</style>

<script>
const NavBar = {
    name:'nav-bar',
    data() {
        return {
            showNav: false
        }
    }
}
export default NavBar
</script>
