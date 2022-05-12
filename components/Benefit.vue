<template>
  <div class="commitments text-center" id="benefits">
    <b-img class="d-none d-xl-inline-block" src="../assets/img/accessories/l1.png" fluid alt="acc-left-1"></b-img>
    <h4 class="d-inline-block">Our Commitment</h4>
    <b-img class="d-inline-block" src="../assets/img/accessories/r1.png" fluid alt="acc-right-1"></b-img>
    <b-container class="commitment-container">
      <b-row class="justify-content-center">
        <b-col sm="3">
          <b-img src="../assets/img/icon/commitment/safe.png" alt="Safe Service"></b-img>
          <h5>Safe Service</h5>
          <p>
            Akun kamu dijamin aman di tangan kami! 
            Kami juga akan membimbingmu untuk mengamankan 
            akun sebelum dan setelah melakukan transaksi
          </p>
        </b-col>
        <b-col sm="3">
          <b-img src="../assets/img/icon/commitment/garansi.png" alt="Garansi"></b-img>
          <h5>Garansi Anti Turun*</h5>
          <p>
            Layanan kami cocok untuk kamu yang kesulitan 
            push rank sendirian!
          </p>
        </b-col>
        <b-col sm="3">
          <b-img src="../assets/img/icon/commitment/experts.png" alt="Experts"></b-img>
          <h5>Experts Team</h5>
          <p>
            Seluruh talent di Talent Pool yang dikelola 
            MakeRank sudah melalui seleksi khusus game 
            dan diikat oleh kontrak professional
          </p>
        </b-col>
        <b-col sm="3">
          <b-img src="../assets/img/icon/commitment/fun.png" alt="Playmates"></b-img>
          <h5>Fun Playmates</h5>
          <p>
            Seluruh pilot (player) kami dijamin 
            orangnya asik dan no-toxic-toxic club!
          </p>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<style>
  .commitments h5, .commitments h4, p {
    color: var(--white);
  }

  .commitments h4{
    font-family: 'RobotoBold';
    margin: 96px 12px 0px 12px;
  }

  .commitments h5 {
    font-family: 'RobotoMedium';
    height: 48px;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .commitment-container {
    margin-top: 96px;
  }
</style>
