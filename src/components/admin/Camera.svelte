<script>
	import { onMount, onDestroy } from 'svelte';
	import Hls from 'hls.js';

    let {src} = $props();

	let video;
	let hls;

	onMount(() => {
		if (Hls.isSupported()) {
			hls = new Hls();
			hls.loadSource(src);
			hls.attachMedia(video);
			hls.on(Hls.Events.MANIFEST_PARSED, function () {
				video.play();
			});
		} else if (video.canPlayType('application/vnd.apple.mpegurl')) {
			// สำหรับ Safari (ไม่ต้องใช้ Hls.js)
			video.src = src;
			video.addEventListener('loadedmetadata', function () {
				video.play();
			});
		}
	});

	onDestroy(() => {
		if (hls) hls.destroy();
	});
</script>

<video bind:this={video} muted autoplay class="h-full w-full"></video>