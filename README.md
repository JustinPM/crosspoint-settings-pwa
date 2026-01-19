<script>
  if ('serviceWorker' in navigator) {
    window.addEventListener('load', () => {
      // The {scope: './'} tells the browser this worker 
      // controls everything in this folder and below.
      navigator.serviceWorker.register('./sw.js', {scope: './'})
        .then(reg => {
          console.log('CrossPoint PWA Registered!', reg.scope);
        })
        .catch(err => {
          console.error('PWA Registration Failed:', err);
        });
    });
  }
</script>
