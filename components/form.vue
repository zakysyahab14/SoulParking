<template>
    <div>
    <div class="responsiveText">
        <p style="fontSize:18px; fontWeight:600">Informasi Petugas Parkir</p>
    </div>
  <div role="group" class="grupInput">
      <b-card no-body>
      <b-row>
          <b-col md="6" class="formPost pb-xl-2 pb-0">
            <label for="inputNama" class="titleForm mb-0">Nama Petugas Parkir</label>
                <b-form-input
                id="inputNama"
                v-model="name"
                :state="nameState"
                aria-describedby="input-live-help input-live-feedback"
                placeholder="Masukan Nama Petugas"
                size="sm"
                class="mb-2"
                trim
                ></b-form-input>

                <label for="inputNik" class="titleForm mb-0">NIK</label>
                <b-form-input
                id="inputNik"
                type="number"
                v-model="nik"
                :state="nikState"
                placeholder="Masukan Nomor Induk"
                size="sm"
                class="mb-2"
                trim
                ></b-form-input>

                <label for="inputNo" class="titleForm mb-0">No. Telepon</label>
                <b-form-input
                id="inputNo"
                type="number"
                v-model="nomor"
                :state="noState"
                placeholder="Masukan Nomor Telepon"
                size="sm"
                class="mb-xl-2 mb-2"
                trim
                ></b-form-input>
          </b-col>
          <b-col md="6" class="formPost pt-xl-2 pt-sm-3 pt-0">
            <label for="inputUser" class="titleForm mb-0">Username</label>
                <b-form-input
                id="inputUser"
                v-model="user"
                placeholder="Masukan Username"
                size="sm"
                class="mb-2"
                trim
                ></b-form-input>

                <label for="inputPassword" class="titleForm mb-0">Password</label>
                <b-form-input
                id="inputPassword"
                type="password"
                v-model="password"
                :state="passwordState"
                placeholder="Masukan Password"
                size="sm"
                class="mb-2"
                trim
                ></b-form-input>

                <label class="titleForm mb-0">Aktif</label>
                    <v-checkbox
                    id="checkAktif"
                    color="orange"
                    size="sm"
                    style="marginTop: 0"
                    hide-details
                    ></v-checkbox>
                </b-col>
            </b-row>
            </b-card>
        </div>
        <div>
            <b-button variant="warning" @click="modalaskbanner" type="submit" class="float-right ml-5" size="sm" style="marginTop: 15px; width: 80px"><span style="color:white; fontSize: 12px; fontWeight:500">Simpan</span></b-button>
            <b-button variant="outline-danger" type="submit" href="/dashboard" class="float-right mr-5" size="sm" style="marginTop: 15px; width: 80px"><span style="color:red; fontSize: 12px; fontWeight:500">Batal</span></b-button>
        </div>
        <b-modal id="modal-ask" ref="modal-ask-banner" centered hide-footer hide-header>
        <button
          type="button"
          aria-label="Close"
          class="close"
          @click="modalaskclosebanner"
        >
          ×
        </button>
        <div class="my-4">
          <div class="mt-3" style="text-align: center;">
            <p style="font-size: 18px; font-weight: bold; color: #000000;">
              Are you sure want to submit?
            </p>
            <div class="pt-5" style="display: flex; justify-content: space-evenly;">
              <button class="btn btn-outline-danger" @click.prevent="modalaskclosebanner">
                CANCEL
              </button>
              <button class="btn btn-outline-success" @click="submitform">
                SUBMIT
              </button>
            </div>
          </div>
        </div>
      </b-modal>
    </div>
</template>

<script>
  export default {
    computed: {
      nameState() {
      },
      nikState() {
      },
      noState() {
      },
      passwordState() {
      }
    },
    data() {
      return {
        name: '',
        nik: null,
        nomor: null,
        user: '',
        status: false,
        password: ''
      }
    },
    methods: {
        modalaskbanner () {
            this.$refs['modal-ask-banner'].show()
    },
        modalaskclosebanner () {
            this.$refs['modal-ask-banner'].hide()
    },
        submitform () {
            this.$toast.success('succes menambah petugas parkir')
            location.reload()
        }
    }
  }
</script>

<style>
 .titleForm {
     font-size: 13px;
     font-weight: 500;
 }
 .formPost {
     padding-left: 30px!important;
 }
 ::-webkit-input-placeholder {
   font-size: 12px;
}
.custom-checkbox .yellowCheck .custom-control-input:checked ~ .custom-control-label::after  {
        background-color: yellow!important;
        border-radius: 50%;
    }
    .custom-checkbox .custom-control-label::before {
        background: url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' width='8' height='8' viewBox='0 0 8 8'%3e%3cpath fill='%23fff' d='M6.564.75l-3.59 3.612-1.538-1.55L0 4.26l2.974 2.99L8 2.193z'/%3e%3c/svg%3e") no-repeat 50% / 50% 50%;
        background-color: rgba(161, 159, 159, 0.74);
        position: absolute;
        top: 0.25rem;
        left: -1.5rem;
        display: block;
        width: 1rem;
        height: 1rem;
    }
    .custom-checkbox .custom-control-label::before {
        border-radius: 1rem
    }
    @media screen and (max-width: 425px) {
        .responsiveText {
            text-align: center;
        }

}
</style>