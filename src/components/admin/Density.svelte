<script>
	import Chart from 'chart.js/auto';

	let chartData = {
		labels: ['08:00', '', '', '', '12:00', '', '', '', '16:00', '', '', '', '20:00'],
		datasets: [
			{
				label: 'current peoples',
				data: [8, 12, 4, 15, 20, 30, 34, 15, 8, 18, 25, 10, 6],
				fill: true,
				borderColor: '#3b82f6',
				backgroundColor: 'rgba(59, 130, 245, 0.2)',
				tension: 0.1,
				pointRadius: 0,
				pointHoverRadius: 6
			}
		]
	};

	function chartAction(node) {
		const chart = new Chart(node, {
			type: 'line',
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
						display: false,
						border: {
							display: false
						}
					}
				},
				interaction: {
					mode: 'index',
					intersect: false
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
