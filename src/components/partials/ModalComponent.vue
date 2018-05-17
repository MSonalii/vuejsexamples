<template>
  <div>
       <div class="modal-background"></div>
         <div class="modal-card customCardModal">
            <header class="modal-card-head">
             <p class="modal-card-title">{{singleProduct.product_name}}</p>
             <button class="delete" aria-label="close" @click="closeModal"></button>
            </header>
    <section class="modal-card-body">
            <figure class="image is-4by3">
                <img :src='singleProduct.product_img' alt="Placeholder image">
            </figure>
        <div class="content">
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla accumsan, metus ultrices eleifend gravida, nulla nunc varius lectus, nec rutrum justo nibh eu lectus. Ut vulputate semper dui. Fusce erat odio, sollicitudin vel erat vel, interdum mattis neque.</p>   
            <Tags :tags="singleProduct.tags"></Tags>
            <select-component :categary="singleProduct.categary"></select-component> 
        </div>      
           <article class="media">
                <div class="media-content">
                    <div class="field">
                    <p class="control">
                        <textarea class="textarea" placeholder="Add a comment..."></textarea>
                    </p>
                </div>  
                </div>
            </article>
            <table-design></table-design>
    </section>
    <footer class="modal-card-foot">
      <button class="button is-success " @click="closeModal">Save changes</button>
      <button class="button" @click="closeModal">Cancel</button>
    </footer>
  </div>
  </div>
</template>
<style lang="scss" >


     .customCardModal {
margin: 0px !important;
}

</style>

<script>
import Tags from './Tags'
import SelectComponent from './SelectComponent'
import TableDesign from './TableDesign'

const ModalComponent = {
    name:'modal-component',
    props:['singleProduct'],
    components:{
        Tags,
        SelectComponent,
        TableDesign
    },  
        methods:{
        closeModal(){
            this.singleProduct.isActive = false
        }
    }
}
export default ModalComponent
</script>
