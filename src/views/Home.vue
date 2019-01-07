<template>
    <main role="main" class="  pt-3 px-4">
      <div class="d-flex justify-content-between flex-wrap flex-md-nowrap align-items-center pb-2 mb-3 border-bottom">
        <h1 class="h2">Dashboard</h1>
        <div class="btn-toolbar mb-2 mb-md-0"></div>
      </div>
        <div class="row">
            <div class="col">
              <VueApexCharts 
                  type="donut" 
                  :options="chartOptions"
                  :series="series"
                  width="450"
              >
              </VueApexCharts>
            </div>
            <div class="col">
                <div class="card">
                  <div class="card-body">
                    <h5 class="card-title">Hoje</h5>
                    <p class="card-text">R$ 1000,00</p>
                  </div>
                </div>
            </div>
            <div class="col">
                <div class="card" >
                  <div class="card-body">
                    <h5 class="card-title">Lucro</h5>
                    <p class="card-text"> R$ 1000,00</p>
                  </div>
                </div>
            </div>
        </div>
    </main>
</template>

<script>
import VueApexCharts from 'vue-apexcharts'

export default {
  name: 'home',
  components:{VueApexCharts},
  data() {
        return {
            series: [44, 55, 13, 43, 22],
            chartOptions: {
                labels: ['Team A', 'Team B', 'Team C', 'Team D', 'Team E'],
            }
        }
  }

}
</script>
