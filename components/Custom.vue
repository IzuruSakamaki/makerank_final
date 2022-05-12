<template>
  <div class="customs text-center" id="custom">
    <b-img class="d-none d-xl-inline-block" src="../assets/img/accessories/l1.png" fluid alt="acc-left-1"></b-img>
    <h4 class="d-inline-block">Cannot Find The Service / The Game You Want?</h4>
    <b-img class="d-inline-block" src="../assets/img/accessories/l1.png" fluid alt="acc-left-1" style="transform:rotate(180deg)"></b-img>
    <p class="mb-5">Contact us for custom order</p>
    <b-form>
      <b-form-group class="d-inline-block" label-for="form-name" @submit.stop.prevent>
        <b-form-input
          id="form-name"
          size="sm"
          placeholder="Name"
        ></b-form-input>
      </b-form-group>
      <b-form-group class="d-inline-block" label-for="form-email">
        <b-form-input
          id="form-email"
          type="email"
          size="sm"
          placeholder="Email"
        ></b-form-input>
      </b-form-group>
      <b-form-group class="d-inline-block" label-for="form-game">
        <b-form-input
          id="form-game"
          size="sm"
          placeholder="What Game?"
        ></b-form-input>
      </b-form-group>
      <b-form-group class="d-inline-block" label-for="form-service">
        <b-form-input
          id="form-service"
          size="sm"
          placeholder="What Service?"
        ></b-form-input>
      </b-form-group>
      <b-form-group class="group-desc" label-for="form-desc">
        <b-form-textarea
          id="textarea"
          v-model="text"
          placeholder="Please describe in more detail your order..."
          rows="9"
          max-rows="9"
        ></b-form-textarea>
      </b-form-group>
      <b-button variant="primary" size="sm" @click="onClick">Contact Us</b-button>
    </b-form>
  </div>
</template>

<style>

  .customs {
    background: url("../assets/img/bg/custom.png") fixed;
    mask-image: linear-gradient(to top, rgba(14,14,14,1) 90%, rgba(14,14,14,0) 100%);
  }
  .customs h5, .customs h4 {
    color: var(--white);
  }

  .customs p {
    color: gray;
  }

  .customs h4{
    font-family: 'RobotoBold';
    margin: 96px 12px 12px 12px;
  }

  .customs form {
    margin: 0 120px;
  }

  .customs form .d-inline-block {
    width: 47%;
    margin: 0px 6px 24px 6px;
  }

  .customs input {
    padding: 18px 12px;
  }

  .customs .group-desc {
    width: 96%;
    margin: 0 auto;
  }

  #form-desc {
    height: 100px;
  }

  .customs .btn {
    margin: 24px 0px 96px 0px;
    background: var(--orange);
    border: none;
    width: 120px;
    font-family: 'RobotoMedium';
  }

</style>