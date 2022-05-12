<template>
  <div class="footer" id="footer">
    <h4 class="d-inline-block">Know Us</h4>
    <b-container class="footer-container">
      <b-row class="justify-content-center">
        <b-col sm="3">
          <h5>Hubungi Kami</h5>
          <p>makerank.id</p>
          <p>+6285731269002</p>
        </b-col>
        <b-col sm="3">
          <h5>Tentang MakeRank</h5>
          <p>
            MakeRank adalah platform yang menyediakan 
            servis dari Pro-Player untuk berbagai jenis 
            game online. Sekarang, tidak perlu repot 
            mencari Pro-Player yang terpercaya untuk 
            meningkatkan gaming experience kamu.
          </p>
        </b-col>
        <b-col sm="3">
          <h5>Payment</h5>
          <p>- Gopay</p>
          <p>- Ovo</p>
          <p>- Shopeepay</p>
          <p>- Dana</p>
        </b-col>
        <b-col sm="3">
          <h5>Layanan Kami</h5>
          <p>Mobile Legends</p>
          <p>Guild Wars 2</p>
          <p>PUBG Mobile</p>
          <p>Albion Online</p>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<style>
  .footer {
    background: #010326;
    padding-bottom: 24px;
  }
  .footer h5, .footer h4, p {
    color: var(--white);
  }

  .footer p {
    margin-bottom: 12px;
    font-family: 'RobotoMedium';
  }

  .footer h4{
    font-family: 'RobotoBold';
    margin: 36px 12px 0px 60px;
  }

  .footer h5 {
    font-family: 'RobotoMedium';
    height: 48px;
    display: flex;
    align-items: center;
  }

  .footer-container {
    margin-top: 24px;
  }
</style>