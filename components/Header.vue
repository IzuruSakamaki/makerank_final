<template>
  <div>
    <b-navbar toggleable="sm mt-4" type="dark" variant="primary">
      <b-navbar-brand href="#" tag="h1">
        <img class="position-absolute d-none d-sm-block" src="../assets/img/logo/logo_a.png" alt="MakeRank">
        <div class="d-block d-sm-none">
          <img class="d-inline-block position-static" src="../assets/img/logo/logo_b.png" alt="MakeRank-Mobile">
          <h5 class="d-inline-block">MakeRank</h5>
        </div>
      </b-navbar-brand>
      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
      <b-collapse class="ml-5" id="nav-collapse" is-nav>
        <b-navbar-nav>
          <b-nav-item href="#promo" active>PROMO</b-nav-item>
          <b-nav-item href="#benefits" active>BENEFITS</b-nav-item>
          <b-nav-item href="#services" active>SERVICES</b-nav-item>
          <b-nav-item href="#game" active>GAME</b-nav-item>
          <b-nav-item href="#contact" active>CONTACT</b-nav-item>
        </b-navbar-nav>
        <b-navbar-nav class="ml-auto mr-5">
          <b-nav-item-dropdown  text="SIGN IN" right >
            <b-dropdown-form class="text-center ml-3 mr-3 mt-3 mb-2">
              <b-dropdown-text class="mb-2">Sign in to your account</b-dropdown-text>
              <b-form-group label-for="dropdown-form-email" @submit.stop.prevent>
                <b-form-input
                  id="dropdown-form-email"
                  size="sm"
                  placeholder="Email"
                ></b-form-input>
              </b-form-group>
              <b-form-group label-for="dropdown-form-password">
                <b-form-input
                  id="dropdown-form-password"
                  type="password"
                  size="sm"
                  placeholder="Password"
                ></b-form-input>
              </b-form-group>
              <b-button class="w-100" variant="primary" size="sm" @click="onClick">Sign In</b-button>
            </b-dropdown-form>
            <div class="text-center login-option mb-3">
              <b-dropdown-text class="mb-2 text-center">or sign in with:</b-dropdown-text>
              <b-button size="sm" id="login-option-google">
                <b-img src="../assets/img/icon/google.png" alt="Google"></b-img>
                <b>Google</b>
              </b-button>
              <b-button size="sm" id="login-option-facebook">
                <b-img src="../assets/img/icon/facebook.png" alt="Facebook"></b-img>
                <b>Facebook</b>
              </b-button>
            </div>
          </b-nav-item-dropdown>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<style>
  .navbar {
    z-index: 100;
  }
  .navbar-brand {
    margin-left: 144px;
  }

  .navbar-brand .position-absolute {
    top: -24px;
    left: 84px;
    width: 120px;
  }

  .navbar-brand .position-static {
    width: 24px;
    margin-left: -144px;
    padding-bottom: 3px;
  }

  .navbar-brand h5 {
    padding-left: 12px;
    margin: 0;
  }

  .nav-link, .b-dropdown-form, h5 {
    font-family: 'BebasKai';
  }

  .dropdown-toggle span {
    color: var(--orange);
  }

  .dropdown-menu {
    background-color: var(--secondary);
    min-width: 240px;
  }

  .dropdown-item, .b-dropdown-text {
    color: var(--white);
  }

  .b-dropdown-form .btn{
    background-color: var(--orange);
    border-color: var(--orange);
    min-width: 240px;
  }


  .login-option .btn{
    padding-right: 18px;
  }

  .login-option img {
    height: 36px;
    margin-right: 12px;
  }

  #login-option-facebook {
    background-color: #3B5998;
  }

  #login-option-google {
    color: #4385f5;
    background-color: #FFFFFF;
  }
</style>