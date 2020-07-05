<template>
    <no-ssr>
    <div> 
    <b-container fluid class="containerClass">
        <b-row>
            <b-col md="6" lg="3" xl="3">
                <v-card class="d-inline-block mx-auto" style="width:100%">
                    <v-container class="mb-0 pb-0 px-0 pt-0 style">
                    <v-row justify="space-around" class="mb-0">
                        <v-col
                        cols="auto"
                        class="text-center pl-3 py-0"
                        >
                        <v-row
                            class="flex-column ma-0 fill-height"
                            justify="center"
                        >
                            <v-col class="textTop text-muted">
                            <b>KEDATANGAN</b>
                            </v-col>
                            <v-col class="textBtm">
                            2500
                            </v-col>
                        </v-row>
                        </v-col>
                        <v-col cols="auto" class="mr-3">
                        <img
                            height="80"
                            width="80"
                            src="img/arrow.png"
                        >
                        </v-col>
                        
                    </v-row>
                    <v-divider class="mb-0 mt-0"></v-divider>
                    <div class="persen pb-1 pt-1" v-bind:style="[percent[0] > 0 ? {color:`green`} : {color:`red`}]">
                        <div v-if="percent[0] > 0">
                            <b>+{{percent[0]}}%</b> dari minggu lalu
                        </div>
                        <div v-else>
                            <b>{{percent[0]}}%</b> dari minggu lalu
                        </div>
                    </div>
                    </v-container>
                </v-card>
            </b-col>
            <b-col md="6" lg="3" xl="3">
                <v-card class="d-inline-block mx-auto" style="width:100%">
                    <v-container class="mb-0 pb-0 px-0 pt-0 style">
                    <v-row justify="space-around" class="mb-0">
                        <v-col
                        cols="auto"
                        class="text-center pl-3 py-0"
                        >
                        <v-row
                            class="flex-column ma-0 fill-height"
                            justify="center"
                        >
                            <v-col class="textTop text-muted">
                            <b>PJP LAMA</b>
                            </v-col>
                            <v-col class="textLama">
                            2000
                            </v-col>
                        </v-row>
                        </v-col>
                        <v-col cols="auto" class="mr-3">
                        <img
                            height="80"
                            width="80"
                            src="img/refresh.png"
                        >
                        </v-col>
                        
                    </v-row>
                    <div class="persen pb-1 pt-1" v-bind:style="[percent[1] > 0 ? {color:`green`} : {color:`red`}]">
                        <div v-if="percent[1] > 0">
                            <b>+{{percent[1]}}%</b> dari minggu lalu
                        </div>
                        <div v-else>
                            <b>{{percent[1]}}%</b> dari minggu lalu
                        </div>
                    </div>
                    </v-container>
                </v-card>
            </b-col>
            <b-col md="6" lg="3" xl="3">
                <v-card class="d-inline-block mx-auto" style="width:100%">
                    <v-container class="mb-0 pb-0 px-0 pt-0 style">
                    <v-row justify="space-around" class="mb-0">
                        <v-col
                        cols="auto"
                        class="text-center pl-3 py-0"
                        >
                        <v-row
                            class="flex-column ma-0 fill-height"
                            justify="center"
                        >
                            <v-col class="textTop text-muted">
                            <b>PJP BARU </b>
                            </v-col>
                            <v-col class="textBaru">
                            500
                            </v-col>
                        </v-row>
                        </v-col>
                        <v-col cols="auto" class="mr-3">
                        <img
                            height="80"
                            width="80"
                            src="img/group.png"
                        >
                        </v-col>
                        
                    </v-row>
                    <v-divider class="mb-0 mt-0"></v-divider>
                    <div class="persen pb-1 pt-1" v-bind:style="[percent[2] > 0 ? {color:`green`} : {color:`red`}]">
                        <div v-if="percent[2] > 0">
                            <b>+{{percent[2]}}%</b> dari minggu lalu
                        </div>
                        <div v-else>
                            <b>{{percent[2]}}%</b> dari minggu lalu
                        </div>
                    </div>
                    </v-container>
                </v-card>
            </b-col>
            <b-col md="6" lg="3" xl="3">
                <v-card class="d-inline-block mx-auto" style="width:100%">
                    <v-container class="mb-0 pb-0 px-0 pt-0 style">
                    <v-row justify="space-around" class="mb-0">
                        <v-col
                        cols="auto"
                        class="text-center pl-3 py-0"
                        >
                        <v-row
                            class="flex-column ma-0 fill-height"
                            justify="center"
                        >
                            <v-col class="textTop text-muted">
                            <b>KELUAR </b>
                            </v-col>
                            <v-col class="textKeluar">
                            1500
                            </v-col>
                        </v-row>
                        </v-col>
                        <v-col cols="auto" class="mr-3">
                        <img
                            height="80"
                            width="80"
                            src="img/switch.png"
                        >
                        </v-col>
                        
                    </v-row>
                    <v-divider class="mb-0 mt-0"></v-divider>
                    <div class="persen pb-1 pt-1" v-bind:style="[percent[3] > 0 ? {color:`green`} : {color:`red`}]">
                        <div v-if="percent[3] > 0">
                            <b>+{{percent[3]}}%</b> dari minggu lalu
                        </div>
                        <div v-else>
                            <b>{{percent[3]}}%</b> dari minggu lalu
                        </div>
                    </div>
                    </v-container>
                </v-card>
            </b-col>
        </b-row>

        <b-row>
                <div class="col-sm-6">
                    <b-card no-body>
                    <b-card-body class="pb-0">
                        <div class="text-muted small mb-3 responsiveText1"><b>TOTAL PEMASUKAN</b></div>
                        <div class="webView">
                            <div class="float-right persen2" v-bind:style="[percent[4] > 0 ? {color:`green`} : {color:`red`}]">
                            <div v-if="percent[4] > 0">
                                <b>+{{percent[4]}}%</b> dari minggu lalu
                            </div>
                            <div v-else>
                                <b>{{percent[4]}}%</b> dari minggu lalu
                            </div>
                            </div>
                        </div>
                        <div class="text-xlarge responsiveText" style="fontSize:24px"><b>RP 1.500.000</b></div>
                        
                    </b-card-body>
                    <div class="px-2">
                        <dashboard1-chart3 class="w-100" :height="170" />
                    </div>
                    <div class="responsive">
                    <v-divider class="mb-0 mt-5"></v-divider>
                        <div class="persen2 pb-1 pt-1" v-bind:style="[percent[4] > 0 ? {color:`green`} : {color:`red`}]">
                            <div v-if="percent[4] > 0">
                                <b>+{{percent[4]}}%</b> dari minggu lalu
                            </div>
                            <div v-else>
                                <b>{{percent[4]}}%</b> dari minggu lalu
                            </div>
                        </div>
                    </div>
                    </b-card>
                </div>

            <div class="col-sm-6">
                    <b-card no-body class="mb-4">
                    <b-card-body class="pb-0">
                        <div class="text-muted small mb-3 responsiveText1"><b>MEMBERSHIP</b></div>
                        <div class="webView">
                            <div class="float-right persen2" v-bind:style="[percent[5] > 0 ? {color:`green`} : {color:`red`}]">
                            <div v-if="percent[5] > 0">
                                <b>+{{percent[5]}}%</b> dari minggu lalu
                            </div>
                            <div v-else>
                                <b>{{percent[5]}}%</b> dari minggu lalu
                            </div>
                            </div>
                        </div>
                        <div class="text-xlarge responsiveText" style="fontSize:24px"><b>1.200</b></div>
                        
                    </b-card-body>
                    <div class="px-2">
                        <dashboard1-chart1 class="w-100" :height="170" />
                    </div>
                    <div class="responsive">
                    <v-divider class="mb-0 mt-5"></v-divider>
                        <div class="persen2 pb-1 pt-1" v-bind:style="[percent[5] > 0 ? {color:`green`} : {color:`red`}]">
                            <div v-if="percent[5] > 0">
                                <b>+{{percent[5]}}%</b> dari minggu lalu
                            </div>
                            <div v-else>
                                <b>{{percent[5]}}%</b> dari minggu lalu
                            </div>
                        </div>
                    </div>
                    </b-card>
                </div>
        </b-row>
        <!-- done resp -->
        <b-row>
                <div class="col-sm-6 webView">
                    <b-card no-body class="mb-4">
                        <div class="centerText mt-2">
                        <div class="persen3">Cash</div>
                        <div class="textBtm2">800</div>
                        </div>
                    <b-card-body class="pb-0 pt-0">
                        <div class="text small mb-3"><b>METODE PEMBAYARAN</b></div>
                        <div>
                            <img src="#" class="rounded float-left dougText" width="15px" height="15px" style="backgroundColor:green" alt="">
                            <div class="float-left dougText pl-2">CASH</div>
                            <img src="#" class="rounded float-left ml-5 dougText" width="15px" height="15px" style="backgroundColor:#36A2EB" alt="">
                            <div class="float-left dougText pl-2">GO-PAY</div>
                            <img src="#" class="rounded float-left ml-5 dougText" width="15px" height="15px" style="backgroundColor:#FFCE56" alt="">
                            <div class="float-left dougText pl-2">MEMBERSHIP</div>
                        </div>
                    </b-card-body>
                    <div class="px-2 pb-5">
                        <vue-chartjs :height="160" />
                    </div>
                    </b-card>
                </div>

                <div class="col-sm-6 responsive">
                    <b-card no-body class="mb-4">
                        <div class="text large text-center mt-3 mb-2"><b>METODE PEMBAYARAN</b></div>
                        <b-row class="text-left" align-h="start">
                            <b-col cols="5" xl="4" class="pt-0 pr-0">
                                <b-card-body class="pb-0 pt-0 pr-0">
                                    <div class="mt-5">
                                        <img src="#" class="rounded float-left mr-1 dougText" width="15px" height="15px" style="backgroundColor:green" alt="">
                                        <div class="dougText mt-5 ml-3">CASH</div>
                                        <img src="#" class="rounded float-left mr-1 mt-2 dougText" width="15px" height="15px" style="backgroundColor:#36A2EB" alt="">
                                        <div class="dougText mt-2 ml-3">GO-PAY</div>
                                        <img src="#" class="rounded float-left mr-1 mt-2 dougText" width="15px" height="15px" style="backgroundColor:#FFCE56" alt="">
                                        <div class="dougText mt-2 ml-3">MEMBERSHIP</div>
                                        
                                    </div>
                                </b-card-body>
                            </b-col>
                            <b-col cols="7" xl="6" class="pl-0 pt-0 pb-0">
                                <div class=" inline">
                        <vue-chartjs :height="260" />
                    </div>
                            </b-col>
                        </b-row>
                        <v-divider class="mb-0 mt-5"></v-divider>
                    <div class="persen pb-1 pt-1" v-bind:style="[percent[6] > 0 ? {color:`green`} : {color:`red`}]">
                        <div v-if="percent[6] > 0">
                            <b>+{{percent[6]}}%</b> dari minggu lalu
                        </div>
                        <div v-else>
                            <b>{{percent[6]}}%</b> dari minggu lalu
                        </div>
                    </div>
                    </b-card>
                </div>

                <div class="col-sm-6 responsive">
                    <b-card no-body class="mb-4">
                        <div class="text large text-center mt-3 mb-2"><b>TRAFIK SITUS</b></div>
                        <b-row class="text-left" align-h="start">
                            <b-col cols="5" xl="4" class="pt-0 pr-0">
                                <b-card-body class="pb-0 pt-0 pr-0">
                                    <div class="mt-5">
                                        <img src="#" class="rounded float-left mr-1 dougText" width="15px" height="15px" style="backgroundColor:green" alt="">
                                        <div class="dougText mt-5 ml-1">Organic Search </div>
                                        <img src="#" class="rounded float-left mr-1 mt-2 dougText" width="15px" height="15px" style="backgroundColor:#36A2EB" alt="">
                                        <div class="dougText mt-2 ml-1">Direct</div>
                                        <img src="#" class="rounded float-left mr-1 mt-2 dougText" width="15px" height="15px" style="backgroundColor:#FFCE56" alt="">
                                        <div class="dougText mt-2 ml-1">Social</div>
                                        <img src="#" class="rounded float-left mr-1 mt-2 dougText" width="15px" height="15px" style="backgroundColor:rgba(49, 45, 45, 0.637)" alt="">
                                        <div class="dougText mt-2 ml-1">Other</div>
                                    </div>
                                </b-card-body>
                            </b-col>
                            <b-col cols="7" xl="6" class="pl-0 pt-0 pb-0">
                                <div class=" inline">
                        <vue-chart2 :height="125" />
                    </div>
                            </b-col>
                        </b-row>
                        <v-divider class="mb-0 mt-5"></v-divider>
                    <div class="persen pb-1 pt-1" v-bind:style="[percent[7] > 0 ? {color:`green`} : {color:`red`}]">
                        <div v-if="percent[7] > 0">
                            <b>+{{percent[7]}}%</b> dari minggu lalu
                        </div>
                        <div v-else>
                            <b>{{percent[7]}}%</b> dari minggu lalu
                        </div>
                    </div>
                    </b-card>
                </div>

            <div class="col-sm-6 webView">
                    <b-card no-body class="mb-4">
                        <b-row class="text-left" align-h="start">
                            <b-col md="4" class="pt-0 pr-0">
                                <b-card-body class="pb-0 pt-0">
                        <div class="text small mb-3"><b>TRAFIK SITUS</b></div>
                        <div>
                            <img src="#" class="rounded float-left mr-3 dougText" width="15px" height="15px" style="backgroundColor:green" alt="">
                            <div class="dougText mt-2 ml-3">Organic Search</div>
                            <img src="#" class="rounded float-left mr-3 mt-2 dougText" width="15px" height="15px" style="backgroundColor:#36A2EB" alt="">
                            <div class="dougText mt-2 ml-3">Direct</div>
                            <img src="#" class="rounded float-left mr-3 mt-2 dougText" width="15px" height="15px" style="backgroundColor:#FFCE56" alt="">
                            <div class="dougText mt-2 ml-3">Social</div>
                            <img src="#" class="rounded float-left mr-3 mt-2 dougText" width="15px" height="15px" style="backgroundColor:rgba(49, 45, 45, 0.637)" alt="">
                            <div class="dougText mt-2 ml-3">Other</div>
                        </div>
                    </b-card-body>
                            </b-col>
                            <b-col md="6" class="pl-0">
                                <div class="px-2 inline">
                        <vue-chart2 :height="210" />
                    </div>
                            </b-col>
                        </b-row>
                    
                    
                    </b-card>
                </div>
        </b-row>
    </b-container>
</div>
    </no-ssr>
</template>

<script>
// import Logo from '~/components/Logo.vue'
import Vue from 'vue'
import VueChartJs from 'vue-chartjs'
import 'chart.piecelabel.js';


Vue.component('dashboard1-chart3', {
  extends: VueChartJs.Bar,
  mounted () {
    this.renderChart({
      datasets: [{
        data: [350000, 1000000, 1250000, 1125000, 1000000, 1400000, 500000, 1200000, 300000, 800000, 1000000, 1500000
        ],
        dataLabel: '350K',
        borderWidth: 0,
        maxBarThickness:30,
        backgroundColor: 'rgb(0, 153, 255)',
      }],
      labels: ['JAN', 'FEB', 'MAR', 'APR', 'MEI', 'JUN', 'JUL', 'AGU', 'SEP', 'OKT', 'NOV', 'DEC'],
    }, {
      scales: {
        xAxes: [{
          display: true,
          gridLines: {
			display: false
			}
        }],
        yAxes: [{
          display: true,
          gridLines: {
            display: true,

			},
            ticks: {
                max: 1500000,
                stepSize: 375000,
                min: 0,
                callback: function(value, index, values) {
                        return value / 1000 + 'k';
                    }
						},
        }]
      },
      legend: {
        display: false
      },
      responsive: true,
      maintainAspectRatio: true
    })
  }
})

Vue.component('dashboard1-chart1', {
  extends: VueChartJs.Bar,
  mounted () {
    this.renderChart({
      datasets: [{
        data: [350, 1000, 1250, 1125, 1000, 1400, 500, 1200, 300, 800, 1000, 1500
        ],
        borderWidth: 0,
        maxBarThickness:30,
        backgroundColor: 'rgb(0, 153, 255)',
      }],
      labels: ['JAN', 'FEB', 'MAR', 'APR', 'MEI', 'JUN', 'JUL', 'AGU', 'SEP', 'OKT', 'NOV', 'DEC'],
    }, {
      scales: {
        xAxes: [{
          display: true,
          gridLines: {
			display: false
			}
        }],
        yAxes: [{
          display: true,
          gridLines: {
            display: true,

			},
            ticks: {
                max: 1200,
                stepSize: 300,
                min: 0,
						},
        }]
      },
      legend: {
        display: false
      },
      responsive: true,
      maintainAspectRatio: true
    })
  }
})
Chart.defaults.global.legend.display = false;
Vue.component('vue-chartjs', {
  extends: VueChartJs.Doughnut,
  mounted () {
    this.renderChart({
        labels: ['GO-PAY', 'CASH', 'MEMBERSHIP'],
        datasets: [{
        data: [ 800, 800, 525 ],
        backgroundColor: [ '#36A2EB', 'green', '#FFCE56' ],
        hoverBackgroundColor: [ '#36A2EB', 'green', '#FFCE56' ],
        responsive: false,
              maintainAspectRatio: false,

      }],
      options: {
          label: {
              display: false
          }
      }
    })
  }
})

Vue.component('vue-chart2', {
  extends: VueChartJs.Pie,
    mounted () {
    this.renderChart({
      labels: ['Direct', 'Organic Search', 'Social', 'Other'],
      datasets: [
        {
          backgroundColor: [
            '#36A2EB',
            'green',
            '#FFCE56',
            'rgba(49, 45, 45, 0.637)'
          ],
          data: [250, 100, 550, 100]
        }
      ]
    }, {
      maintainAspectRatio: false,
      pieceLabel: {
        render: 'percentage',
        precision: 1,
        fontColor: 'white',
        overlap: true
      }
    }
    )}
})
 
export default {
    data() {
        return{
            percent: [ +30, 25, -25, -20, 30, -10, 30, 30]
        }
    },
    percent: null,
  components: {
    // Logo,
  },
}
</script>

<style>
    .v-main {
        background-color: rgba(211, 211, 211, 0.637);
    }
    .textTop {
        font-size: 16px;
        text-align: left;
    }
    .textBtm {
        font-size: 24px;
        color: green;
        text-align: left;
        font-weight: bold;
    }
    .textBtm2 {
        font-size: 30px;
        color: green;
        text-align: center;
        font-weight: bold;
    }
    .persen3 {
        font-size: 20px;
        color: green;
        text-align: center;
        font-weight: bold;
    }
    .textLama {
        font-size: 24px;
        color: purple;
        text-align: left;
        font-weight: bold;
    }
    .textBaru {
        font-size: 24px;
        color: blue;
        text-align: left;
        font-weight: bold;
    }
    .textKeluar {
        font-size: 24px;
        color: red;
        text-align: left;
        font-weight: bold;
    }
    .persen {
        font-size: 10px;
        color: green;
        padding-left: 10px;
        background-color:bisque;
    }
    .persen2 {
        font-size: 10px;
        color: green;
        padding-top: 10px;
    }
    .persen2red {
        font-size: 10px;
        color: red;
        padding-top: 10px;
    }
    .dougText {
        font-size: 10px;
        color: grey;
    }
    .inline {
        display: inline;
    }
    .centerText {
          position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 0
    }
    .style {
        border-radius: 20px;
    }
    .responsive {
        display: none;
    }
    @media screen and (max-width: 1024px) {
  .persen {
    text-align: center;
  }
   .persen2 {
    text-align: center;
  }
  .webView {
      display: none;
  }
  .responsive {
      display: block;
  }
  .responsiveText {
      text-align: center;
  }
  .responsiveText1 {
      text-align: center;
      font-size: 20px;
  }
}
</style>