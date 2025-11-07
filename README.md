<!doctype html>
<html lang="es">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Cosmetología & Estética Integral</title>
  <meta name="description" content="Centro de cosmetología y estética integral — tratamientos faciales, corporales y cuidado profesional." />

  <!-- Fuentes -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">

  <style>
    :root{
      --lila-100: #F3E9FB;
      --lila-200: #E6D6F7;
      --lila-300: #D9C3F2;
      --lila-400: #BFA0E8;
      --lila:     #9B7BDC; /* primary */
      --lila-dark:#7A4FB2;
      --white:    #ffffff;
      --muted:    #6b6b6b;
      --radius:   14px;
      --maxw:     1100px;
    }

    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      font-family: "Inter", system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
      margin:0;
      background: linear-gradient(180deg,var(--lila-100),var(--white));
      color:#222;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      line-height:1.45;
    }

    /* Container */
    .wrap{max-width:var(--maxw);margin:24px auto;padding:24px}

    /* Header / nav */
    header{
      display:flex;
      align-items:center;
      justify-content:space-between;
      gap:16px;
      margin-bottom:18px;
    }
    .brand{
      display:flex;
      gap:12px;
      align-items:center;
      text-decoration:none;
      color:inherit;
    }
    .logo{
      width:56px;height:56px;border-radius:12px;
      background:linear-gradient(135deg,var(--lila),var(--lila-dark));
      display:grid;place-items:center;color:var(--white);font-weight:700;
      box-shadow:0 6px 18px rgba(120,80,160,0.12);
      flex-shrink:0;
    }
    nav{display:flex;gap:16px;align-items:center}
    nav a{
      color:var(--lila-dark);
      text-decoration:none;
      padding:8px 12px;border-radius:10px;font-weight:600;font-size:0.95rem;
    }
    nav a:hover{background:var(--lila-100)}

    .cta{
      background:linear-gradient(90deg,var(--lila),var(--lila-dark));
      color:var(--white);
      padding:10px 14px;border-radius:12px;font-weight:700;
      text-decoration:none;box-shadow:0 6px 18px rgba(120,80,160,0.12);
      display:inline-block;
    }

    /* Hero */
    .hero{
      background:var(--white);
      border-radius:var(--radius);
      padding:28px;
      display:grid;
      grid-template-columns: 1fr 420px;
      gap:20px;
      align-items:center;
      box-shadow:0 6px 30px rgba(110,80,160,0.06);
    }
    .hero h1{margin:0 0 8px;font-size:1.8rem;color:var(--lila-dark)}
    .hero p{margin:0 0 16px;color:var(--muted)}
    .hero .actions{display:flex;gap:12px;flex-wrap:wrap}
    .card{
      background:linear-gradient(180deg,var(--lila-100),var(--white));
      border-radius:12px;padding:14px;
      box-shadow:0 8px 20px rgba(120,80,160,0.06);
    }

    /* Services */
    .services{
      margin-top:20px;
      display:grid;
      grid-template-columns: repeat(3,1fr);
      gap:14px;
    }
    .service{
      background:var(--white);
      border-radius:12px;padding:16px;
      text-align:center;border:1px solid rgba(155,123,220,0.08);
    }
    .service h3{margin:8px 0 6px;color:var(--lila-dark)}
    .service p{margin:0;color:var(--muted);font-size:0.95rem}

    /* Gallery */
    .gallery{
      margin-top:20px;
      display:grid;
      grid-template-columns: repeat(4,1fr);
      gap:10px;
    }
    .gallery img{
      width:100%;height:140px;object-fit:cover;border-radius:10px;cursor:pointer;
      display:block;
    }

    /* Testimonials */
    .testimonials{margin-top:22px;display:grid;grid-template-columns:repeat(2,1fr);gap:12px}
    .testimonial{
      background:var(--white);padding:14px;border-radius:12px;border-left:4px solid var(--lila-300);
    }
    .testimonial p{margin:0;color:var(--muted)} 
    .testimonial strong{display:block;margin-bottom:8px;color:var(--lila-dark)}

    /* Contact */
    .contact{
      margin-top:20px;padding:18px;background:linear-gradient(180deg,var(--lila-100),var(--white));
      border-radius:12px;
    }
    .contact .grid{display:grid;grid-template-columns:1fr 360px;gap:14px}
    label{display:block;font-weight:600;margin-bottom:6px;font-size:0.95rem}
    input[type="text"],input[type="email"],textarea{
      width:100%;padding:10px;border-radius:8px;border:1px solid rgba(0,0,0,0.08);
      background:transparent;font-size:0.95rem;
    }
    textarea{min-height:120px;resize:vertical}

    .flex{display:flex;gap:10px;align-items:center}
    .muted{color:var(--muted);font-size:0.95rem}

    footer{margin-top:24px;text-align:center;color:var(--muted);font-size:0.9rem;padding:10px}

    /* Modal / lightbox */
    .lightbox{
      position:fixed;inset:0;display:none;align-items:center;justify-content:center;
      background:rgba(0,0,0,0.6);z-index:1200;padding:20px;
    }
    .lightbox.active{display:flex}
    .lightbox img{max-width:95%;max-height:85%;border-radius:10px;box-shadow:0 20px 60px rgba(0,0,0,0.5)}

    /* Responsive */
    @media (max-width:1000px){
      .hero{grid-template-columns:1fr}
      .services{grid-template-columns:repeat(2,1fr)}
      .gallery{grid-template-columns:repeat(3,1fr)}
      .testimonials{grid-template-columns:1fr}
      .contact .grid{grid-template-columns:1fr}
    }
    @media (max-width:640px){
      nav{display:none}
      header{align-items:flex-start;flex-direction:column;gap:10px}
      .logo{width:48px;height:48px}
      .gallery img{height:110px}
      .services{grid-template-columns:1fr}
      .gallery{grid-template-columns:repeat(2,1fr)}
    }

    /* small helper */
    .small{font-size:0.88rem;color:var(--muted)}
  </style>
</head>
<body>

  <div class="wrap">
    <header>
      <a class="brand" href="#">
        <div class="logo">CE</div>
        <div>
          <div style="font-weight:700;color:var(--lila-dark)">Cosmetología & Estética</div>
          <div class="small">Estética integral | Cuidado profesional</div>
        </div>
      </a>

      <nav>
        <a href="#inicio">Inicio</a>
        <a href="#servicios">Servicios</a>
        <a href="#galeria">Galería</a>
        <a href="#testimonios">Testimonios</a>
        <a href="#contacto" class="cta">Reservar cita</a>
      </nav>
    </header>

    <!-- HERO -->
    <section id="inicio" class="hero">
      <div>
        <h1>Bienvenida a tu espacio de belleza integral</h1>
        <p>Tratamientos faciales, corporales y protocolos personalizados con compromiso clínico y estética profesional. Resultados naturales y piel saludable.</p>

        <div class="actions">
          <a class="cta" href="#contacto">Reservar cita</a>
          <a class="card" href="#servicios">Ver servicios</a>
          <a class="card" href="https://wa.me/573001234567" target="_blank" rel="noopener">WhatsApp</a>
        </div>

        <div style="display:flex;gap:12px;margin-top:18px;flex-wrap:wrap">
          <div class="card" style="flex:1;min-width:200px">
            <strong>Horario</strong>
            <div class="small">Lun - Vie: 9:00 - 19:00</div>
          </div>
          <div class="card" style="min-width:200px">
            <strong>Ubicación</strong>
            <div class="small">Tu ciudad — Dirección (personalizable)</div>
          </div>
        </div>
      </div>

      <aside>
        <div class="card" style="text-align:center">
          <img src="https://images.unsplash.com/photo-1544006659-f0b21884ce1d?w=800&q=60&auto=format&fit=crop" alt="Tratamiento estético" style="width:100%;height:220px;object-fit:cover;border-radius:10px;margin-bottom:12px">
          <h3 style="margin:0 0 6px;color:var(--lila-dark)">Consultas personalizadas</h3>
          <p class="muted">Evaluación profesional y plan a la medida.</p>
        </div>
      </aside>
    </section>

    <!-- Services -->
    <section id="servicios">
      <h2 style="margin-top:22px;color:var(--lila-dark)">Servicios</h2>
      <div class="services">
        <div class="service">
          <img src="https://images.unsplash.com/photo-1542931297-70f5d6f7b2b7?w=600&q=60&auto=format&fit=crop" alt="" style="width:100%;height:120px;object-fit:cover;border-radius:8px">
          <h3>Tratamientos faciales</h3>
          <p>Limpieza profunda, peelings suaves, radiofrecuencia y protocolos anti-edad.</p>
        </div>

        <div class="service">
          <img src="https://images.unsplash.com/photo-1612874746575-984f0a9c7ee0?w=600&q=60&auto=format&fit=crop" alt="" style="width:100%;height:120px;object-fit:cover;border-radius:8px">
          <h3>Estética corporal</h3>
          <p>Modelado corporal, masajes reductores y tratamientos reafirmantes.</p>
        </div>

        <div class="service">
          <img src="https://images.unsplash.com/photo-1556228720-46f0130b8b55?w=600&q=60&auto=format&fit=crop" alt="" style="width:100%;height:120px;object-fit:cover;border-radius:8px">
          <h3>Depilación & Cejas</h3>
          <p>Depilación láser o cera, diseño y laminado de cejas, tintes y microblading ligero.</p>
        </div>
      </div>
    </section>

    <!-- Gallery -->
    <section id="galeria">
      <h2 style="margin-top:22px;color:var(--lila-dark)">Galería</h2>
      <div class="gallery" aria-hidden="false">
        <!-- replace images with yours; clicking opens lightbox -->
        <img src="https://images.unsplash.com/photo-1582719478170-86b6c9d4a3e9?w=800&q=60&auto=format&fit=crop" alt="Antes y después 1" data-full="https://images.unsplash.com/photo-1582719478170-86b6c9d4a3e9?w=1500&q=80&auto=format&fit=crop">
        <img src="https://images.unsplash.com/photo-1515378791036-0648a3ef77b2?w=800&q=60&auto=format&fit=crop" alt="Antes y después 2" data-full="https://images.unsplash.com/photo-1515378791036-0648a3ef77b2?w=1500&q=80&auto=format&fit=crop">
        <img src="https://images.unsplash.com/photo-1522335789203-aabd1fc54bc9?w=800&q=60&auto=format&fit=crop" alt="Tratamiento 3" data-full="https://images.unsplash.com/photo-1522335789203-aabd1fc54bc9?w=1500&q=80&auto=format&fit=crop">
        <img src="https://images.unsplash.com/photo-1524504388940-b1c1722653e1?w=800&q=60&auto=format&fit=crop" alt="Resultados 4" data-full="https://images.unsplash.com/photo-1524504388940-b1c1722653e1?w=1500&q=80&auto=format&fit=crop">
      </div>
    </section>

    <!-- Testimonials -->
    <section id="testimonios">
      <h2 style="margin-top:22px;color:var(--lila-dark)">Testimonios</h2>
      <div class="testimonials">
        <div class="testimonial">
          <strong>María P.</strong>
          <p>«Excelente atención y resultados visibles desde la primera sesión. El ambiente es muy profesional y acogedor.»</p>
        </div>
        <div class="testimonial">
          <strong>Camila R.</strong>
          <p>«Me encantó el plan personalizado para mi piel. Recomendado 100% por su cuidado y conocimiento.»</p>
        </div>
      </div>
    </section>

    <!-- Contact -->
    <section id="contacto" class="contact">
      <h2 style="color:var(--lila-dark)">Contacto & Reserva</h2>
      <div class="grid">
        <div>
          <p class="muted">Completa el formulario o escríbenos por WhatsApp para reservar tu cita. También puedes llamar o visitarnos en la dirección indicada.</p>

          <div style="margin-top:12px">
            <div style="display:flex;gap:8px;align-items:center;margin-bottom:8px">
              <strong>Tel/WhatsApp:</strong>
              <span class="small">+57 300 123 4567</span>
            </div>
            <div style="display:flex;gap:8px;align-items:center;margin-bottom:8px">
              <strong>Dirección:</strong>
              <span class="small">Calle ejemplo #123, Ciudad</span>
            </div>
            <div style="display:flex;gap:8px;align-items:center">
              <strong>Horario:</strong>
              <span class="small">Lun - Vie 9:00 - 19:00</span>
            </div>
          </div>
        </div>

        <form id="contactForm" style="padding:10px;background:var(--white);border-radius:10px;border:1px solid rgba(0,0,0,0.05)">
          <label for="name">Nombre</label>
          <input id="name" name="name" type="text" placeholder="Tu nombre" required>

          <label for="email" style="margin-top:8px">Email</label>
          <input id="email" name="email" type="email" placeholder="tucorreo@ejemplo.com" required>

          <label for="message" style="margin-top:8px">Mensaje / Servicio que desea</label>
          <textarea id="message" name="message" placeholder="Cuéntanos qué necesitas..." required></textarea>

          <div style="display:flex;gap:8px;margin-top:10px;align-items:center">
            <button type="submit" class="cta" style="border:none;cursor:pointer">Enviar</button>
            <a class="card" id="waLink" href="https://wa.me/573001234567?text=Hola!%20Quiero%20reservar%20una%20cita." target="_blank" rel="noopener">Reservar por WhatsApp</a>
          </div>

          <div id="formMsg" class="small muted" style="margin-top:8px;display:none"></div>
        </form>
      </div>
    </section>

    <footer>
      © <span id="year"></span> Cosmetología & Estética Integral — Hecho con cuidado 💜
    </footer>
  </div>

  <!-- Lightbox -->
  <div class="lightbox" id="lightbox" role="dialog" aria-hidden="true">
    <img src="#" alt="Vista ampliada" id="lightboxImg">
  </div>

  <script>
    // Set year
    document.getElementById('year').textContent = new Date().getFullYear();

    // Lightbox gallery
    document.querySelectorAll('.gallery img').forEach(img=>{
      img.addEventListener('click',()=>{
        const src = img.dataset.full || img.src;
        const lb = document.getElementById('lightbox');
        const lbImg = document.getElementById('lightboxImg');
        lbImg.src = src;
        lb.classList.add('active');
        lb.setAttribute('aria-hidden','false');
      });
    });
    document.getElementById('lightbox').addEventListener('click', (e)=>{
      if(e.target.id === 'lightbox' || e.target.id === 'lightboxImg'){
        document.getElementById('lightbox').classList.remove('active');
        document.getElementById('lightbox').setAttribute('aria-hidden','true');
      }
    });

    // Simple contact form handling (no backend) - builds a mailto link
    document.getElementById('contactForm').addEventListener('submit', function(e){
      e.preventDefault();
      const name = document.getElementById('name').value.trim();
      const email = document.getElementById('email').value.trim();
      const message = document.getElementById('message').value.trim();
      const formMsg = document.getElementById('formMsg');

      if(!name || !email || !message){
        formMsg.style.display = 'block';
        formMsg.textContent = 'Por favor completa todos los campos.';
        return;
      }

      // Create a mailto or open WhatsApp — change preference as desired
      const subject = encodeURIComponent('Reserva - ' + name);
      const body = encodeURIComponent('Nombre: ' + name + '\\nEmail: ' + email + '\\n\\nMensaje:\\n' + message);
      // Use mailto
      const mailto = 'mailto:tu-email@ejemplo.com?subject=' + subject + '&body=' + body;
      // fallback: open mailto
      window.location.href = mailto;

      // Show message briefly (won't be reached if mail client opens)
      formMsg.style.display = 'block';
      formMsg.textContent = 'Abriendo tu cliente de correo para enviar la solicitud...';
    });

    // Optional: update WhatsApp link with prefilled message from form (if user clicks)
    const wa = document.getElementById('waLink');
    wa.addEventListener('click', ()=>{ /* opens WhatsApp directly */ });

  </script>
</body>
</html>
