<script>
  import { onMount, onDestroy } from 'svelte';
  import Hls from 'hls.js';

  // 🔴 เอาลิงก์ .m3u8 ที่หาเจอมาใส่ตรงนี้
//   let src = 'https://stream1.ioc.pattaya.go.th/live/CC-002.m3u8'; 
  let src = 'https://camerai1.iticfoundation.org/hls/pty74.m3u8'; //ATC4-18 แยกสุขุมวิท-พัทยาเหนือ
  
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

<div class="flex flex-col items-center">
  <h1 class="text-xl font-bold mb-4">CCTV Player (HLS)</h1>
  
  <div class="aspect-video w-full max-w-3xl bg-black rounded-lg overflow-hidden shadow-lg">
    <video 
      bind:this={video} 
      muted 
      autoplay
      class="w-full h-full"
    ></video>
  </div>
</div>