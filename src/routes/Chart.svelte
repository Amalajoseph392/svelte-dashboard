
<script>
  import { onMount } from 'svelte';
  import Chart from 'chart.js/auto';

  let ctx;
  let chartData = [6356, 6218, 6156, 6526, 6356, 6256, 6056];
  let labels = ['01 Feb', '02 Feb', '03 Feb', '04 Feb', '05 Feb', '06 Feb', '07 Feb'];

  /**
   * @type {Chart<"line", number[], string>}
   */
  let chart; // Store the chart instance

  onMount(async () => {
    const canvas = document.getElementById('myChart');
    chart = new Chart(canvas, {
      type: 'line',
      data: {
        labels: labels,

        
        datasets: [
          {
            
            data: chartData,
            
            borderColor: ['#0694a2'],
            borderWidth: 4,
            tension: 0.3,
            radius: 5,
            pointHoverRadius: 8,
            fill: true,
            backgroundColor: '#bce2ea'
          },
        ],
      },
      options: {
        responsive: true, // Enable responsiveness
        scales: {
          x: {
            grid: { display: false },
          },

          y: {
            grid: { display: false },
          },
        },
      },
    });

    // Add a window resize event listener to update the chart when the screen size changes
    const handleResize = () => {
      chart.resize();
    };

    window.addEventListener('resize', handleResize);
    return () => {
      window.removeEventListener('resize', handleResize); // Clean up the event listener on unmount
    };
  });
</script>

<main>
  <div class="flex justify-center items-center ml-[50px] mt-10">
    <canvas
      id="myChart"
      
      bind:this={ctx}
      width="800"
      height="350"
     
    ></canvas>
  </div>
</main>
