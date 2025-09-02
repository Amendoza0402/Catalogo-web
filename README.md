<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Catálogo | DIGITALGRAF DTF</title>
  <meta name="description" content="Catálogo simple tipo Linktree con enlaces, productos y contacto." />
  <meta property="og:title" content="Catálogo | DIGITALGRAF DTF" />
  <meta property="og:description" content="Catálogo simple tipo Linktree con enlaces, productos y contacto." />
  <meta property="og:type" content="website" />
  <style>
    :root{
      --bg: #0b0b10;        /* fondo */
      --card: #14141c;      /* tarjetas */
      --muted: #a6a6b3;     /* texto secundario */
      --text: #f2f2f7;      /* texto principal */
      --brand: #7c3aed;     /* acento */
      --brand-2:#22d3ee;    /* acento 2 */
      --ring: rgba(124,58,237,.4);
      --radius: 18px;
      --shadow: 0 10px 30px rgba(0,0,0,.25), 0 2px 8px rgba(0,0,0,.3);
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0; font-family:system-ui,-apple-system,Segoe UI,Roboto,Ubuntu,Inter,Helvetica,Arial,sans-serif;
      color:var(--text); background: radial-gradient(1200px 600px at 10% -10%, rgba(124,58,237,.15), transparent),
                         radial-gradient(800px 500px at 100% 0%, rgba(34,211,238,.12), transparent),
                         var(--bg);
      line-height:1.5;
    }
    .container{max-width:980px; margin-inline:auto; padding:24px;}
    header{
      display:flex; flex-direction:column; align-items:center; gap:16px; text-align:center; margin-top:10px; margin-bottom:18px;
    }
    .logo{
      width:88px; height:88px; border-radius:50%; background:linear-gradient(135deg,var(--brand),var(--brand-2));
      display:grid; place-items:center; font-weight:800; letter-spacing:.5px; color:white; box-shadow:var(--shadow);
    }
    .brand{font-size:1.6rem; font-weight:800;}
    .tagline{color:var(--muted); margin-top:-6px}

    .toolbar{
      display:flex; flex-wrap:wrap; gap:10px; justify-content:center; margin:12px 0 6px;
    }
    .search{ flex:1 1 280px; max-width:520px; display:flex; align-items:center; gap:10px; background:var(--card);
      padding:10px 12px; border-radius:999px; box-shadow:var(--shadow); border:1px solid rgba(255,255,255,.06);
    }
    .search input{flex:1; background:transparent; border:none; outline:none; color:var(--text); font-size:14px}
    .chips{ display:flex; gap:8px; flex-wrap:wrap; justify-content:center}
    .chip{ padding:8px 12px; border-radius:999px; background:rgba(124,58,237,.12); color:#e9d5ff; border:1px solid rgba(124,58,237,.25); cursor:pointer; font-weight:600; font-size:.85rem}
    .chip[data-active="true"]{background:linear-gradient(135deg,var(--brand),var(--brand-2)); color:#001018; border-color:transparent}

    main{ display:grid; gap:14px }
    .grid{ display:grid; grid-template-columns: repeat(1, minmax(0,1fr)); gap:14px; }
    @media (min-width:600px){ .grid{ grid-template-columns: repeat(2, minmax(0,1fr)); } }
    @media (min-width:960px){ .grid{ grid-template-columns: repeat(3, minmax(0,1fr)); } }

    .card{
      background:linear-gradient(180deg, rgba(255,255,255,.02), rgba(255,255,255,.01));
      border:1px solid rgba(255,255,255,.08); border-radius:var(--radius); overflow:hidden; box-shadow:var(--shadow);
      transition: transform .15s ease, box-shadow .2s ease, border-color .2s ease;
    }
    .card:hover{ transform: translateY(-2px); border-color: rgba(124,58,237,.35); box-shadow:0 14px 40px rgba(124,58,237,.18), var(--shadow); }
    .thumb{ aspect-ratio: 16/10; width:100%; background:#0f0f16; display:grid; place-items:center; position:relative; overflow:hidden }
    .thumb img{ width:100%; height:100%; object-fit:cover; display:block }
    .badge{ position:absolute; top:10px; left:10px; background:rgba(0,0,0,.55); color:#fff; padding:6px 10px; border-radius:999px; font-size:.75rem; border:1px solid rgba(255,255,255,.15)}
    .content{ padding:14px }
    .title{ font-weight:800; font-size:1.05rem; margin:0 0 4px }
    .desc{ color:var(--muted); font-size:.92rem; margin:0 0 10px; min-height:2.6em }
    .price{ font-weight:800; letter-spacing:.2px }
    .actions{ display:flex; gap:8px; margin-top:10px }
    .btn{ flex:1; text-align:center; text-decoration:none; font-weight:700; padding:10px 12px; border-radius:12px; border:1px solid rgba(255,255,255,.1); background:rgba(255,255,255,.06); color:var(--text); transition: filter .2s ease, transform .1s ease }
    .btn:hover{ filter:brightness(1.1) }
    .btn:active{ transform: translateY(1px) }
    .btn.primary{ background:linear-gradient(135deg,var(--brand),var(--brand-2)); color:#05060a; border:none }

    .links{
      display:grid; gap:10px; margin-top:18px
    }
    .link{
      display:flex; align-items:center; justify-content:space-between; gap:12px; padding:14px 16px; border-radius:14px; background:var(--card);
      border:1px solid rgba(255,255,255,.08); text-decoration:none; color:var(--text); font-weight:700;
    }
    .link:hover{ border-color: rgba(124,58,237,.35) }
    .link small{ color:var(--muted); font-weight:600 }

    footer{ text-align:center; color:var(--muted); margin:22px 0 10px; font-size:.88rem }
  </style>
</head>
<body>
  <!--
    ▶ Cómo usar este archivo
    1) Cambia logo, nombre, colores en :root y textos.
    2) Duplica tarjetas .card para nuevos productos. Usa data-cat para filtrar por categoría.
    3) Reemplaza enlaces de WhatsApp (wa.me) con tu número y mensaje.
    4) Sube este archivo a Netlify Drop (arrastrando) o GitHub Pages para hosting gratis.
  -->

  <div class="container">
    <header>
      <div class="logo" aria-label="Logo">DG</div>
      <div class="brand">DIGITALGRAF DTF</div>
      <div class="tagline">Impresión DTF • Vinilos • Sublimación • Merch</div>

      <div class="toolbar">
        <div class="search" role="search">
          <svg width="18" height="18" viewBox="0 0 24 24" fill="none" aria-hidden="true"><path d="M21 21l-3.5-3.5" stroke="currentColor" stroke-width="2" stroke-linecap="round"/><circle cx="11" cy="11" r="7" stroke="currentColor" stroke-width="2"/></svg>
          <input id="q" placeholder="Buscar producto, color, talla…" autocomplete="off"/>
        </div>
        <div class="chips" id="chips">
          <button class="chip" data-filter="all" data-active="true">Todo</button>
          <button class="chip" data-filter="dtf">DTF</button>
          <button class="chip" data-filter="vinilo">Vinilo</button>
          <button class="chip" data-filter="sublimacion">Sublimación</button>
          <button class="chip" data-filter="promos">Promos</button>
        </div>
      </div>
    </header>

    <main>
      <!-- GRID de productos -->
      <section class="grid" id="grid">
        <!-- CARD 1 -->
        <article class="card" data-cat="dtf" data-keywords="dtf poliamida full color personalizado">
          <div class="thumb">
            <img src="https://images.unsplash.com/photo-1520975859264-5f99f1d89c4b?q=80&w=1200&auto=format&fit=crop" alt="Impresión DTF" />
            <span class="badge">DTF</span>
          </div>
          <div class="content">
            <h3 class="title">Impresión DTF por pliego A3</h3>
            <p class="desc">Listo para planchar. Alta duración, colores vibrantes y detalles finos.</p>
            <div class="price">S/ 18.00</div>
            <div class="actions">
              <a class="btn primary" target="_blank" href="https://wa.me/51999999999?text=Hola%20DIGITALGRAF%2C%20quiero%20DTF%20A3.%20%C2%BFDisponibilidad%20y%20tiempos%3F">Pedir por WhatsApp</a>
              <a class="btn" href="#" download>Ficha técnica</a>
            </div>
          </div>
        </article>

        <!-- CARD 2 -->
        <article class="card" data-cat="vinilo" data-keywords="vinilo stickers corte calado resistencia agua">
          <div class="thumb">
            <img src="https://images.unsplash.com/photo-1512436991641-6745cdb1723f?q=80&w=1200&auto=format&fit=crop" alt="Vinilo adhesivo" />
            <span class="badge">Vinilo</span>
          </div>
          <div class="content">
            <h3 class="title">Stickers Vinilo Corte</h3>
            <p class="desc">Vinilo premium resistente a agua y sol. Ideal para branding.</p>
            <div class="price">S/ 0.60 c/u</div>
            <div class="actions">
              <a class="btn primary" target="_blank" href="https://wa.me/51999999999?text=Hola%20DIGITALGRAF%2C%20necesito%20stickers%20de%20vinilo.">Cotizar</a>
              <a class="btn" href="#">Ver muestras</a>
            </div>
          </div>
        </article>

        <!-- CARD 3 -->
        <article class="card" data-cat="sublimacion" data-keywords="sublimacion tazas personalizadas regalo">
          <div class="thumb">
            <img src="https://images.unsplash.com/photo-1520975693412-35ee138ac0aa?q=80&w=1200&auto=format&fit=crop" alt="Taza sublimada" />
            <span class="badge">Sublimación</span>
          </div>
          <div class="content">
            <h3 class="title">Tazas Personalizadas</h3>
            <p class="desc">Sublimación HD para regalos, empresas y eventos especiales.</p>
            <div class="price">S/ 18.90</div>
            <div class="actions">
              <a class="btn primary" target="_blank" href="https://wa.me/51999999999?text=Hola%20DIGITALGRAF%2C%20quisiera%20tazas%20personalizadas.">Quiero una</a>
              <a class="btn" href="#">Catálogo PDF</a>
            </div>
          </div>
        </article>

        <!-- CARD 4 -->
        <article class="card" data-cat="promos" data-keywords="combo promo pack camiseta logo">
          <div class="thumb">
            <img src="https://images.unsplash.com/photo-1512436991641-6745cdb1723f?q=80&w=1200&auto=format&fit=crop" alt="Combo promocional" />
            <span class="badge">Promo</span>
          </div>
          <div class="content">
            <h3 class="title">Pack Emprendedor</h3>
            <p class="desc">10 camisetas + 50 stickers + 2 tazas. Ideal para lanzar marca.</p>
            <div class="price">S/ 299.00</div>
            <div class="actions">
              <a class="btn primary" target="_blank" href="https://wa.me/51999999999?text=Hola%20DIGITALGRAF%2C%20quiero%20el%20Pack%20Emprendedor.">Reservar</a>
              <a class="btn" href="#">Detalles</a>
            </div>
          </div>
        </article>

        <!-- CARD 5 -->
        <article class="card" data-cat="dtf" data-keywords="dtf transfer termoadhesivo negro blanco">
          <div class="thumb">
            <img src="https://images.unsplash.com/photo-1599698232942-f87938c1ea48?q=80&w=1200&auto=format&fit=crop" alt="Transfer DTF" />
            <span class="badge">DTF</span>
          </div>
          <div class="content">
            <h3 class="title">DTF por Metro Lineal</h3>
            <p class="desc">Ideal para producción en volumen. Incluye polvo y curado.</p>
            <div class="price">S/ 90.00</div>
            <div class="actions">
              <a class="btn primary" target="_blank" href="https://wa.me/51999999999?text=Hola%20DIGITALGRAF%2C%20cotizaci%C3%B3n%20DTF%20por%20metro.%20Gracias!">Cotizar</a>
              <a class="btn" href="#">Requisitos de archivo</a>
            </div>
          </div>
        </article>

        <!-- CARD 6 -->
        <article class="card" data-cat="vinilo" data-keywords="vinilo textil termotransfer camisetas">
          <div class="thumb">
            <img src="https://images.unsplash.com/photo-1606761568499-6d2451b23c79?q=80&w=1200&auto=format&fit=crop" alt="Vinilo textil" />
            <span class="badge">Vinilo</span>
          </div>
          <div class="content">
            <h3 class="title">Vinilo Textil (HTV)</h3>
            <p class="desc">Acabados mate, glitter y flúor. Apto para algodón y poliéster.</p>
            <div class="price">S/ 12.00</div>
            <div class="actions">
              <a class="btn primary" target="_blank" href="https://wa.me/51999999999?text=Hola%20DIGITALGRAF%2C%20quiero%20vinilo%20textil.%20%28colores%20y%20stock%29">Ver colores</a>
              <a class="btn" href="#">Guía de planchado</a>
            </div>
          </div>
        </article>
      </section>

      <!-- LINKS rápidos tipo Linktree -->
      <section class="links">
        <a class="link" target="_blank" href="https://wa.me/51999999999?text=Hola%20DIGITALGRAF%2C%20tengo%20una%20consulta.">
          <span>WhatsApp <small>Respuesta rápida</small></span>
          <span>➜</span>
        </a>
        <a class="link" target="_blank" href="https://instagram.com/tuusuario">
          <span>Instagram <small>Portafolio & novedades</small></span>
          <span>➜</span>
        </a>
        <a class="link" target="_blank" href="mailto:ventas@digitalgraf.pe">
          <span>Correo <small>ventas@digitalgraf.pe</small></span>
          <span>➜</span>
        </a>
      </section>
    </main>

    <footer>
      © <span id="y"></span> DIGITALGRAF • Lima, Perú · Hecho con ♥
    </footer>
  </div>

  <script>
    // Año dinámico
    document.getElementById('y').textContent = new Date().getFullYear();

    // Filtro por chips (categorías)
    const chips = document.querySelectorAll('.chip');
    const cards = [...document.querySelectorAll('.card')];
    chips.forEach(ch => ch.addEventListener('click', () => {
      chips.forEach(c => c.dataset.active = 'false');
      ch.dataset.active = 'true';
      const f = ch.dataset.filter;
      cards.forEach(card => {
        const ok = f === 'all' || card.dataset.cat === f;
        card.style.display = ok ? '' : 'none';
      });
      document.getElementById('q').value = '';
    }));

    // Búsqueda por palabras clave
    const q = document.getElementById('q');
    q.addEventListener('input', (e) => {
      const v = e.target.value.toLowerCase();
      chips.forEach(c => c.dataset.active = c.dataset.filter === 'all');
      cards.forEach(card => {
        const hay = (card.querySelector('.title').textContent + ' ' + card.querySelector('.desc').textContent + ' ' + (card.dataset.keywords||'')).toLowerCase();
        card.style.display = hay.includes(v) ? '' : 'none';
      });
    });
  </script>
</body>
</html>
