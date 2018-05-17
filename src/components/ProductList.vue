<template>
 <div class="columns product-list">
    <div class="column" v-for="product in Products.product" :key="product.name">
        <div class="card">
            <div class="card-image">
                <figure class="image is-4by3">
                     <img :src='"../assets/"+product.imageUrl+".png"'  alt="Placeholder image">
                </figure>
            </div>
            <div class="card-content">
                <div class="media">
                    <div class="media-left">
                        <figure class="image is-48x48">
                            <img :src='"../assets/"+product.imageUrl+".png"' alt="Placeholder image">
                            <!-- <img src="../assets/Duck.png" /> -->
                        </figure>
                    </div>
                    <div class="media-content">
                        <p class="title is-4"> {{product.name}}</p>
                        <p class="subtitle is-6">@ {{product.name}}</p>
                    </div>
                </div>

                <div class="content">
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus nec iaculis mauris. <a>@bulmaio</a>.
                    <a href="#">#css</a> <a href="#">#responsive</a>
                    <br>
                    <time datetime="2016-1-1">11:09 PM - 1 Jan 2016</time>
                </div>

            </div>
            <footer class="card-footer">
                <a href="#" class="card-footer-item" @click="showModal(product)">Details</a>

                <a href="#" class="card-footer-item" @click="openCart()">Add to Cart</a>
            </footer>
        </div>
    </div>


      <div class="modal" v-if="singleProduct.isActive" v-bind:class="{ 'is-active': singleProduct.isActive }">
          <ModalComponent :singleProduct="singleProduct" />
        </div>
        <div class="modal" v-if="singleProduct.isCartOpen" v-bind:class="{ 'is-active': singleProduct.isCartOpen }">
            <addto-cart :singleProduct="singleProduct" ></addto-cart>

        </div>

</div>
</template>
<style lang="scss">
.product-list{
     margin-top: 4%;
    .image.is-4by3{
        max-width: 200px;
        margin: 0 auto;
       
    }
}
</style>
<script>
import ModalComponent from '@/components/partials/ModalComponent'
import AddtoCart from '@/components/partials/AddtoCart'

const ProductList = {
    name:'product-list',
    components:{
        ModalComponent,
        AddtoCart
    },
    props: {
        Products: {
            type:Object,
            required:true
        }
    },
    data() {
        return {

            singleProduct :{
                  isActive: false,
                  isCartOpen: false,
                  product_name: '',
                  product_img: '',
                  tags:'',
                  categary: ''
            }
          
        
        }
    },
    methods:{
        showModal(prod) {
           this.singleProduct.isActive = true
           this.singleProduct.product_name = prod.name
           this.singleProduct.product_img = prod.imageUrl
           this.singleProduct.tags = prod.tags
           this.singleProduct.categary = prod.categary
        },
        closeModal(){
            this.isActive = false
        },
        openCart(){
            this.singleProduct.isCartOpen = true
        }
    }
}
export default ProductList
</script>
