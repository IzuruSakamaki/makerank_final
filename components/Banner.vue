<template>
  <div>
    <b-carousel id="carousel-fade" fade indicators img-width="1024" img-height="480">
      <b-carousel-slide img-src="../assets/img/banner/1.png"></b-carousel-slide>
      <b-carousel-slide img-src="../assets/img/banner/2.png"></b-carousel-slide>
      <b-carousel-slide img-src="../assets/img/banner/3.png"></b-carousel-slide>
      <b-carousel-slide img-src="../assets/img/banner/4.png"></b-carousel-slide>
    </b-carousel>
  </div>
</template>

<style>
.carousel {
  margin-top: -84px;
}

.carousel .img-fluid {
  mask-image: linear-gradient(to bottom, rgba(14,14,14,1) 90%, rgba(14,14,14,0) 100%);
}

.carousel-indicators .active {
  background-color: var(--secondary);
  width: 84px;
}
</style>