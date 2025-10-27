---
permalink: /bot-trap/
layout: none
sitemap: false
robots: noindex
---

<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="robots" content="noindex,nofollow" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>bot trap</title>
</head>
<body>
  <!-- intentionally empty: bot trap page -->
  <script>
  (function(){
    const LOGGER_URL = ""; 
    
    try {
      if (typeof gtag === 'function') {
        gtag('event', 'bot_trap_pageview', {
          method: 'direct_url',
          page_location: location.href,
          non_interaction: true
        });
      }
    } catch(e){ /* ignore */ }

    if (LOGGER_URL) {
      try {
        const payload = JSON.stringify({
          type: 'bot_trap',
          url: location.href,
          ua: navigator.userAgent || null,
          ts: (new Date()).toISOString()
        });
        if (navigator.sendBeacon) {
          const blob = new Blob([payload], { type: 'application/json' });
          navigator.sendBeacon(LOGGER_URL, blob);
        } else {
          fetch(LOGGER_URL, {
            method: 'POST',
            headers: { 'Content-Type': 'application/json' },
            body: payload,
            keepalive: true
          }).catch(()=>{});
        }
      } catch(e){}
    }

  })();
  </script>
</body>
</html>