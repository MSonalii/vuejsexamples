<template>
  <section class="hero  footer-bar">
      <div class="hero-body">
        <div class="container">
          <p class="title">
            My Company
          </p>
          <p class="subtitle">
            All Rights reserved.
          </p>
        </div>
      </div>
    </section>
</template>
<style lang="scss">
.footer-bar{
    background-color: #0097a7;
    margin-top: 4%;
    .hero-body{
        .container{
            .title{
                color: white;
            }
            .subtitle {
                color: wheat;
            }
        }
    }
}
</style>

<script>

const FooterBar = {
    name:'footer-bar'
}
export default FooterBar
</script>
