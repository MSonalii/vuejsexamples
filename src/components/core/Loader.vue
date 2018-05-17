<template>
  <div class="columns">
      <div class="column loader-container">
<svg version="1.1" id="L1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" viewBox="0 0 100 100" enable-background="new 0 0 100 100" xml:space="preserve">
    <circle fill="none" stroke="#ff3860" stroke-width="6" stroke-miterlimit="15" stroke-dasharray="14.2472,14.2472" cx="50" cy="50" r="47" >
      <animateTransform 
         attributeName="transform" 
         attributeType="XML" 
         type="rotate"
         dur="5s" 
         from="0 50 50"
         to="360 50 50" 
         repeatCount="indefinite" />
  </circle>
  <circle fill="none" stroke="#ff3860" stroke-width="1" stroke-miterlimit="10" stroke-dasharray="10,10" cx="50" cy="50" r="39">
      <animateTransform 
         attributeName="transform" 
         attributeType="XML" 
         type="rotate"
         dur="5s" 
         from="0 50 50"
         to="-360 50 50" 
         repeatCount="indefinite" />
  </circle>
  <g fill="#ff3860">
  <rect x="30" y="35" width="5" height="30">
    <animateTransform 
       attributeName="transform" 
       dur="1s" 
       type="translate" 
       values="0 5 ; 0 -5; 0 5" 
       repeatCount="indefinite" 
       begin="0.1"/>
  </rect>
  <rect x="40" y="35" width="5" height="30" >
    <animateTransform 
       attributeName="transform" 
       dur="1s" 
       type="translate" 
       values="0 5 ; 0 -5; 0 5" 
       repeatCount="indefinite" 
       begin="0.2"/>
  </rect>
  <rect x="50" y="35" width="5" height="30" >
    <animateTransform 
       attributeName="transform" 
       dur="1s" 
       type="translate" 
       values="0 5 ; 0 -5; 0 5" 
       repeatCount="indefinite" 
       begin="0.3"/>
  </rect>
  <rect x="60" y="35" width="5" height="30" >
    <animateTransform 
       attributeName="transform" 
       dur="1s" 
       type="translate" 
       values="0 5 ; 0 -5; 0 5"  
       repeatCount="indefinite" 
       begin="0.4"/>
  </rect>
  <rect x="70" y="35" width="5" height="30" >
    <animateTransform 
       attributeName="transform" 
       dur="1s" 
       type="translate" 
       values="0 5 ; 0 -5; 0 5" 
       repeatCount="indefinite" 
       begin="0.5"/>
  </rect>
  </g>
</svg>


<h1>Loading....</h1>


  </div>
  </div>
</template>


<style lang="scss">
@import url(https://fonts.googleapis.com/css?family=Comfortaa:400,700,300);

*,html{margin:0;padding:0}

//variables
$baseColor :#fff;
$fontColor : #fff;
body{
   font-family: 'Comfortaa', cursive;
}
.loader-container{
        padding-top: 12%;
        background: $baseColor;
        text-align: center;
         height: 100vh;

      svg{
          width: 100px;
          height: 100px;
          margin: 20px;
          display:inline-block;
        }
      h1{
          text-align: center;
          color: #ff3860;
          margin: 0 0 100px;
          font-size: 34px;
          font-weight: 100;
          padding: 20px 0;
          b{
            font-weight: 700;
          }
        }
}
      @media screen and (max-width: 600px) {
   .loader-container{
     padding-top: 50% !important;
   }
}
</style>



<script>
const Loader = {
    name:'loader',

}
export default Loader
</script>
