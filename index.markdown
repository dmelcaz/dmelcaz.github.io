---
layout: home
title: Language
---

<noscript>
  <p>
    <a href="{{ '/en/' | relative_url }}">English</a> · <a href="{{ '/es/' | relative_url }}">Espanol</a>
  </p>
</noscript>

<script>
  (function () {
    var base = "{{ '/' | relative_url }}";
    var stored = localStorage.getItem('site-lang');
    if (stored) {
      window.location.replace(base + stored + '/');
      return;
    }
    var lang = (navigator.language || navigator.userLanguage || 'en').toLowerCase();
    var target = lang.indexOf('es') === 0 ? 'es' : 'en';
    localStorage.setItem('site-lang', target);
    window.location.replace(base + target + '/');
  })();
</script>
