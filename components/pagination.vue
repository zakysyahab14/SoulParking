<template>
  <no-ssr>
  <div>
                  <div>
                <b-list-group :flush="true" >

                    <li v-for="course in courseDataFilter" :key="course.id" class="list-group-item px-0">
                        <b-card no-body class="pl-0 pr-0 cardPerson" style="width:100%">
                    
                    <div class="media flex-wrap">
                        <div class="d-sm-block">
                            <img :src="`img/bg/${course.image}`" class="mt-4 gaskirImage" style="width:70px; height:70px; borderRadius:50%" />
                        </div>
                        <div class="media-body ml-xl-4 gaskirData">
                        <h5 class="mb-1 pt-2">
                            <a href="javascript:void(0)" class="text-dark name">{{course.title}}</a>
                        </h5>
                        <div class="d-flex flex-wrap align-items-center mb-1">
                            <img src="img/mobile-app.png" class="mr-2" style="width:18px; height:20px">
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
                <b-pagination
                    v-model="currentPage"
                    :total-rows="rows"
                    :per-page="perPage"
                    />
                  </div>
    
  </div>
  </no-ssr>
</template>

<script>

export default {

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
    .name {
        font-size: 14px;
    }
    .number {
        font-size: 11px;
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
    @media screen and (max-width: 768px) {
  .gaskirImage {
            margin-left: 85%;
        }
        .gaskirData {
            margin-left: 15%;
        }
}
    @media screen and (max-width: 425px) {
        .gaskirImage {
            margin-left: 85%;
        }
        .gaskirData {
            margin-left: 25%;
        }
}
@media screen and (max-width: 374px) {
        .gaskirImage {
            margin-left: 20%;
        }
        .gaskirData {
            margin-left: 15%;
        }
}
</style>