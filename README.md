<link rel="manifest" href="manifest.json" crossorigin="use-credentials">
<meta name="theme-color" content="#0d0d0d">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<script>
  if ('serviceWorker' in navigator) {
    window.addEventListener('load', () => {
      navigator.serviceWorker.register('./sw.js', { scope: './' })
        .then(reg => console.log('CrossPoint PWA Active:', reg.scope))
        .catch(err => console.error('PWA Registration Failed:', err));
    });
  }
</script>
