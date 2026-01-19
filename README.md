<link rel="manifest" href="manifest.json">
<meta name="theme-color" content="#0d0d0d">
<link rel="apple-touch-icon" href="icon-192.png">

<script>
  if ('serviceWorker' in navigator) {
    window.addEventListener('load', () => {
      navigator.serviceWorker.register('sw.js');
    });
  }
</script>
