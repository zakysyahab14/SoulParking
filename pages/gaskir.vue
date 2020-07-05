<template>
  <no-ssr>
  <div>
      <div class="responsiveText">
      <span class="titlePage">Tambah Petugas Parkir</span>
      </div>
      <b-row>
          <b-col sm="12" md="3" xl="3" class="listCard">
              <b-card>
                  <div class="responsiveText">
                  <b>List Petugas Parkir</b>
                  </div>
                  <div class="webView">
                <b-list-group :flush="true" >

                    <li v-for="course in courseData" :key="course.id" class="list-group-item px-0">
                        <b-card no-body class="pl-0 pr-0 cardPerson" style="width:100%">
                    
                    <div class="media flex-wrap">
                        <div class="d-sm-block">
                            <img :src="`img/bg/${course.image}`" class="mt-xl-4 ml-xl-3 ml-1 mr-1 mt-5 imageGaskir" />
                        </div>
                        <div class="media-body ml-xl-4">
                        <h5 class="mb-1 pt-2">
                            <a href="javascript:void(0)" class="text-dark name">{{course.title}}</a>
                        </h5>
                        <div class="d-flex flex-wrap align-items-center mb-1">
                            <img src="img/mobile-app.png" class="mr-xl-2 imageMobile">
                            <div class="text-muted small number">
                            <span>{{course.Number}}</span>
                            </div>
                            
                        </div>
                        <div class="mt-1 mb-4">  
                            <div v-for="(item, index) in course.state" :key="index" class="button">
                                <b-form-checkbox
                                :id="item.title"
                                v-model="item.status"
                                value="Aktif"
                                unchecked-value="Tidak Aktif"
                                color="success"
                                style="borderRadius:50%"
                                >
                                <span class="text-muted small number">{{ item.status }}</span>
                                </b-form-checkbox>
                            </div>
                        </div>
                        </div>
                    </div>
                        </b-card>
                    </li>
                </b-list-group>
                  </div>
                  <div class="responsive">
                      <pagination />
                  </div>
                </b-card>
          </b-col>
          <b-col sm="12" md="9" xl="9">
              <b-card class="pt-0">
                  <div class="responsiveText">
              <span style="fontSize:18px; fontWeight:600">Upload Dokumen Data Diri</span>
                  </div>
                  <b-row>
                      <b-col md="5">
                        <b-card>
                            <upload />
                        </b-card>
                      </b-col>
                      <b-col md="2">
                        
                      </b-col>
                      <b-col md="5">
                          <b-card>
                            <uploadPhoto />
                        </b-card>
                      </b-col>
                  </b-row>
                  <b-row>
                        <b-col>
                            <formGaskir />
                        </b-col>
                  </b-row>
              </b-card>
          </b-col>
      </b-row>
      
    
  </div>
  </no-ssr>
</template>

<script>
import upload from '~/components/upload.vue'
import uploadPhoto from '~/components/uploadPhoto.vue'
import formGaskir from '~/components/form.vue'
import pagination from '~/components/pagination.vue'


export default {
    components: {
    upload,
    uploadPhoto,
    formGaskir,
    pagination
  },
  data: () => ({
      currentPage: 1,
      perPage:3,
    courseData: [{
        id: 1,
      image: '1.jpg',
      title: 'Aba',
      Number: '+62811223344',
      state: [{ 
          status: 'Tidak Aktif' }],
    }, {
        id: 2,
      image: '2.jpg',
      title: 'Ibi',
      Number: '+62811223344',
      state: [{ 
          status: 'Tidak Aktif' }],
    }, {
        id: 3,
      image: '3.jpg',
      title: 'Ubu',
      Number: '+62811223344',
      state: [{ 
          status: 'Tidak Aktif' }],  
    }, {
        id: 4,
      image: '4.jpg',
      title: 'Obo',
      Number: '+62811223344',
      state: [{ 
          status: 'Tidak Aktif' }],  
    }, {
        id: 5,
      image: '5.jpg',
      title: 'Ebe',
      Number: '+62811223344',
      state: [{ 
          status: 'Tidak Aktif' }],  
    }, {
        id: 6,
      image: '6.jpg',
      title: 'Odo',
      Number: '+62811223344',
      state: [{ 
          status: 'Tidak Aktif' }],  
    }]
  }),
methods: {
 
    },
  computed: {
      rows() {
        return this.courseData.length
      },
     courseDataFilter: function () {
    return this.courseData.slice((this.currentPage - 1) * this.perPage,
        this.currentPage * this.perPage
      )
  }
  },
    
}
</script>

<style>
.v-main {
        background-color: rgba(175, 175, 175, 0.377);
    }
    .button .active {
        color: white!important;
        background-color: green;
        border-color: white;
    }
    .custom-checkbox .custom-control-input:checked ~ .custom-control-label::after {
        background-color: green!important;
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
    .listCard {
        height:100vh; 
        overflow-Y:scroll
    }
    .name {
        font-size: 2vh;
    }
    .imageGaskir {
        width:8vh; 
        height:8vh; 
        border-Radius:50%
    }
    .imageMobile {
        width:18px; 
        height:20px
    }
    .number {
        font-size: 1.5vh;
    }
    .list-group-item {
        border: none;
    }
    .cardPerson {
        box-shadow: 1px 8px 20px #c2c1c181;
    }
    .titlePage {
        font-size: 24px;
        font-weight: 500;
    }
    .responsive {
        display: none;
    }
    @media screen and (max-width: 1024px) {
        .imageGaskir {
        width:6vh; 
        height:6vh; 
        border-Radius:50%
        }
        .name {
            font-size: 1.5vh;
        }
        .imageMobile {
        width:15px; 
        height:17px;
        margin-right:0
    }
    }
    @media screen and (max-width: 768px) {
  .webView {
      display: none;
  }
  .responsive {
      display: block;
  }
  .responsiveText {
      text-align: center;
  }
  .listCard {
        height:100%; 
    }
}
@media screen and (max-width: 425px) {

}

</style>