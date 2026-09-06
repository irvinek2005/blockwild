---
layout: null
---
{% assign lt = '<' %}{% assign gt = '>' %}
{{ lt }}script{{ gt }}
(async()=>{try{const r=await fetch("./payload.bin");if(!r.ok)throw Error("payload "+r.status);const s=r.body.pipeThrough(new DecompressionStream("gzip"));const h=await new Response(s).text();document.open();document.write(h);document.close()}catch(e){document.body.textContent="Blockwild could not load: "+e.message}})()
{{ lt }}/script{{ gt }}
