<template>
<div class="home-page">

    <div class="container">
      <div class="columns first-box ">
       
        <div class="column ">
          <div class="text-section">
            <h1 class="title">
                Featured Products.
          </h1>
      <h2 class="subtitle">
        wide range of products for you.
      </h2>
      <p class="">
“The story so far:
In the beginning the Universe was created.
This has made a lot of people very angry and been widely regarded as a bad move.” <br/>
― Douglas Adams,
      </p>
          </div>
          <div class="btn-container">
  
          <a class="button is-primary is-outlined">How does it work</a>
        <a class="button is-link is-outlined">Explore more</a>

</div>

  </div>
  <div class="column is-8">
  <video src="../assets/big_buck_bunny.mp4" autoplay loop muted width="746px" ></video>
  </div>
         </div>
     
    </div>
 <product-list :Products='Products'></product-list>

</div>
</template>
<style lang="scss">
body{

    background: -moz-linear-gradient(top, rgba(235,233,249,0.14) 0%, rgba(232,230,248,0.14) 7%, rgba(216,208,239,0.17) 50%, rgba(206,199,236,0.17) 51%, rgba(197,193,235,0.2) 85%, rgba(193,191,234,0.2) 100%); /* FF3.6-15 */
background: -webkit-linear-gradient(top, rgba(235,233,249,0.14) 0%,rgba(232,230,248,0.14) 7%,rgba(216,208,239,0.17) 50%,rgba(206,199,236,0.17) 51%,rgba(197,193,235,0.2) 85%,rgba(193,191,234,0.2) 100%); /* Chrome10-25,Safari5.1-6 */
background: linear-gradient(to bottom, rgba(235,233,249,0.14) 0%,rgba(232,230,248,0.14) 7%,rgba(216,208,239,0.17) 50%,rgba(206,199,236,0.17) 51%,rgba(197,193,235,0.2) 85%,rgba(193,191,234,0.2) 100%); /* W3C, IE10+, FF16+, Chrome26+, Opera12+, Safari7+ */

}
.home-page{
  .columns{
    margin-left: 0px;
    margin-right: 0px;
  }
    .container{
      .first-box{ 
        margin-top: 20px;
      }
    .btn-container{
      margin-top: 2%;
    }
    }
  @media screen and (min-width: 768px) {
   .text-section {
      padding-top: 20%;
      }
}
}
</style>

<script>
import ProductList from '@/components/ProductList'
import Bunny from '@/assets/Bunny.png'
import Duck from '@/assets/Duck.png'
import Timon from '@/assets/Timon.png'
import Sid from '@/assets/sid.png'
import axios from 'axios'
import VueAxios from 'vue-axios'

const HomePage = {
  name: 'HomePage',
  components:{
    ProductList
  },
  data () {
    return {
      Products: {}
    }
  },
  created() {
    var that = this;
    console.log('propertyComputed will update, as this.property is now reactive.')
    axios.get('https://noderestserver.herokuapp.com/products', {
 
	}).then(function (response) {
    console.log('response is : ' , response.data.Products.product);
    that.Products = response.data.Products;
	}).catch(function (error) {
    console.log('error occured ', error);
});
  }
}
export default HomePage
</script>

<style lang="scss">

</style>

