#   
<!doctype html>  
<html lang="en">  
<head>  
  <meta charset="utf-8" />  
  <meta name="viewport" content="width=device-width,initial-scale=1" />  
  <title>💘 Valentine Invite</title>  
  <style>  
    :root{  
      --bg1:#ff5aa5;  
      --bg2:#7c4dff;  
      --bg3:#00d4ff;  
      --card: rgba(255,255,255,.16);  
      --card2: rgba(255,255,255,.10);  
      --text: rgba(255,255,255,.95);  
      --muted: rgba(255,255,255,.78);  
      --shadow: 0 22px 70px rgba(0,0,0,.25);  
      --radius: 22px;  
    }  
  
    * { box-sizing: border-box; }  
    html,body { height: 100%; margin:0; font-family: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Arial; }  
    body{  
      overflow:hidden;  
      color: var(--text);  
      background: radial-gradient(1200px 800px at 15% 10%, rgba(255,255,255,.18), transparent 55%),  
                  radial-gradient(900px 650px at 80% 25%, rgba(255,255,255,.12), transparent 60%),  
                  linear-gradient(120deg, var(--bg1), var(--bg2), var(--bg3));  
      background-size: 200% 200%;  
      animation: bgShift 10s ease-in-out infinite;  
    }  
    @keyframes bgShift {  
      0% { background-position: 0% 40%; }  
      50% { background-position: 100% 60%; }  
      100% { background-position: 0% 40%; }  
    }  
  
    /* Subtle sparkle layer */  
    .sparkles{  
      position:fixed; inset:0;  
      background-image:  
        radial-gradient(circle at 20% 30%, rgba(255,255,255,.25) 0 2px, transparent 3px),  
        radial-gradient(circle at 70% 20%, rgba(255,255,255,.20) 0 1.5px, transparent 2.5px),  
        radial-gradient(circle at 60% 70%, rgba(255,255,255,.18) 0 1.8px, transparent 3px),  
        radial-gradient(circle at 30% 80%, rgba(255,255,255,.22) 0 2px, transparent 3px);  
      opacity:.55;  
      filter: blur(.2px);  
      animation: twinkle 3.2s ease-in-out infinite alternate;  
      pointer-events:none;  
    }  
    @keyframes twinkle { from{opacity:.35} to{opacity:.65} }  
  
    /* Floating hearts */  
    .hearts {  
      position: fixed; inset:0;  
      pointer-events:none;  
      overflow:hidden;  
    }  
    .heart {  
      position:absolute;  
      width: 18px; height: 18px;  
      transform: rotate(45deg);  
      opacity: .8;  
      animation: floatUp linear forwards;  
      filter: drop-shadow(0 10px 10px rgba(0,0,0,.18));  
    }  
    .heart:before, .heart:after{  
      content:"";  
      position:absolute;  
      width: 18px; height: 18px;  
      border-radius: 50%;  
      background: currentColor;  
    }  
    .heart { background: currentColor; }  
    .heart:before { left: -9px; top: 0; }  
    .heart:after  { left: 0; top: -9px; }  
  
    @keyframes floatUp {  
      from { transform: translateY(0) rotate(45deg) scale(var(--s,1)); opacity: 0; }  
      10%  { opacity: .9; }  
      to   { transform: translateY(-120vh) rotate(45deg) scale(var(--s,1)); opacity: 0; }  
    }  
  
    /* Center card */  
    .wrap{  
      position:relative;  
      height:100%;  
      display:grid;  
      place-items:center;  
      padding: 24px;  
    }  
    .card{  
      width:min(560px, 92vw);  
      background: linear-gradient(180deg, var(--card), var(--card2));  
      border: 1px solid rgba(255,255,255,.22);  
      border-radius: var(--radius);  
      box-shadow: var(--shadow);  
      backdrop-filter: blur(14px);  
      padding: 26px 22px 22px;  
      text-align:center;  
      position:relative;  
      overflow:hidden;  
    }  
    .badge{  
      display:inline-flex;  
      gap:10px;  
      align-items:center;  
      padding: 9px 14px;  
      border-radius: 999px;  
      background: rgba(255,255,255,.14);  
      border: 1px solid rgba(255,255,255,.22);  
      font-size: 14px;  
      color: var(--muted);  
    }  
    .badge b{ color: var(--text); }  
  
    h1{  
      margin: 16px 0 10px;  
      font-size: clamp(28px, 4vw, 40px);  
      letter-spacing: .2px;  
      text-shadow: 0 10px 25px rgba(0,0,0,.20);  
    }  
    .sub{  
      margin: 0 auto 18px;  
      max-width: 46ch;  
      color: var(--muted);  
      line-height: 1.35;  
      font-size: 15.5px;  
    }  
  
    .question{  
      font-size: clamp(22px, 3.4vw, 30px);  
      margin: 12px 0 18px;  
      font-weight: 800;  
    }  
  
    .btns{  
      display:flex;  
      gap: 12px;  
      justify-content:center;  
      align-items:center;  
      flex-wrap: wrap;  
      margin-top: 6px;  
    }  
    button{  
      appearance:none;  
      border:none;  
      cursor:pointer;  
      border-radius: 14px;  
      padding: 12px 18px;  
      font-weight: 800;  
      font-size: 16px;  
      transition: transform .12s ease, filter .12s ease, background .2s ease;  
      box-shadow: 0 16px 35px rgba(0,0,0,.22);  
      user-select:none;  
    }  
    button:active{ transform: translateY(1px) scale(.99); }  
    .yes{  
      background: rgba(255,255,255,.92);  
      color:#ff2d7a;  
      min-width: 140px;  
    }  
    .yes:hover{ filter: brightness(1.03); transform: translateY(-1px); }  
    .no{  
      background: rgba(20,20,35,.35);  
      color: rgba(255,255,255,.92);  
      border: 1px solid rgba(255,255,255,.18);  
      min-width: 120px;  
      position: relative;  
    }  
    .no:hover{ filter: brightness(1.05); transform: translateY(-1px); }  
  
    .footer{  
      margin-top: 16px;  
      font-size: 12.5px;  
      color: rgba(255,255,255,.68);  
    }  
  
    /* Modal */  
    .modalOverlay{  
      position:fixed; inset:0;  
      background: rgba(0,0,0,.42);  
      display:none;  
      align-items:center;  
      justify-content:center;  
      padding: 22px;  
      z-index: 50;  
    }  
    .modal{  
      width:min(520px, 94vw);  
      background: rgba(255,255,255,.12);  
      border: 1px solid rgba(255,255,255,.22);  
      border-radius: 18px;  
      padding: 18px 16px 14px;  
      backdrop-filter: blur(16px);  
      box-shadow: var(--shadow);  
    }  
    .modal h2{  
      margin: 6px 0 6px;  
      font-size: 20px;  
    }  
    .modal p{  
      margin: 0 0 12px;  
      color: rgba(255,255,255,.82);  
      line-height: 1.35;  
    }  
    .modal .row{  
      display:flex;  
      gap:10px;  
      justify-content:flex-end;  
      flex-wrap:wrap;  
    }  
    .tiny{  
      background: rgba(255,255,255,.9);  
      color:#382a5a;  
      box-shadow:none;  
      padding: 10px 14px;  
      border-radius: 12px;  
      font-size: 14px;  
      font-weight: 800;  
    }  
  
    /* Celebration state */  
    .hidden { display:none !important; }  
    .bigLove{  
      font-size: clamp(26px, 4vw, 44px);  
      font-weight: 900;  
      margin: 14px 0 6px;  
      text-shadow: 0 10px 30px rgba(0,0,0,.25);  
    }  
    .loveNote{  
      margin: 0 auto;  
      max-width: 52ch;  
      font-size: 16px;  
      color: rgba(255,255,255,.88);  
      line-height: 1.4;  
    }  
  
    /* Canvas overlay */  
    canvas{  
      position:fixed;  
      inset:0;  
      z-index: 40;  
      pointer-events:none;  
    }  
  
    /* Small “pulse” heart icon */  
    .pulse{  
      display:inline-block;  
      animation: pulse 1.2s ease-in-out infinite;  
    }  
    @keyframes pulse {  
      0%,100%{ transform: scale(1); }  
      50%{ transform: scale(1.15); }  
    }  
  
    /* Mobile spacing */  
    @media (max-width: 420px){  
      .btns{ gap:10px; }  
      button{ width: 100%; }  
      .yes,.no{ min-width: unset; }  
    }  
  </style>  
</head>  
  
<body>  
  <div class="sparkles"></div>  
  <div class="hearts" id="hearts"></div>  
  <canvas id="fx"></canvas>  
  
  <div class="wrap">  
    <div class="card" id="card">  
      <div class="badge">  
        <span class="pulse">💘</span>  
        <span>To <b id="toName">my favourite person</b> • From <b id="fromName">your admirer</b></span>  
      </div>  
  
      <h1 id="headline">Open me 💌</h1>  
      <p class="sub" id="subline">  
        I made this tiny little page because you deserve something cute, personal, and slightly dramatic.  
      </p>  
  
      <div id="askBlock">  
        <div class="question" id="question">Will you be my Valentine?</div>  
        <div class="btns">  
          <button class="yes" id="yesBtn">Yes 💖</button>  
          <button class="no" id="noBtn">No 🙈</button>  
        </div>  
        <div class="footer" id="footer">  
          (P.S. This link is just for you. Try clicking… 😌)  
        </div>  
      </div>  
  
      <div id="yayBlock" class="hidden">  
        <div class="bigLove" id="yayTitle">YAAAY!! 💞</div>  
        <p class="loveNote" id="yayNote">  
          You just made my whole day. I can’t wait to spoil you and make you feel ridiculously loved.  
          <br><br>  
          <b>Happy Valentine’s, my love.</b> 🌹  
        </p>  
      </div>  
    </div>  
  </div>  
  
  <!-- Modal -->  
  <div class="modalOverlay" id="modalOverlay" aria-hidden="true">  
    <div class="modal" role="dialog" aria-modal="true" aria-labelledby="mTitle">  
      <h2 id="mTitle">Wait… 😭</h2>  
      <p id="mBody">Are you sure? I prepared premium cuddles and elite snacks.</p>  
      <div class="row">  
        <button class="tiny" id="closeModal">Okay okay… try again</button>  
      </div>  
    </div>  
  </div>  
  
  <script>  
    // ---- Personalisation via URL ----  
    // Example link:  
    // https://your-site.com/?to=Ayesha&from=Hassan  
    const params = new URLSearchParams(location.search);  
    const to = (params.get("to") || "my favourite person").trim();  
    const from = (params.get("from") || "your admirer").trim();  
  
    const toName = document.getElementById("toName");  
    const fromName = document.getElementById("fromName");  
    const headline = document.getElementById("headline");  
    const subline = document.getElementById("subline");  
    const question = document.getElementById("question");  
  
    toName.textContent = to;  
    fromName.textContent = from;  
  
    headline.textContent = `Hey ${to} 💘`;  
    subline.textContent = `I have an important question for you… (Answer carefully, ${to} 😌)`;  
    question.textContent = `Will you be my Valentine, ${to}?`;  
  
    // ---- Floating hearts background ----  
    const heartsWrap = document.getElementById("hearts");  
    function spawnBgHeart(){  
      const h = document.createElement("div");  
      h.className = "heart";  
      const left = Math.random() * 100;  
      const dur = 6 + Math.random() * 7;  
      const size = 0.7 + Math.random() * 1.6;  
  
      const colors = ["#fff", "#ffd1e8", "#ffecf7", "#ffe8a6", "#e7d7ff", "#d7fbff"];  
      h.style.color = colors[Math.floor(Math.random()*colors.length)];  
      h.style.left = left + "vw";  
      h.style.bottom = (-10 - Math.random()*20) + "vh";  
      h.style.animationDuration = dur + "s";  
      h.style.setProperty("--s", size.toFixed(2));  
  
      heartsWrap.appendChild(h);  
      setTimeout(()=> h.remove(), dur*1000);  
    }  
    setInterval(spawnBgHeart, 260);  
    for(let i=0;i<14;i++) setTimeout(spawnBgHeart, i*120);  
  
    // ---- Modal logic for "No" ----  
    const modalOverlay = document.getElementById("modalOverlay");  
    const mBody = document.getElementById("mBody");  
    const closeModal = document.getElementById("closeModal");  
  
    const noBtn = document.getElementById("noBtn");  
    const yesBtn = document.getElementById("yesBtn");  
  
    let noCount = 0;  
  
    const noLines = [  
      (t)=> `Ouch… my heart just did a tiny backflip. 💔 Try again, ${t}?`,  
      (t)=> `Declined?! I literally prepared “princess treatment” DLC for you. 👑`,  
      (t)=> `Okay but… imagine: snacks, flowers, and you looking stunning. Still no? 😭`,  
      (t)=> `I’m filing an appeal to the Supreme Court of ${t}. Verdict: you’re too cute to say no. 🧑‍⚖️`,  
      (t)=> `This “No” button is acting suspicious. Are you sure you meant that, ${t}? 😌`,  
      (t)=> `Final offer: unlimited hugs + your favourite dessert + a perfect date. 🥺`,  
    ];  
  
    function openModal(text){  
      mBody.textContent = text;  
      modalOverlay.style.display = "flex";  
      modalOverlay.setAttribute("aria-hidden","false");  
    }  
    function closeIt(){  
      modalOverlay.style.display = "none";  
      modalOverlay.setAttribute("aria-hidden","true");  
    }  
    closeModal.addEventListener("click", closeIt);  
    modalOverlay.addEventListener("click", (e)=> { if(e.target === modalOverlay) closeIt(); });  
  
    noBtn.addEventListener("click", ()=>{  
      noCount++;  
      const line = noLines[Math.min(noCount-1, noLines.length-1)](to);  
      openModal(line);  
  
      // Make "Yes" slightly more tempting (playful, not forcing)  
      const grow = Math.min(1.0 + noCount*0.08, 1.45);  
      yesBtn.style.transform = `scale(${grow})`;  
  
      // Optional playful move after multiple "No"s  
      if(noCount >= 3){  
        jiggleButton(noBtn);  
      }  
      // After many "No"s, change question copy (still allows No)  
      if(noCount === 4){  
        question.textContent = `Pretty please, ${to}? 🥺 Will you be my Valentine?`;  
      }  
      if(noCount === 6){  
        question.textContent = `Okay last time asking… (not really) 😇 Valentine, ${to}?`;  
      }  
    });  
  
    function jiggleButton(btn){  
      btn.animate(  
        [  
          { transform: "translateX(0px)" },  
          { transform: "translateX(-5px)" },  
          { transform: "translateX(5px)" },  
          { transform: "translateX(-3px)" },  
          { transform: "translateX(0px)" }  
        ],  
        { duration: 320, easing: "ease-in-out" }  
      );  
    }  
  
    // ---- YES celebration: confetti + heart shower ----  
    const askBlock = document.getElementById("askBlock");  
    const yayBlock = document.getElementById("yayBlock");  
    const yayTitle = document.getElementById("yayTitle");  
    const yayNote = document.getElementById("yayNote");  
  
    const canvas = document.getElementById("fx");  
    const ctx = canvas.getContext("2d");  
    let W, H;  
    function resize(){  
      W = canvas.width = window.innerWidth * devicePixelRatio;  
      H = canvas.height = window.innerHeight * devicePixelRatio;  
    }  
    window.addEventListener("resize", resize);  
    resize();  
  
    let particles = [];  
    function rand(min,max){ return Math.random()*(max-min)+min; }  
  
    function burstConfetti(){  
      const count = 180;  
      for(let i=0;i<count;i++){  
        particles.push({  
          x: rand(0,W),  
          y: rand(-40, H*0.35),  
          vx: rand(-2.5,2.5)*devicePixelRatio,  
          vy: rand(1.5,5.0)*devicePixelRatio,  
          r: rand(3,6)*devicePixelRatio,  
          rot: rand(0,Math.PI*2),  
          vr: rand(-0.12,0.12),  
          life: rand(80,140),  
          kind: Math.random() < 0.55 ? "heart" : "confetti",  
          hue: rand(0,360)  
        });  
      }  
    }  
  
    function drawHeart(x,y,s,rot){  
      ctx.save();  
      ctx.translate(x,y);  
      ctx.rotate(rot);  
      ctx.scale(s,s);  
      ctx.beginPath();  
      ctx.moveTo(0, -6);  
      ctx.bezierCurveTo(8,-14, 18,-4, 0, 12);  
      ctx.bezierCurveTo(-18,-4, -8,-14, 0, -6);  
      ctx.closePath();  
      ctx.fill();  
      ctx.restore();  
    }  
  
    function loop(){  
      ctx.clearRect(0,0,W,H);  
      for(let i=particles.length-1;i>=0;i--){  
        const p = particles[i];  
        p.x += p.vx;  
        p.y += p.vy;  
        p.vy += 0.035*devicePixelRatio;  
        p.rot += p.vr;  
        p.life -= 1;  
  
        const alpha = Math.min(1, p.life/40);  
        ctx.globalAlpha = alpha;  
  
        if(p.kind === "confetti"){  
          ctx.fillStyle = `hsla(${p.hue}, 95%, 70%, 1)`;  
          ctx.save();  
          ctx.translate(p.x,p.y);  
          ctx.rotate(p.rot);  
          ctx.fillRect(-p.r, -p.r, p.r*2, p.r*1.4);  
          ctx.restore();  
        } else {  
          ctx.fillStyle = `hsla(${p.hue}, 95%, 78%, 1)`;  
          drawHeart(p.x,p.y, p.r/6, p.rot);  
        }  
  
        if(p.life <= 0 || p.y > H + 80){  
          particles.splice(i,1);  
        }  
      }  
      ctx.globalAlpha = 1;  
      requestAnimationFrame(loop);  
    }  
    loop();  
  
    function showerHearts(durationMs=2500){  
      const start = performance.now();  
      const timer = setInterval(()=>{  
        // spawn a few bigger hearts foreground  
        for(let i=0;i<8;i++){  
          const h = document.createElement("div");  
          h.className = "heart";  
          const left = 10 + Math.random()*80;  
          const dur = 2.6 + Math.random()*2.2;  
          const size = 1.6 + Math.random()*2.6;  
          const colors = ["#ffffff","#ffd1e8","#ff87c2","#ffe8a6","#d7fbff"];  
          h.style.color = colors[Math.floor(Math.random()*colors.length)];  
          h.style.left = left + "vw";  
          h.style.bottom = (-10 - Math.random()*15) + "vh";  
          h.style.animationDuration = dur + "s";  
          h.style.setProperty("--s", size.toFixed(2));  
          heartsWrap.appendChild(h);  
          setTimeout(()=> h.remove(), dur*1000);  
        }  
        if(performance.now() - start > durationMs){  
          clearInterval(timer);  
        }  
      }, 140);  
    }  
  
    yesBtn.addEventListener("click", ()=>{  
      closeIt();  
  
      askBlock.classList.add("hidden");  
      yayBlock.classList.remove("hidden");  
  
      yayTitle.textContent = `She said YES!! 💖`;  
      yayNote.innerHTML = `  
        <b>${to}</b>, you just made me the happiest person ever.  
        <br><br>  
        Tonight: love, laughter, and me making sure you feel <i>properly</i> adored.  
        <br><br>  
        Love, <b>${from}</b> 🌹  
      `;  
  
      burstConfetti();  
      showerHearts(3200);  
  
      // Extra bursts for drama  
      setTimeout(burstConfetti, 450);  
      setTimeout(burstConfetti, 900);  
    });  
  </script>  
</body>  
</html>  
