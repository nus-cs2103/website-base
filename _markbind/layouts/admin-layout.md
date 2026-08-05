<head-bottom>
<link rel="stylesheet" href="{{baseUrl}}/css/main.css">
<link rel="stylesheet" href="{{baseUrl}}/css/admin.css">
  <script>
    function mdblockCopy(btn) {
      const md = decodeURIComponent(btn.closest('.mdblock').dataset.md);
      const flash = (msg) => {
        btn.textContent = msg;
        setTimeout(() => { btn.textContent = btn.dataset.label; }, 1500);
      };
      // navigator.clipboard needs a secure context (https or localhost); fall
      // back to the textarea + execCommand trick everywhere else.
      const legacy = () => {
        const ta = document.createElement('textarea');
        ta.value = md;
        ta.setAttribute('readonly', '');
        ta.style.cssText = 'position:fixed;top:-1000px;opacity:0';
        document.body.appendChild(ta);
        ta.select();
        const ok = document.execCommand('copy');
        document.body.removeChild(ta);
        flash(ok ? 'Copied!' : 'Copy failed');
      };
      if (navigator.clipboard && window.isSecureContext) {
        navigator.clipboard.writeText(md).then(() => flash('Copied!'), legacy);
      } else {
        legacy();
      }
    }
  </script>
</head-bottom>
{% include '_markbind/layouts/header.md' %}
{% set file =  "" if course in ['TIC2002', 'TEE3201'] else "admin" %}
{% set sitenav_title =  "Admin info" %}
{% include '_markbind/layouts/body.md' %}
{% include '_markbind/layouts/footer.md' %}
