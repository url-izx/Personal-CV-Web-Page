<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Earl Laurence Masana — CV</title>
<style>
  :root{
    --paper:#f1efe9; --ink:#15171a; --sub:#5b5d5f;
    --accent:#3d4b94; --accent-soft:#e2e5f2; --sage:#7c9473; --line:#d9d6cc;
    --card:#ffffff;
  }
  @media (prefers-color-scheme: dark){
    :root:not([data-theme="light"]){
      --paper:#121316; --ink:#efeee9; --sub:#a3a29c;
      --accent:#8f9de8; --accent-soft:#242847; --sage:#9db894; --line:#2c2d30;
      --card:#1a1b1e;
    }
  }
  :root[data-theme="dark"]{
    --paper:#121316; --ink:#efeee9; --sub:#a3a29c;
    --accent:#8f9de8; --accent-soft:#242847; --sage:#9db894; --line:#2c2d30;
    --card:#1a1b1e;
  }
  *{box-sizing:border-box}
  html{height:100%; scroll-padding-top:env(safe-area-inset-top,0px)}
  body{
    margin:0; min-height:100%; background:var(--paper); color:var(--ink);
    font-family:Helvetica,Arial,sans-serif;
    padding-top:env(safe-area-inset-top,0px);
    padding-bottom:env(safe-area-inset-bottom,0px);
  }
  .layout{
    display:grid; grid-template-columns:280px 1fr; max-width:980px; margin:0 auto;
    min-height:100vh; align-items:start;
  }
  .side{position:relative;}
  @media (max-width:720px){ .layout{grid-template-columns:1fr;} .side{position:static !important;} }

  .side{
    position:sticky; top:0; padding:56px 32px 40px 24px; height:100vh;
    display:flex; flex-direction:column; justify-content:space-between;
    overflow:hidden;
  }
  .side::before{
    content:""; position:absolute; width:260px; height:260px; border-radius:50%;
    background:radial-gradient(circle, var(--accent-soft) 0%, transparent 70%);
    left:var(--glow-x, -80px); top:var(--glow-y, -80px);
    pointer-events:none; z-index:0; transition:left 260ms ease, top 260ms ease;
  }
  .side > *{position:relative; z-index:1;}
  .name{
    font-family:Georgia,'Iowan Old Style',serif; font-size:2.1rem; line-height:1.15;
    margin:0 0 6px; letter-spacing:0.2px;
  }
  .title{color:var(--accent); font-weight:600; font-size:0.95rem; margin:0 0 22px;}
  .blurb{color:var(--sub); font-size:0.92rem; line-height:1.6; max-width:34ch;}

  .contact-block{margin-top:28px;}
  .contact-row{
    display:flex; align-items:center; gap:10px; margin-bottom:10px;
    font-size:0.88rem;
  }
  .contact-row a, .contact-row span{color:var(--ink); text-decoration:none;}
  .copy-btn{
    border:1px solid var(--line); background:var(--card); color:var(--sub);
    border-radius:6px; padding:4px 9px; font-size:0.72rem; cursor:pointer;
    font-family:inherit; transition:background 120ms ease, color 120ms ease;
  }
  .copy-btn:hover{background:var(--accent-soft); color:var(--accent);}
  .copy-btn:focus-visible{outline:2px solid var(--accent); outline-offset:2px;}
  .copy-btn.done{color:var(--sage); border-color:var(--sage);}

  .nav-tabs{margin-top:auto; padding-top:24px; border-top:1px solid var(--line);}
  .nav-tabs button{
    display:block; width:100%; text-align:left; background:none; border:none;
    padding:7px 0; font-family:inherit; font-size:0.85rem; color:var(--sub);
    cursor:pointer; position:relative; padding-left:16px;
  }
  .nav-tabs button::before{
    content:""; position:absolute; left:0; top:12px; width:6px; height:6px;
    border-radius:50%; background:var(--line);
    transition:background 150ms ease, transform 150ms ease, box-shadow 150ms ease;
  }
  .nav-tabs button.active{color:var(--ink); font-weight:600;}
  .nav-tabs button.active::before{
    background:var(--accent); transform:scale(1.4);
    box-shadow:0 0 0 4px var(--accent-soft);
  }

  .main{padding:64px 32px 80px 40px; border-left:1px solid var(--line);}
  @media (max-width:720px){ .main{border-left:none; padding:16px 24px 60px;} }

  section{margin-bottom:52px; opacity:0; transform:translateY(10px); animation:rise 500ms ease forwards;}
  section:nth-of-type(1){animation-delay:60ms}
  section:nth-of-type(2){animation-delay:140ms}
  section:nth-of-type(3){animation-delay:220ms}
  @keyframes rise{ to{opacity:1; transform:translateY(0);} }
  @media (prefers-reduced-motion: reduce){ section{animation:none; opacity:1; transform:none;} }

  h2{
    font-size:0.78rem; letter-spacing:1.5px; text-transform:uppercase;
    color:var(--sub); margin:0 0 20px; font-weight:700;
  }
  .item{
    display:grid; grid-template-columns:1fr; gap:4px; padding:18px 20px;
    background:var(--card); border:1px solid var(--line); border-radius:10px; margin-bottom:14px;
    transition:transform 220ms cubic-bezier(.2,.8,.2,1), box-shadow 220ms ease, border-color 220ms ease;
  }
  .item:hover{
    transform:translateY(-3px);
    box-shadow:0 14px 28px -18px rgba(0,0,0,0.35);
    border-color:var(--accent);
  }
  .item-title{font-weight:700; font-size:1.02rem;}
  .item-meta{color:var(--sub); font-size:0.85rem;}
  .item-desc{margin-top:6px; line-height:1.55; font-size:0.92rem; color:var(--ink);}

  .skills{display:flex; flex-wrap:wrap; gap:9px;}
  .skill{
    background:var(--accent-soft); color:var(--accent); padding:7px 13px;
    border-radius:999px; font-size:0.83rem; font-weight:600;
    transition:transform 160ms ease, background 160ms ease;
  }
  .skill:hover{ transform:scale(1.06); background:var(--accent); color:var(--card); }

  footer{color:var(--sub); font-size:0.76rem; margin-top:8px;}
</style>
</head>
<body>
<div class="layout">
  <aside class="side">
    <div>
      <h1 class="name">Earl Laurence<br>Masana</h1>
      <p class="title">Information Technology</p>
      <p class="blurb">
        Curious, detail-oriented IT graduate who enjoys turning ambiguous problems
        into simple, well-built solutions.
      </p>
      <div class="contact-block">
        <div class="contact-row">
          <span id="email-text">earlmasana1@gmail.com</span>
          <button class="copy-btn" id="copy-email">Copy</button>
        </div>
        <div class="contact-row"><span>Panabo Davao, Philippines</span></div>
      </div>
    </div>
    <nav class="nav-tabs" id="nav-tabs">
      <button data-target="education" class="active">Education</button>
      <button data-target="skills">Skills</button>
      <button data-target="contact">Contact</button>
    </nav>
  </aside>

  <main class="main">
    <section id="education">
      <h2>Education</h2>
      <div class="item">
        <div class="item-title">Bachelor of Science in Information Technology (BSIT)</div>
        <div class="item-meta">Davao del Norte State College</div>
      </div>
    </section>

    <section id="skills">
      <h2>Skills</h2>
      <div class="skills">
        <span class="skill">JavaScript</span>
        <span class="skill">Python</span>
        <span class="skill">HTML &amp; CSS</span>
        <span class="skill">SQL</span>
        <span class="skill">Git</span>
        <span class="skill">Problem Solving</span>
      </div>
    </section>

    <section id="contact">
      <h2>Contact</h2>
      <div class="item">
        <div class="item-desc">Reach out anytime by emailSS happy to talk about opportunities, projects, or a quick chat.</div>
      </div>
      <footer>Update skills and blurb to match your experience.</footer>
    </section>
  </main>
</div>

<script>
  // Sidebar glow follows cursor
  const side = document.querySelector('.side');
  side.addEventListener('mousemove', (e) => {
    const rect = side.getBoundingClientRect();
    side.style.setProperty('--glow-x', (e.clientX - rect.left - 130) + 'px');
    side.style.setProperty('--glow-y', (e.clientY - rect.top - 130) + 'px');
  });

  // Copy email to clipboard
  const copyBtn = document.getElementById('copy-email');
  copyBtn.addEventListener('click', async () => {
    const email = document.getElementById('email-text').textContent;
    try {
      await navigator.clipboard.writeText(email);
    } catch (e) {
      // fallback: select text silently fails gracefully, no UI break
    }
    copyBtn.textContent = 'Copied';
    copyBtn.classList.add('done');
    setTimeout(() => {
      copyBtn.textContent = 'Copy';
      copyBtn.classList.remove('done');
    }, 1500);
  });

  // Scroll-spy nav tabs
  const sections = document.querySelectorAll('main section');
  const tabs = document.querySelectorAll('.nav-tabs button');
  const setActive = (id) => {
    tabs.forEach(t => t.classList.toggle('active', t.dataset.target === id));
  };
  tabs.forEach(t => t.addEventListener('click', () => {
    document.getElementById(t.dataset.target).scrollIntoView({behavior:'smooth', block:'start'});
  }));
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => { if (entry.isIntersecting) setActive(entry.target.id); });
  }, { rootMargin: '-20% 0px -70% 0px' });
  sections.forEach(s => observer.observe(s));
</script>
</body>
</html>
