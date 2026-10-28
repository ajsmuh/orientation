
<script>

    let alpha = $state(null);

    let beta = $state(null);

    let gamma = $state(null);
 
    async function start() {

        if (DeviceOrientationEvent.requestPermission) {

            await DeviceOrientationEvent.requestPermission();

        }
 
        window.addEventListener('deviceorientation', (event) => {

            alpha = event.alpha;

            beta = event.beta;

            gamma = event.gamma;

        });

    }
</script>
 
<h1>Device Orientation</h1>
 
<button onclick={start}>Start</button>
 
<p>Alpha: {alpha}</p>
<p>Beta: {beta}</p>
<p>Gamma: {gamma}</p>

 