<template>
  <div class="services text-center" id="services">
    <b-img class="d-none d-xl-inline-block" src="../assets/img/accessories/l1.png" fluid alt="acc-left-1"></b-img>
    <h4 class="d-inline-block">Popular Services</h4>
    <b-img class="d-inline-block" src="../assets/img/accessories/r1.png" fluid alt="acc-right-1"></b-img>
    <b-container class="service-container">
      <b-card
        overlay
        class="d-inline-block"
        img-src="../assets/img/bg/services/pr.png"
        img-alt="Card Image"
        text-variant="white"
      >
      </b-card>
      <b-card
        overlay
        class="d-inline-block"
        img-src="../assets/img/bg/services/gf.png"
        img-alt="Card Image"
        text-variant="white"
      >
      </b-card>
      <b-card
        overlay
        class="d-inline-block"
        img-src="../assets/img/bg/services/pw.png"
        img-alt="Card Image"
        text-variant="white"
      >
      </b-card>
    </b-container>
  </div>
</template>

<style>

  .services {
    background: url("../assets/img/bg/services.png") fixed;
    mask-image: linear-gradient(to top, rgba(14,14,14,1) 90%, rgba(14,14,14,0) 100%);
  }
  .services h5, .services h4, p {
    color: var(--white);
  }

  .services h4{
    font-family: 'RobotoBold';
    margin: 96px 12px 0px 12px;
  }

  .service-container{
    margin-top: 96px;
    padding-bottom: 120px;
  }

  .service-container img{
    max-height: 300px;
    width: auto;
  }

  .services .card {
    background: transparent;
    margin-top: 12px;
    border: none;
  }

</style>