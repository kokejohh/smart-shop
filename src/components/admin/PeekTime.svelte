<script>
  import Chart from 'chart.js/auto';

  let chartData = {
    labels: ['08:00', '', '', '', '12:00', '', '', '', '16:00', '', '', '', '20:00'],
    datasets: [
      { label: 'current peoples', data: [8, 12, 4, 15, 20, 30, 34, 15, 8, 18, 25, 10, 6], grouped: false, backgroundColor: '#3b82f6', order: 1, borderRadius: 4},
      { label: 'mean peoples', data: [10, 15, 10, 25, 30, 40, 50, 25, 15, 28, 35, 19, 16], grouped: false, backgroundColor: '#dbeafe', order: 2, borderRadius: 4, hoverBackgroundColor: '#dbeafe' }
    ]
  };

  function chartAction(node) {
    const chart = new Chart(node, {
      type: 'bar',
      data: chartData,
      options: {
        responsive: true,
        plugins: {
            legend: {
                display: false
            }
        },
        scales: {
            x: {
                grid: {
                    display: false
                },
                ticks: {
                  font: {
                    size: 16
                  }  
                }
            },
            y: {
                grid: {
                    display: false,
                },
                border: {
                    display: false
                },
                ticks: {
                    display: false
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