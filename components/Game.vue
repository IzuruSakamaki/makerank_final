<template>
  <div class="games text-center" id="game">
    <b-img class="d-none d-xl-inline-block" src="../assets/img/accessories/l1.png" fluid alt="acc-left-1"></b-img>
    <h4 class="d-inline-block">Games</h4>
    <b-img class="d-inline-block" src="../assets/img/accessories/r1.png" fluid alt="acc-right-1"></b-img>
    <b-container class="game-container">
      <b-row class="justify-content-center">
        <b-col sm="6" class="list-game">
          <b-img class="position-absolute" src="../assets/img/bg/mlbg.png" alt="MLBG"></b-img>
          <b-row >
            <b-button size="sm" id="game-option-valorant">
              <b-img class="d-block" src="../assets/img/icon/games/all/vl.png" alt="Valorant"></b-img>
            </b-button>
          </b-row>
          <b-row >
            <b-button size="sm" id="game-option-guild-wars">
              <b-img class="d-block" src="../assets/img/icon/games/all/gw.png" alt="Guild Wars"></b-img>
            </b-button>
          </b-row>
          <b-row >
            <b-button size="sm" id="game-option-pubg">
              <b-img class="d-block" src="../assets/img/icon/games/all/pj.png" alt="PUBG"></b-img>
            </b-button>
          </b-row>
          <b-row >
            <b-button size="sm" id="game-option-mobile-legend">
              <b-img class="d-block" src="../assets/img/icon/games/all/ml.png" alt="Mobile Legends"></b-img>
            </b-button>
          </b-row>
          <b-row >
            <b-button size="sm" id="game-option-albion">
              <b-img class="d-block" src="../assets/img/icon/games/all/ao.png" alt="Albion Online"></b-img>
            </b-button>
          </b-row>
        </b-col>
        <b-col sm="6" class="option-transaction">
          <h5>MOBILE LEGENDS</h5>
          <p>
            Mobile Legends: Bang Bang adalah sebuah permainan 
            MOBA (Multiplayer Online Battle Arena) yang 
            dirancang untuk ponsel. Kedua tim lawan berjuang 
            untuk mencapai dan menghancurkan base musuh 
            sambil mempertahankan base mereka sendiri. 
            Pilih servis untuk Main Bareng (Mabar) Pro-Player 
            atau Push Rank akunmu oleh expert team kami. 
          </p>
          <b-button size="sm" v-model="selected" id="service-option-push-rank">
            <b-img class="d-block" src="../assets/img/icon/games/Push Rank LG.png" alt="Push Rank"></b-img>
            <b>Push Rank</b>
          </b-button>
          <b-button size="sm" v-model="selected" id="service-option-mabar">
            <b-img class="d-block" src="../assets/img/icon/games/Mabar LG.png" alt="Mabar"></b-img>
            <b>Mabar</b>
          </b-button>
          <b-button size="sm" v-model="selected" id="service-option-grinding">
            <b-img class="d-block" src="../assets/img/icon/games/Grinding LG.png" alt="Grinding"></b-img>
            <b>Grinding</b>
          </b-button><br>
          <b-button pill  @click="$bvModal.show('modal-scoped')" class="d-block float-right" size="sm" id="order"><b>Pesan</b></b-button>
        </b-col>
      </b-row>
    </b-container>
    <b-modal id="modal-scoped">
      <template #modal-header="{ close }">
        <h5>Pesan Sekarang!</h5>
        <b-button pill size="sm" variant="outline-danger" @click="close()">X</b-button>
      </template>
      <template>
        <div>
          <b-form class="text-center" id="transform" @submit="onSubmit" v-if="show">
              <label>Your Contact</label>
            <b-input-group
              id="input-group-number"
              prepend="+62"
            >
              <b-form-input
                v-model="form.number"
                type="number"
                placeholder="Whatsapp Number"
                required
              ></b-form-input>
            </b-input-group>
            <b-form-group id="input-group-service" label="Service Details" label-for="input-service">
              <b-form-select v-model="form.service" :options="optionService" class="mb-3">
                <template #first>
                  <b-form-select-option :value="null" disabled>-- Choose Service --</b-form-select-option>
                </template>
              </b-form-select>
              <b-form-select v-model="form.package" :options="optionPackage" class="mb-3">
                <template #first>
                  <b-form-select-option :value="null" disabled>-- Choose Package --</b-form-select-option>
                </template>
              </b-form-select>
            </b-form-group>
          </b-form>
          <b-card class="mt-3" header="Ntar diapus bre, buat ngecek logic doang">
            <pre class="m-0">{{ form }}</pre>
          </b-card>
        </div>
      </template>
      <template #modal-footer="{ ok }">
        <b-button type="submit" variant="primary" form="transform" @submit="ok(onSubmit)">
          Checkout
        </b-button>
      </template>
    </b-modal>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        form: {
          number: '',
          service: null,
          package: null,
        },
        show: true,
        optionService: [
          { value: 'PushRank', text: 'Push Rank' },
          { value: 'Mabar', text: 'Main Bareng 2 Pro' }
        ],
        optionPackage: [
          { value: 'GM', text: 'Bye-Bye GM' },
          { value: 'Epic', text: 'Bongkar Epic' },
          { value: 'Mythic', text: 'Road to Mythic' }
        ]
      }
    },
    methods: {
      onSubmit(event) {
        event.preventDefault()
        alert(JSON.stringify(this.form))
      },
    }
  }
</script>

<style>
  .games {
    background: url("../assets/img/bg/games.png");
    margin-top: 60px;
    mask-image: linear-gradient(to bottom, rgba(14,14,14,1) 90%, rgba(14,14,14,0) 100%);
  }

  .games h5, .games h4, p {
    color: var(--white);
  }

  .games h4{
    font-family: 'RobotoBold';
    margin: 36px 12px 0px 12px;
  }

  .games h5 {
    font-family: 'RobotoMedium';
    height: 48px;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .games p {
    font-family: 'RobotoRegular';
    text-align: justify;
    text-justify: inter-word;
    margin-bottom: 120px;
  }

  .game-container {
    margin-top: 96px;
    
  }

  .games img {
    max-height: 60px;
  }

  .games .btn {
    background: transparent;
    border: none;
  }

  .list-game .position-absolute {
    top: -60px;
    z-index: -1;
    max-height: 120%;
    left: -120px;
  }

  .list-game .btn {
    padding: 0;
    margin: 3px 0px;
  }

  #game-option-mobile-legend {
    border-right: 6px solid var(--orange);
  }

  .option-transaction .btn {
    height: 120px;
    border-bottom: 3px solid var(--orange);
    margin: 24px 12px;
  }

  .option-transaction img {
    margin: 0px 24px 12px 24px;
  }

  .games #order {
    border: 1px solid var(--orange);
    background: var(--orange);
    height: fit-content;
    padding: 9px 36px;
    margin-top: 120px;
    margin-bottom: 120px;
  }

  .modal-header, .modal-footer {
    border: none;
  }

  .modal-content {
    font-family: 'RobotoMedium';
    background: url("../assets/img/bg/transaction.png");
    background-size: cover;
    color: var(--white);
    border-radius: 12px;
    padding: 0px 12px 12px 12px;
  }

  .modal-content label {
    margin-bottom: 12px;
  }

  #input-group-service {
    margin-top: 24px;
  }

  .modal-header {
    padding-top: 36px;
  }
  .modal-footer {
    align-self: center;
    padding-bottom: 24px;
  }

  .modal-footer .btn-primary {
    background: var(--orange);
  }
</style>
