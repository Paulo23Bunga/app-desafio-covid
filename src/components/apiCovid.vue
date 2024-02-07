<template>
  <div>
    <canvas ref="chartCanvas"></canvas>
  </div>
</template>

<script>
import Chart from 'chart.js/auto';


export default {
  data() {
    return {
      countriesData: []
    };
  },
  mounted() {
    fetch("https://covid19-brazil-api.now.sh/api/report/v1/countries", {
      method: "GET"
    })
    .then(response => response.json())
    .then(data => {
      
      // Salvar os dados dos países na variável countriesData
      this.countriesData = data.data;
     // this.countriesData = data.data.filter(country => country.confirmed > 20000000);

      // Ordenar os países de acordo com o número de casos confirmados
     // this.countriesData.sort((a, b) => b.confirmed - a.confirmed);

      
      // Preparar os dados para o gráfico
      const countriesLabels = this.countriesData.map(country => country.country);
      const confirmedCases = this.countriesData.map(country => country.confirmed); 


      
      //console.log(countriesLabels);
      // Criar o gráfico de Barras
      const chartCanvas = this.$refs.chartCanvas;
      new Chart(chartCanvas, {
        type: 'bar',
        data: {
          labels: countriesLabels,
          datasets: [{
            label: 'Casos Confirmados',
            data: confirmedCases,
            backgroundColor: [
              'rgba(75, 192, 192, 0.3)'
            ],
            borderColor: 'rgb(75, 192, 192)',
           
            tension: 0.1
          }]
        },
        options: {
          scales: {
            y: {
              beginAtZero: true
            }
          }
        }
      });
    })
    .catch(error => {
      console.error('Erro ao obter dados:', error);
    });
  }
};
</script>
