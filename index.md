---
title: Welcome to my blog
---

<input id="eur" type="number" step="0.01" placeholder="EUR">
<p id="bgn"></p>

<script>
  const RATE = 1.95583;
  const eur = document.getElementById("eur");
  const bgn = document.getElementById("bgn");

  eur.addEventListener("input", () => {
    const val = parseFloat(eur.value);
    if (Number.isFinite(val)) bgn.textContent = (val * RATE).toFixed(2) + " BGN";
    else bgn.textContent = "";
  });
</script>
