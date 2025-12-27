<script>
  import Chart from 'chart.js/auto';

  let chartData = {
    labels: ['Office Worker', 'Students', 'Others'],
    datasets: [
      { label: 'current peoples', data: [40, 10, 6], borderWidth: 0, hoverOffset: 15},
    ]
  };

  function chartAction(node) {
    const chart = new Chart(node, {
      type: 'doughnut',
      data: chartData,
      options: {
        responsive: true,
        cutout: '50%', 
        
        plugins: {
          legend: {
            position: 'bottom',
            labels: {
                usePointStyle: true,
                padding: 20
            }
          }
        }
       }
    });

    return {
      destroy() {
        chart.destroy();
      }
    };
  }
</script>
<div class="relative w-full aspect-video">
    <canvas use:chartAction></canvas>
</div>