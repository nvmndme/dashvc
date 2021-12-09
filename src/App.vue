<template>
  <Header msg="PT. Sukamaju"/>
  <Chart id="Chart" v-bind:chartData="this.state.chartData" v-bind:chartOptions="this.state.chartOptions" />
</template>

<script>
import Header from './components/Header'
import { defineComponent } from 'vue'
import Chart from './components/Chart'

export default defineComponent({
  name: 'App',
  components: {
    Header, Chart
  },
  data () {
    return {
      state: {
        chartData: {
          datasets: [
            {
              label: 'HS Code',
              data: [{x: -10,y: 0}, {x: 0,y: 10}, {x: 10,y: 5}, {x: 0.5,y: 5.5}],
              backgroundColor: 'rgb(255, 99, 132)'
            }
          ],
        },
        chartOptions: {
          responsive: false
        }
      }
    }
  }
})
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #2c3e50;
  margin-top: 20px;
  margin-left: 50px;
}

#Chart {
  border:2px;
  border-style:solid;
  border-color: rgb(165, 165, 165);
  width: min-content;
}

</style>
