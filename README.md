# Mata-flower-and-craft
<style>
@import url('https://fonts.googleapis.com/css2?family=Mitr:wght@400;500;600&family=Prompt:wght@300;400;500;600;700&display=swap');

:root{
  --cream:#FFF8EE; --yellow:#FFC94B; --yellow-soft:#FFF3D1;
  --green:#6A994E; --green-dark:#527D3A; --green-soft:#EDF4E4;
  --pink:#F49CC8; --pink-soft:#FDE9F3;
  --blue:#79BEE8; --blue-soft:#E7F4FC;
  --ink:#43382C; --muted:#8C7B67;
  --shadow:0 6px 24px rgba(93,64,20,.10);
}
*{margin:0;padding:0;box-sizing:border-box}
html{scroll-behavior:smooth}
body{font-family:'Prompt',sans-serif;background:var(--cream);color:var(--ink);line-height:1.6;overflow-x:hidden}
img{display:block;max-width:100%}
a{text-decoration:none;color:inherit}
h1,h2,h3{font-family:'Mitr',sans-serif;font-weight:500;line-height:1.25}
::selection{background:var(--yellow);color:#5c430f}

/* ===== Navbar ===== */
.navbar{position:sticky;top:0;z-index:100;display:flex;align-items:center;justify-content:space-between;
  padding:14px 6%;background:rgba(255,248,238,.88);backdrop-filter:blur(12px);transition:box-shadow .3s}
.navbar.scrolled{box-shadow:var(--shadow)}
.logo{font-family:'Mitr';font-size:1.25rem;font-weight:600;display:flex;align-items:center;gap:6px}
.logo span{font-size:.65rem;letter-spacing:.22em;color:var(--green);font-weight:500}
.nav-links{display:flex;gap:28px}
.nav-links a{font-weight:500;color:var(--muted);position:relative;transition:color .25s}
.nav-links a:hover{color:var(--green-dark)}
.nav-links a::after{content:'';position:absolute;left:0;bottom:-5px;width:0;height:3px;border-radius:3px;background:var(--yellow);transition:width .25s}
.nav-links a:hover::after{width:100%}
.nav-toggle{display:none;background:none;border:0;font-size:1.5rem;cursor:pointer;color:var(--ink)}

/* ===== Hero ===== */
.hero{display:grid;grid-template-columns:1.05fr .95fr;gap:52px;align-items:center;max-width:1200px;margin:auto;padding:60px 6% 80px}
.badge{display:inline-block;background:var(--yellow-soft);color:#8a6a1f;padding:8px 18px;border-radius:999px;font-size:.85rem;font-weight:600}
.hero h1{font-size:clamp(2.1rem,4.5vw,3.3rem);margin-top:18px}
.hero h1 em{font-style:normal;color:var(--green-dark);position:relative;z-index:0}
.hero h1 em::after{content:'';position:absolute;left:0;right:0;bottom:5px;height:12px;background:var(--yellow);opacity:.55;border-radius:6px;z-index:-1}
.hero p{color:var(--muted);margin:18px 0 28px;max-width:46ch}
.hero-cta{display:flex;gap:14px;flex-wrap:wrap}
.btn{display:inline-block;padding:13px 28px;border-radius:999px;font-weight:600;font-family:'Prompt';transition:transform .25s,box-shadow .25s,background .25s}
.btn-primary{background:var(--yellow);color:#5c430f;box-shadow:0 8px 20px rgba(255,201,75,.4)}
.btn-primary:hover{transform:translateY(-3px)}
.btn-ghost{border:2px solid var(--green);color:var(--green-dark)}
.btn-ghost:hover{background:var(--green-soft)}
.hero-stats{display:flex;gap:36px;margin-top:38px}
.stat b{font-family:'Mitr';font-size:1.45rem;color:var(--green-dark);display:block}
.stat span{font-size:.85rem;color:var(--muted)}
.hero-img{position:relative}
.hero-img img{width:100%;aspect-ratio:4/5;object-fit:cover;border-radius:30px;box-shadow:var(--shadow);border:8px solid #fff}
.float-card{position:absolute;background:#fff;border-radius:16px;padding:10px 18px;font-size:.85rem;font-weight:600;box-shadow:var(--shadow);animation:float 4.5s ease-in-out infinite}
.fc1{top:26px;right:-12px}
.fc2{bottom:30px;left:-12px;animation-delay:1.6s}
@keyframes float{0%,100%{transform:translateY(0)}50%{transform:translateY(-10px)}}

/* ===== Marquee ===== */
.marquee{background:var(--green);color:#fff;overflow:hidden;padding:12px 0}
.marquee-track{display:flex;width:max-content;animation:marquee 22s linear infinite;font-family:'Mitr';font-size:.95rem}
.marquee span{white-space:nowrap}
@keyframes marquee{to{transform:translateX(-50%)}}

/* ===== Section head ===== */
.section-head{text-align:center;max-width:640px;margin:0 auto 42px}
.kicker{display:inline-block;color:var(--green);font-weight:700;font-size:.75rem;letter-spacing:.2em;text-transform:uppercase;margin-bottom:8px}
.section-head h2{font-size:clamp(1.6rem,3vw,2.2rem)}
.section-head p{color:var(--muted);margin-top:8px}

/* ===== Products ===== */
.products{max-width:1200px;margin:auto;padding:80px 6% 70px}
.filter{display:flex;gap:10px;justify-content:center;flex-wrap:wrap;margin-bottom:38px}
.filter button{border:2px solid #e8dcc8;background:#fff;padding:8px 22px;border-radius:999px;font-family:'Prompt';font-weight:600;font-size:.9rem;color:var(--muted);cursor:pointer;transition:.25s}
.filter button:hover{border-color:var(--green);color:var(--green-dark)}
.filter button.active{background:var(--green);border-color:var(--green);color:#fff}
.grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(250px,1fr));gap:26px}
.card{background:#fff;border-radius:22px;overflow:hidden;box-shadow:0 4px 18px rgba(93,64,20,.08);transition:transform .35s,box-shadow .35s}
.card:hover{transform:translateY(-8px);box-shadow:0 16px 34px rgba(93,64,20,.16)}
.card.hide{display:none}
.thumb{height:250px;overflow:hidden;position:relative}
.thumb img{width:100%;height:100%;object-fit:cover;transition:transform .6s}
.card:hover .thumb img{transform:scale(1.07)}
.tag{position:absolute;top:14px;left:14px;padding:6px 14px;border-radius:999px;font-size:.75rem;font-weight:700;color:#fff}
.t-yellow{background:var(--yellow);color:#6b4e0e}
.t-green{background:var(--green)}
.t-blue{background:var(--blue)}
.t-pink{background:var(--pink)}
.card-body{padding:18px 20px 22px}
.card-body h3{font-size:1rem}
.desc{font-size:.83rem;color:var(--muted);margin:6px 0 14px}
.card-foot{display:flex;justify-content:space-between;align-items:center}
.price{font-family:'Mitr';font-weight:600;color:var(--green-dark);font-size:1.1rem}
.btn-order{background:var(--green);color:#fff;padding:8px 20px;border-radius:999px;font-size:.83rem;font-weight:600;transition:background .25s}
.btn-order:hover{background:var(--green-dark)}
.card.custom{border:2px dashed #d8c9ae;background:transparent;box-shadow:none}
.custom-body{height:100%;min-height:380px;display:flex;flex-direction:column;align-items:center;justify-content:center;gap:12px;text-align:center;padding:32px 24px}
.custom-emoji{font-size:3rem}
.custom-body p{font-size:.85rem;color:var(--muted)}

/* ===== Why ===== */
.why{background:#fff;padding:80px 6%}
.why-grid{max-width:1100px;margin:auto;display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:24px}
.why-item{background:var(--cream);border-radius:20px;padding:30px 24px;text-align:center;transition:transform .3s}
.why-item:hover{transform:translateY(-6px)}
.icon{width:60px;height:60px;border-radius:50%;display:inline-flex;align-items:center;justify-content:center;font-size:1.6rem;margin-bottom:14px}
.i-yellow{background:var(--yellow-soft)} .i-green{background:var(--green-soft)}
.i-blue{background:var(--blue-soft)} .i-pink{background:var(--pink-soft)}
.why-item h3{font-size:1rem;margin-bottom:6px}
.why-item p{font-size:.85rem;color:var(--muted)}

/* ===== About ===== */
.about{display:grid;grid-template-columns:.9fr 1.1fr;gap:56px;align-items:center;max-width:1100px;margin:auto;padding:80px 6%}
.about-img img{width:100%;height:480px;object-fit:cover;border-radius:28px;box-shadow:var(--shadow);border:8px solid #fff}
.about-text h2{font-size:clamp(1.6rem,3vw,2.2rem);margin-bottom:16px}
.about-text p{color:var(--muted);margin-bottom:14px}
.quote{margin-top:20px;background:var(--yellow-soft);border-left:5px solid var(--yellow);border-radius:14px;padding:18px 22px;font-family:'Mitr';color:#7a5a1a;font-size:.95rem}

/* ===== Steps ===== */
.steps{padding:80px 6%}
.steps-grid{max-width:1100px;margin:auto;display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:22px}
.step{background:#fff;border-radius:20px;padding:28px 22px;text-align:center;box-shadow:var(--shadow)}
.step span{width:46px;height:46px;border-radius:50%;background:var(--yellow);color:#6b4e0e;font-family:'Mitr';font-weight:600;font-size:1.2rem;display:inline-flex;align-items:center;justify-content:center;margin-bottom:12px}
.step h3{font-size:1rem;margin-bottom:6px}
.step p{font-size:.85rem;color:var(--muted)}

/* ===== Contact ===== */
.contact{padding:20px 6% 90px}
.contact-card{max-width:1000px;margin:auto;background:linear-gradient(135deg,var(--green),#8FBC74);border-radius:32px;padding:56px 8%;text-align:center;color:#fff;box-shadow:0 18px 40px rgba(106,153,78,.35)}
.contact-card h2{font-size:clamp(1.5rem,3vw,2.1rem)}
.contact-card p{margin:10px 0 26px;opacity:.92}
.contact-btns{display:flex;gap:14px;justify-content:center;flex-wrap:wrap}
.btn-white{background:#fff;color:var(--green-dark)}
.btn-white:hover{transform:translateY(-3px)}
.btn-outline-w{border:2px solid rgba(255,255,255,.75);color:#fff}
.btn-outline-w:hover{background:rgba(255,255,255,.15)}

footer{background:#fff;border-top:1px solid #f0e6d6;padding:26px;text-align:center;color:var(--muted);font-size:.88rem}

/* ===== Reveal animation ===== */
.reveal{opacity:0;transform:translateY(26px);transition:opacity .7s ease,transform .7s ease}
.reveal.show{opacity:1;transform:none}
.why-item:nth-child(2),.step:nth-child(2),.grid .card:nth-child(even){transition-delay:.1s}
.why-item:nth-child(3),.step:nth-child(3){transition-delay:.2s}
.why-item:nth-child(4),.step:nth-child(4){transition-delay:.3s}

/* ===== Responsive ===== */
@media(max-width:880px){
  .nav-toggle{display:block}
  .nav-links{display:none;position:absolute;top:100%;left:6%;right:6%;background:#fff;flex-direction:column;gap:16px;padding:20px;border-radius:18px;box-shadow:var(--shadow)}
  .nav-links.open{display:flex}
  .hero{grid-template-columns:1fr;padding-top:36px}
  .hero-img{order:-1}
  .about{grid-template-columns:1fr}
  .about-img img{height:360px}
}
</style>

<!-- 🌻 แม่ตา Craft & Flower -->
<header class="navbar" id="navbar">
  <a href="#home" class="logo">🌻 แม่ตา <span>CRAFT &amp; FLOWER</span></a>
  <nav class="nav-links" id="navLinks">
    <a href="#home">หน้าแรก</a>
    <a href="#products">สินค้า</a>
    <a href="#why">ทำไมต้องเรา</a>
    <a href="#about">เรื่องราวของเรา</a>
    <a href="#contact">ติดต่อ</a>
  </nav>
  <button class="nav-toggle" id="navToggle" aria-label="เปิดเมนู">☰</button>
</header>

<!-- ============ HERO ============ -->
<section class="hero" id="home">
  <div class="hero-text reveal">
    <span class="badge">🧶 แฮนด์เมด • ทุกช่อมีหนึ่งเดียวในโลก</span>
    <h1>ดอกไม้กำมะหยี่ถัก<br>ด้วย<em>ความรัก</em>เพื่อคุณ</h1>
    <p>ทานตะวัน ทิวลิป เดซี่ — ทุกกลีบถักทออย่างตั้งใจด้วยมือของแม่
       ไม่เหี่ยวเฉา เก็บไว้ได้หลายปี เหมาะเป็นของขวัญให้คนพิเศษ</p>
    <div class="hero-cta">
      <a href="#products" class="btn btn-primary">ชมสินค้าทั้งหมด</a>
      <a href="#about" class="btn btn-ghost">เรื่องราวของเรา</a>
    </div>
    <div class="hero-stats">
      <div class="stat"><b>100+</b><span>ชิ้นงานที่ส่งมอบ</span></div>
      <div class="stat"><b>100%</b><span>ทำมือทุกขั้นตอน</span></div>
      <div class="stat"><b>∞</b><span>ปีไม่มีเหี่ยว</span></div>
    </div>
  </div>
  <div class="hero-img reveal">
    <img src="https://i.ibb.co/HTzvHYKc/IMG-3733.jpg" alt="กระถางดอกทานตะวันกำมะหยี่">
    <div class="float-card fc1">🌼 ไม่เหี่ยว ไม่ต้องรดน้ำ</div>
    <div class="float-card fc2">💛 ถักด้วยมือโดยแม่</div>
  </div>
</section>

<div class="marquee"><div class="marquee-track">
  <span>🌻 ทานตะวัน • 🌷 ทิวลิป • 🌼 เดซี่ • 💐 ช่อดอกไม้ • 🪴 กระถาง • 🎁 กล่องของขวัญ • 💌 การ์ดอวยพร •&nbsp;</span>
  <span aria-hidden="true">🌻 ทานตะวัน • 🌷 ทิวลิป • 🌼 เดซี่ • 💐 ช่อดอกไม้ • 🪴 กระถาง • 🎁 กล่องของขวัญ • 💌 การ์ดอวยพร •&nbsp;</span>
</div></div>

<!-- ============ สินค้า ============ -->
<section class="products" id="products">
  <div class="section-head reveal">
    <span class="kicker">Our Products</span>
    <h2>ทุกแบบ ถักด้วยใจ</h2>
    <p>เลือกแบบที่ชอบ หรือกำหนดสีเองได้ตามใจเลยนะ</p>
  </div>

  <div class="filter reveal">
    <button data-filter="all" class="active">ทั้งหมด</button>
    <button data-filter="pot">🪴 กระถาง</button>
    <button data-filter="bouquet">💐 ช่อดอกไม้</button>
    <button data-filter="box">🎁 กล่องของขวัญ</button>
    <button data-filter="card">💌 การ์ด</button>
  </div>

  <div class="grid">
    <article class="card reveal" data-cat="pot">
      <div class="thumb">
        <img src="https://i.ibb.co/HTzvHYKc/IMG-3733.jpg" alt="กระถางทานตะวัน">
        <span class="tag t-yellow">★ ขายดี</span>
      </div>
      <div class="card-body">
        <h3>แดดอุ่น — กระถางทานตะวัน</h3>
        <p class="desc">ทานตะวัน + ทิวลิปเหลือง + เดซี่ ในกระถางขาวผูกโบเขียว</p>
        <div class="card-foot"><span class="price">฿590</span><a class="btn-order" href="https://line.me/" target="_blank">สั่งซื้อ</a></div>
      </div>
    </article>

    <article class="card reveal" data-cat="box">
      <div class="thumb">
        <img src="https://i.ibb.co/CpkPmCZq/IMG-3735.jpg" alt="กล่องของขวัญทานตะวัน">
        <span class="tag t-green">กล่องของขวัญ</span>
      </div>
      <div class="card-body">
        <h3>ของขวัญพิเศษ — กล่องใส</h3>
        <p class="desc">กระถางทานตะวันในกล่องใสผูกโบริบบิ้น พร้อมมอบทันที</p>
        <div class="card-foot"><span class="price">฿890</span><a class="btn-order" href="https://line.me/" target="_blank">สั่งซื้อ</a></div>
      </div>
    </article>

    <article class="card reveal" data-cat="bouquet">
      <div class="thumb">
        <img src="https://i.ibb.co/TD27dvCb/IMG-3734.jpg" alt="ช่อดอกไม้สีฟ้า">
        <span class="tag t-blue">ช่อดอกไม้</span>
      </div>
      <div class="card-body">
        <h3>ท้องฟ้า — ช่อสีฟ้า</h3>
        <p class="desc">ทิวลิปฟ้า + ลิลลี่ + เดซี่ ห่อกระดาษน้ำเงิน-ขาว โบฟ้า</p>
        <div class="card-foot"><span class="price">฿690</span><a class="btn-order" href="https://line.me/" target="_blank">สั่งซื้อ</a></div>
      </div>
    </article>

    <article class="card reveal" data-cat="bouquet">
      <div class="thumb">
        <img src="https://i.ibb.co/rK44sXgs/IMG-3737.jpg" alt="ช่อดอกไม้สีชมพู">
        <span class="tag t-pink">ช่อดอกไม้</span>
      </div>
      <div class="card-body">
        <h3>ชมพูอุ่น — ช่อสีชมพู</h3>
        <p class="desc">กุหลาบ + ทิวลิปชมพู + เดซี่ ห่อกระดาษครีม-ชมพูหวาน</p>
        <div class="card-foot"><span class="price">฿650</span><a class="btn-order" href="https://line.me/" target="_blank">สั่งซื้อ</a></div>
      </div>
    </article>

    <article class="card reveal" data-cat="card">
      <div class="thumb">
        <img src="https://i.ibb.co/HTzvHYKc/IMG-3733.jpg" alt="การ์ดอวยพร">
        <span class="tag t-pink">การ์ด</span>
      </div>
      <div class="card-body">
        <h3>คำเล็กๆ — การ์ดดอกไม้</h3>
        <p class="desc">การ์ดทำมือประดับดอกทานตะวันถัก เขียนข้อความฟรี</p>
        <div class="card-foot"><span class="price">฿129</span><a class="btn-order" href="https://line.me/" target="_blank">สั่งซื้อ</a></div>
      </div>
    </article>

    <article class="card custom reveal">
      <div class="custom-body">
        <span class="custom-emoji">🧶</span>
        <h3>อยากได้แบบของตัวเอง?</h3>
        <p>บอกสีและไอเดียที่ชอบได้เลย แม่จะถักช่อเดียวในโลกให้คุณ</p>
        <a class="btn btn-primary" href="https://line.me/" target="_blank">คุยกับเรา</a>
      </div>
    </article>
  </div>
</section>

<!-- ============ จุดเด่น ============ -->
<section class="why" id="why">
  <div class="section-head reveal">
    <span class="kicker">Why Us</span>
    <h2>ทำไมต้องดอกไม้กำมะหยี่</h2>
  </div>
  <div class="why-grid">
    <div class="why-item reveal"><span class="icon i-yellow">🧶</span><h3>ทำมือทุกชิ้น</h3><p>ทุกกิ่งทุกกลีบถักด้วยมืออย่างประณีต</p></div>
    <div class="why-item reveal"><span class="icon i-green">🌼</span><h3>ไม่เหี่ยวเฉา</h3><p>เก็บได้หลายปี ไม่ต้องรดน้ำหรือโดนแดด</p></div>
    <div class="why-item reveal"><span class="icon i-blue">🎁</span><h3>พร้อมมอบ</h3><p>ห่อสวย แพ็กแน่น แถมการ์ดเขียนมือฟรี</p></div>
    <div class="why-item reveal"><span class="icon i-pink">💛</span><h3>ส่งต่อความรู้สึก</h3><p>จากครอบครัวของเรา (แม่) สู่ครอบครัวของคุณ</p></div>
  </div>
</section>

<!-- ============ เรื่องราว ============ -->
<section class="about" id="about">
  <div class="about-img reveal">
    <img src="https://i.ibb.co/rK44sXgs/IMG-3737.jpg" alt="เรื่องราวของเรา">
  </div>
  <div class="about-text reveal">
    <span class="kicker">Our Story</span>
    <h2>เริ่มต้นจากงานอดิเรกของแม่</h2>
    <p>แม่ตา Craft & Flower เริ่มจากงานอดิเรกของแม่ที่ชอบงานฝีมือ
       จากกระถางดอกไม้กำมะหยี่ใบแรกบนโต๊ะอาหาร กลายเป็นร้านเล็กๆ ที่อบอุ่น</p>
    <p>ทุกกิ่งแม่เป็นคนถักเองกับมือ ดังนั้นทุกช่อจึงไม่ใช่แค่สวย
       แต่เต็มไปด้วยความรักจริงใจ พร้อมส่งต่อให้คนพิเศษของคุณ</p>
    <div class="quote">"ดอกไม้อาจไม่ใช่ของขวัญที่แพงที่สุด<br>แต่เราทำด้วยใจที่มากที่สุด" — แม่</div>
  </div>
</section>

<!-- ============ วิธีสั่ง ============ -->
<section class="steps">
  <div class="section-head reveal">
    <span class="kicker">How to Order</span>
    <h2>สั่งง่ายใน 4 ขั้นตอน</h2>
  </div>
  <div class="steps-grid">
    <div class="step reveal"><span>1</span><h3>เลือกแบบ</h3><p>เลือกจากร้าน หรือส่งรูปอ้างอิงมา</p></div>
    <div class="step reveal"><span>2</span><h3>เลือกสี</h3><p>บอกสีที่ชอบและงบที่ต้องการ</p></div>
    <div class="step reveal"><span>3</span><h3>แม่ถักให้</h3><p>ใช้เวลาถักอย่างตั้งใจ 3–5 วัน</p></div>
    <div class="step reveal"><span>4</span><h3>ส่งถึงมือ</h3><p>แพ็กสวยงาม ส่งถึงบ้านทั่วไทย</p></div>
  </div>
</section>

<!-- ============ ติดต่อ ============ -->
<section class="contact" id="contact">
  <div class="contact-card reveal">
    <h2>พร้อมส่งต่อความรักให้คนพิเศษหรือยัง 💌</h2>
    <p>สั่งสินค้าหรือสอบถามเพิ่มเติมได้ที่ "แม่ตา Craft & Flower"</p>
    <div class="contact-btns">
      <a class="btn btn-white" href="https://line.me/" target="_blank">💬 สั่งผ่าน Line</a>
      <a class="btn btn-outline-w" href="#" target="_blank">📘 Facebook Page</a>
    </div>
  </div>
</section>

<footer>
  <p>© <span id="year"></span> แม่ตา Craft & Flower — ทำด้วย 💛 เพื่อแม่</p>
</footer>

<script>
// ปีปัจจุบันใน footer
document.getElementById('year').textContent = new Date().getFullYear();

// เงา navbar ตอนเลื่อนจอ
const navbar = document.getElementById('navbar');
window.addEventListener('scroll', () => navbar.classList.toggle('scrolled', window.scrollY > 10));

// เมนูมือถือ
const navToggle = document.getElementById('navToggle');
const navLinks = document.getElementById('navLinks');
navToggle.addEventListener('click', () => navLinks.classList.toggle('open'));
navLinks.querySelectorAll('a').forEach(a => a.addEventListener('click', () => navLinks.classList.remove('open')));

// ปุ่มกรองหมวดสินค้า
const filterBtns = document.querySelectorAll('.filter button');
const cards = document.querySelectorAll('.grid .card');
filterBtns.forEach(btn => btn.addEventListener('click', () => {
  filterBtns.forEach(b => b.classList.remove('active'));
  btn.classList.add('active');
  const f = btn.dataset.filter;
  cards.forEach(c => {
    if (c.classList.contains('custom')) return;
    c.classList.toggle('hide', f !== 'all' && c.dataset.cat !== f);
  });
}));

// อนิเมชั่นค่อยๆ โผล่เมื่อเลื่อนจอ
const io = new IntersectionObserver(entries => {
  entries.forEach(e => {
    if (e.isIntersecting) { e.target.classList.add('show'); io.unobserve(e.target); }
  });
}, { threshold: 0.12 });
document.querySelectorAll('.reveal').forEach(el => io.observe(el));
</script>
