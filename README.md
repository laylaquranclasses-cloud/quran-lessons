# quran-lessons
<!DOCTYPE html>

<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>ليلى عبدالله — دروس القرآن الكريم أونلاين</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,600;0,700;1,400;1,600&family=Tajawal:wght@300;400;500;700&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet"/>
<style>
:root{
  --ink:#1a1208;--gold:#b8860b;--gold-light:#d4a843;--gold-pale:#f5e9c8;--gold-shimmer:#efe0aa;
  --teal:#0d4a4a;--teal-mid:#155f5f;--teal-light:#1e7a7a;--teal-pale:#e8f4f4;
  --cream:#faf7f0;--parchment:#f2ead8;--white:#ffffff;--muted:#6b5c3e;--border:#e0d5be;--error:#c0392b;
}
*{box-sizing:border-box;margin:0;padding:0;}
html{scroll-behavior:smooth;}
body{font-family:'Tajawal',sans-serif;background:var(--cream);color:var(--ink);overflow-x:hidden;}
html[lang="en"] body{font-family:'DM Sans',sans-serif;}

/* ── LANG BAR ── */
.lang-bar{
background:var(–teal);
border-bottom:1px solid rgba(255,255,255,0.08);
display:flex;align-items:center;
padding:8px 20px;gap:6px;
position:sticky;top:0;z-index:100;
justify-content:flex-start;
}
html[lang=“en”] .lang-bar{justify-content:flex-end;}
.lang-btn{
display:flex;align-items:center;gap:6px;
padding:6px 16px;border-radius:100px;font-size:13px;font-weight:600;
border:1.5px solid rgba(212,168,67,.35);
cursor:pointer;transition:all .18s;
background:transparent;color:rgba(255,255,255,.65);
font-family:‘Tajawal’,sans-serif;
}
html[lang=“en”] .lang-btn{font-family:‘DM Sans’,sans-serif;}
.lang-btn:hover{background:rgba(212,168,67,.12);color:var(–gold-shimmer);}
.lang-btn.active{background:var(–gold);color:var(–ink);border-color:var(–gold);}
.lang-flag{font-size:15px;}

/* ── HERO ── */
.hero{background:var(–teal);background-image:radial-gradient(ellipse 80% 60% at 50% -10%,rgba(184,134,11,0.18) 0%,transparent 70%),radial-gradient(ellipse 40% 40% at 90% 90%,rgba(184,134,11,0.08) 0%,transparent 60%);padding:0 20px;position:relative;overflow:hidden;}
.hero-inner{max-width:900px;margin:0 auto;display:grid;grid-template-columns:1fr 1fr;gap:40px;align-items:center;padding:64px 0 80px;}
@media(max-width:680px){.hero-inner{grid-template-columns:1fr;text-align:center;padding:48px 0 64px;}.hero-avatar-wrap{order:-1;display:flex;justify-content:center;}}
.basmala{font-family:‘Tajawal’,sans-serif;font-size:clamp(16px,2.5vw,24px);color:var(–gold-light);letter-spacing:3px;margin-bottom:18px;opacity:.9;animation:fadeIn 1s ease both;}
.hero h1{font-family:‘Tajawal’,sans-serif;font-size:clamp(28px,5vw,52px);color:var(–white);line-height:1.2;font-weight:700;animation:slideUp .9s ease .1s both;}
html[lang=“en”] .hero h1{font-family:‘Cormorant Garamond’,serif;font-size:clamp(30px,5.5vw,54px);line-height:1.15;}
.hero h1 em{color:var(–gold-light);font-style:normal;}
html[lang=“en”] .hero h1 em{font-style:italic;}
.hero-tagline{margin-top:16px;font-size:clamp(13px,1.8vw,15px);color:rgba(255,255,255,.75);line-height:1.9;font-weight:400;max-width:420px;animation:slideUp .9s ease .2s both;}
@media(max-width:680px){.hero-tagline{margin-inline:auto;}}
.hero-badges{display:flex;flex-wrap:wrap;gap:8px;margin-top:24px;animation:slideUp .9s ease .3s both;}
@media(max-width:680px){.hero-badges{justify-content:center;}}
.badge{background:rgba(212,168,67,.15);border:1px solid rgba(212,168,67,.35);color:var(–gold-shimmer);border-radius:100px;padding:5px 14px;font-size:12px;font-weight:500;}
.avatar-ring{width:clamp(180px,26vw,260px);height:clamp(180px,26vw,260px);border-radius:50%;border:3px solid rgba(212,168,67,.4);display:flex;align-items:center;justify-content:center;position:relative;animation:fadeIn 1.2s ease .4s both;}
.avatar-ring::before{content:’’;position:absolute;inset:-8px;border-radius:50%;border:1px dashed rgba(212,168,67,.22);}
.avatar-inner{width:88%;height:88%;border-radius:50%;background:linear-gradient(135deg,var(–teal-mid),#0a3535);display:flex;align-items:center;justify-content:center;font-size:clamp(60px,9vw,90px);}
.avatar-badge{position:absolute;bottom:10px;left:0;background:var(–gold);color:var(–ink);border-radius:100px;padding:5px 13px;font-size:11px;font-weight:700;box-shadow:0 4px 14px rgba(0,0,0,.25);white-space:nowrap;}
html[lang=“en”] .avatar-badge{left:auto;right:0;}
.hero-wave{position:absolute;bottom:-1px;left:0;right:0;height:50px;background:var(–cream);clip-path:ellipse(55% 100% at 50% 100%);}

/* ── SECTIONS ── */
.section{max-width:900px;margin:0 auto;padding:56px 20px;}
.section-title{font-family:‘Tajawal’,sans-serif;font-size:clamp(24px,4vw,36px);font-weight:700;color:var(–teal);text-align:center;margin-bottom:6px;}
html[lang=“en”] .section-title{font-family:‘Cormorant Garamond’,serif;}
.section-title em{font-style:normal;color:var(–gold);}
html[lang=“en”] .section-title em{font-style:italic;}
.section-sub{text-align:center;color:var(–muted);font-size:14.5px;margin-bottom:36px;line-height:1.8;}

/* ── ABOUT ── */
.about-grid{display:grid;grid-template-columns:1fr 1fr;gap:20px;}
@media(max-width:600px){.about-grid{grid-template-columns:1fr;}}
.about-card{background:var(–white);border-radius:16px;padding:26px;border:1px solid var(–border);box-shadow:0 2px 14px rgba(0,0,0,.05);transition:transform .2s,box-shadow .2s;}
.about-card:hover{transform:translateY(-3px);box-shadow:0 8px 28px rgba(0,0,0,.09);}
.about-card.full{grid-column:1/-1;}
.about-icon{font-size:26px;margin-bottom:10px;}
.about-card h3{font-family:‘Tajawal’,sans-serif;font-size:20px;font-weight:700;color:var(–teal);margin-bottom:8px;}
html[lang=“en”] .about-card h3{font-family:‘Cormorant Garamond’,serif;}
.about-card p{font-size:14px;color:var(–muted);line-height:1.9;}
.quote-card{background:linear-gradient(135deg,var(–teal) 0%,var(–teal-mid) 100%);border-radius:16px;padding:32px 36px;position:relative;overflow:hidden;}
.quote-card::before{content:’”’;position:absolute;top:-20px;right:16px;font-family:‘Tajawal’,sans-serif;font-size:150px;color:rgba(255,255,255,.06);line-height:1;}
html[lang=“en”] .quote-card::before{right:auto;left:16px;font-family:‘Cormorant Garamond’,serif;content:’”’;}
.quote-card p{font-family:‘Tajawal’,sans-serif;font-size:clamp(16px,2.5vw,21px);color:var(–gold-shimmer);line-height:1.8;position:relative;}
html[lang=“en”] .quote-card p{font-family:‘Cormorant Garamond’,serif;font-style:italic;font-size:clamp(17px,2.5vw,22px);}
.quote-card cite{display:block;margin-top:12px;font-size:13px;font-style:normal;color:rgba(255,255,255,.5);}

/* ── PRICING ── */
.pricing-bg{background:var(–parchment);}
.pricing-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:18px;}
@media(max-width:600px){.pricing-grid{grid-template-columns:1fr;}}
.price-card{background:var(–white);border-radius:18px;padding:30px 22px;text-align:center;border:2px solid var(–border);position:relative;transition:all .22s;}
.price-card:hover{border-color:var(–teal-light);box-shadow:0 8px 28px rgba(13,74,74,.1);}
.price-card.popular{border-color:var(–gold);background:linear-gradient(180deg,#fffdf5 0%,var(–white) 100%);box-shadow:0 8px 30px rgba(184,134,11,.15);transform:scale(1.03);}
.pop-label{position:absolute;top:-12px;left:50%;transform:translateX(-50%);background:var(–gold);color:var(–ink);border-radius:100px;padding:4px 16px;font-size:11px;font-weight:700;text-transform:uppercase;letter-spacing:1px;white-space:nowrap;}
.price-duration{font-family:‘Cormorant Garamond’,serif;font-size:40px;font-weight:700;color:var(–teal);line-height:1;}
.price-duration span{font-size:17px;font-weight:400;font-family:‘Tajawal’,sans-serif;}
.price-label{font-size:12.5px;color:var(–muted);margin-top:3px;margin-bottom:18px;}
.price-amount{font-size:30px;font-weight:700;color:var(–gold);margin-bottom:3px;}
.price-per{font-size:12px;color:var(–muted);}
.price-features{margin-top:18px;list-style:none;text-align:right;}
html[lang=“en”] .price-features{text-align:left;}
.price-features li{font-size:13px;color:var(–muted);padding:4px 0;display:flex;align-items:flex-start;gap:7px;line-height:1.6;flex-direction:row-reverse;}
html[lang=“en”] .price-features li{flex-direction:row;}
.price-features li::before{content:‘✓’;color:var(–teal-light);font-weight:700;flex-shrink:0;}

/* ── FORM ── */
.form-card{background:var(–white);border-radius:20px;box-shadow:0 4px 40px rgba(0,0,0,.08);padding:40px 38px;border:1px solid var(–border);}
@media(max-width:520px){.form-card{padding:26px 18px;}}
.form-section-label{font-family:‘Tajawal’,sans-serif;font-size:20px;font-weight:700;color:var(–teal);border-right:3px solid var(–gold);padding-right:12px;margin-bottom:18px;}
html[lang=“en”] .form-section-label{font-family:‘Cormorant Garamond’,serif;border-right:none;border-left:3px solid var(–gold);padding-right:0;padding-left:12px;}
.form-row{display:grid;grid-template-columns:1fr 1fr;gap:14px;}
@media(max-width:480px){.form-row{grid-template-columns:1fr;}}
.field{display:flex;flex-direction:column;gap:5px;margin-bottom:14px;}
label{font-size:11.5px;font-weight:700;color:var(–muted);letter-spacing:0;text-transform:uppercase;}
label .req{color:var(–error);}
input,select,textarea{padding:11px 13px;border:1.5px solid var(–border);border-radius:10px;font-size:14.5px;font-family:‘Tajawal’,sans-serif;color:var(–ink);background:#fdfcf9;transition:border-color .2s,box-shadow .2s;outline:none;width:100%;text-align:right;}
html[lang=“en”] input,html[lang=“en”] select,html[lang=“en”] textarea{font-family:‘DM Sans’,sans-serif;text-align:left;}
input:focus,select:focus,textarea:focus{border-color:var(–teal-light);box-shadow:0 0 0 3px rgba(30,122,122,.1);background:var(–white);}
select{appearance:none;background-image:url(“data:image/svg+xml,%3Csvg xmlns=‘http://www.w3.org/2000/svg’ width=‘12’ height=‘8’%3E%3Cpath d=‘M1 1l5 5 5-5’ stroke=’%236b5c3e’ stroke-width=‘1.5’ fill=‘none’ stroke-linecap=‘round’/%3E%3C/svg%3E”);background-repeat:no-repeat;background-position:left 13px center;padding-left:36px;cursor:pointer;}
html[lang=“en”] select{background-position:right 13px center;padding-left:13px;padding-right:36px;}
textarea{resize:vertical;min-height:78px;}
.divider{border:none;border-top:1px dashed var(–border);margin:26px 0;}

/* ── DURATION ── */
.duration-cards{display:grid;grid-template-columns:repeat(3,1fr);gap:12px;margin-bottom:4px;}
@media(max-width:460px){.duration-cards{grid-template-columns:1fr;}}
.dur-card{border:2px solid var(–border);border-radius:12px;padding:16px 12px;text-align:center;cursor:pointer;transition:all .18s;background:#fdfcf9;}
.dur-card:hover{border-color:var(–teal-light);background:var(–teal-pale);}
.dur-card.selected{border-color:var(–gold);background:var(–gold-pale);box-shadow:0 3px 14px rgba(184,134,11,.18);}
.dur-mins{font-family:‘Cormorant Garamond’,serif;font-size:30px;font-weight:700;color:var(–teal);line-height:1;}
.dur-mins span{font-size:14px;font-weight:400;font-family:‘Tajawal’,sans-serif;}
.dur-price{font-size:17px;font-weight:700;color:var(–gold);margin-top:4px;}
.dur-note{font-size:11px;color:var(–muted);margin-top:2px;}

/* ── CALENDAR ── */
.cal-nav{display:flex;align-items:center;justify-content:space-between;margin-bottom:12px;}
.cal-nav button{background:var(–cream);border:1.5px solid var(–border);border-radius:8px;width:34px;height:34px;cursor:pointer;font-size:17px;display:flex;align-items:center;justify-content:center;transition:all .15s;color:var(–ink);}
.cal-nav button:hover{background:var(–teal);color:var(–white);border-color:var(–teal);}
.cal-month-label{font-family:‘Tajawal’,sans-serif;font-size:19px;font-weight:700;color:var(–teal);}
html[lang=“en”] .cal-month-label{font-family:‘Cormorant Garamond’,serif;}
.cal-grid{display:grid;grid-template-columns:repeat(7,1fr);gap:4px;margin-bottom:6px;}
.cal-header{text-align:center;font-size:10.5px;font-weight:700;color:var(–muted);padding-bottom:5px;text-transform:uppercase;letter-spacing:.5px;}
.cal-day{aspect-ratio:1;display:flex;align-items:center;justify-content:center;border-radius:8px;font-size:13px;font-weight:500;border:1.5px solid transparent;transition:all .15s;}
.cal-day.empty{background:transparent;}
.cal-day.disabled{color:#ccc;background:#f5f5f5;cursor:not-allowed;}
.cal-day.available{background:rgba(13,74,74,.07);color:var(–teal);cursor:pointer;border-color:rgba(30,122,122,.2);}
.cal-day.available:hover{background:var(–teal-mid);color:var(–white);border-color:var(–teal-mid);transform:scale(1.1);}
.cal-day.selected{background:var(–teal);color:var(–white);border-color:var(–teal);font-weight:700;box-shadow:0 3px 10px rgba(13,74,74,.3);}
.cal-day.today-ring{border-color:var(–gold)!important;}
.legend{display:flex;gap:14px;flex-wrap:wrap;font-size:12px;color:var(–muted);margin-top:8px;}
.legend-item{display:flex;align-items:center;gap:6px;}
.leg-dot{width:12px;height:12px;border-radius:4px;}
.leg-avail{background:rgba(13,74,74,.1);border:1.5px solid rgba(30,122,122,.3);}
.leg-sel{background:var(–teal);}
.leg-off{background:#f0f0f0;border:1.5px solid #ddd;}

/* ── TIME SLOTS ── */
.time-slots{display:none;margin-top:16px;}
.time-slots.visible{display:block;}
.time-slots h4{font-size:11.5px;font-weight:700;color:var(–muted);text-transform:uppercase;letter-spacing:0;margin-bottom:10px;}
.slot-grid{display:flex;flex-wrap:wrap;gap:8px;}
.slot{padding:8px 15px;border-radius:8px;border:1.5px solid var(–border);font-size:13px;font-weight:600;cursor:pointer;transition:all .15s;color:var(–muted);background:#fdfcf9;text-align:center;}
.slot:hover{border-color:var(–teal-light);color:var(–teal);background:var(–teal-pale);}
.slot.selected{background:var(–gold);border-color:var(–gold);color:var(–white);box-shadow:0 3px 10px rgba(184,134,11,.3);}
.slot-duration-note{font-size:10px;color:inherit;display:block;opacity:.8;}

/* ── SUMMARY ── */
.summary-box{display:none;background:linear-gradient(135deg,rgba(13,74,74,.05),rgba(184,134,11,.07));border:1.5px solid rgba(184,134,11,.3);border-radius:10px;padding:13px 17px;margin-top:14px;font-size:14px;color:var(–teal);font-weight:500;line-height:1.7;}
.summary-box.visible{display:block;}

/* ── NOTICE ── */
.no-duration-notice{display:none;background:rgba(184,134,11,0.1);border:1.5px solid rgba(184,134,11,0.4);border-radius:10px;padding:12px 16px;font-size:13.5px;color:var(–gold);margin-top:12px;text-align:center;}
.no-duration-notice.visible{display:block;}

/* ── T&C ── */
.tc-box{background:#fdfcf9;border:1.5px solid var(–border);border-radius:12px;padding:20px 22px;max-height:250px;overflow-y:auto;margin-bottom:16px;font-size:13px;line-height:1.9;color:var(–muted);}
.tc-box h4{font-family:‘Tajawal’,sans-serif;font-size:16px;font-weight:700;color:var(–teal);margin-top:16px;margin-bottom:5px;}
html[lang=“en”] .tc-box h4{font-family:‘Cormorant Garamond’,serif;}
.tc-box h4:first-child{margin-top:0;}
.tc-box ul{padding-right:18px;}
html[lang=“en”] .tc-box ul{padding-right:0;padding-left:18px;}
.tc-box ul li{margin-bottom:4px;}
.tc-accept{display:flex;align-items:flex-start;gap:10px;font-size:13.5px;color:var(–ink);}
.tc-accept input[type=checkbox]{width:17px;height:17px;margin-top:2px;accent-color:var(–teal);cursor:pointer;flex-shrink:0;}

/* ── SUBMIT ── */
.submit-btn{width:100%;padding:16px;background:linear-gradient(135deg,var(–teal) 0%,var(–teal-mid) 100%);color:var(–white);border:none;border-radius:12px;font-size:16px;font-weight:700;cursor:pointer;margin-top:10px;transition:all .2s;font-family:‘Tajawal’,sans-serif;}
html[lang=“en”] .submit-btn{font-family:‘DM Sans’,sans-serif;}
.submit-btn:hover{transform:translateY(-2px);box-shadow:0 8px 24px rgba(13,74,74,.35);}
.submit-btn:disabled{opacity:.6;cursor:not-allowed;transform:none;}
.submit-note{text-align:center;font-size:12.5px;color:var(–muted);margin-top:12px;line-height:1.8;}

/* ── SUCCESS ── */
.success-screen{display:none;text-align:center;padding:40px 20px;}
.success-icon{width:80px;height:80px;background:linear-gradient(135deg,var(–teal),var(–teal-mid));border-radius:50%;display:flex;align-items:center;justify-content:center;margin:0 auto 24px;font-size:36px;}
.success-screen h2{font-family:‘Tajawal’,sans-serif;font-size:30px;color:var(–teal);margin-bottom:12px;}
html[lang=“en”] .success-screen h2{font-family:‘Cormorant Garamond’,serif;}
.success-screen p{color:var(–muted);line-height:1.8;max-width:400px;margin-inline:auto;font-size:15px;}

/* ── FOOTER ── */
footer{background:var(–teal);color:rgba(255,255,255,.6);text-align:center;padding:32px 20px;font-size:13px;line-height:1.9;}
footer strong{color:var(–gold-shimmer);}
.footer-arabic{font-family:‘Tajawal’,sans-serif;font-size:20px;color:var(–gold-light);margin-bottom:6px;}

@keyframes fadeIn{from{opacity:0}to{opacity:1}}
@keyframes slideUp{from{opacity:0;transform:translateY(18px)}to{opacity:1;transform:translateY(0)}}
</style>

</head>
<body>

<!-- ── LANG BAR ── -->

<div class="lang-bar">
  <button class="lang-btn active" id="btnAR" onclick="setLang('ar')"><span class="lang-flag">🇧🇭</span> العربية</button>
  <button class="lang-btn" id="btnEN" onclick="setLang('en')"><span class="lang-flag">🇬🇧</span> English</button>
</div>

<!-- ── HERO ── -->

<div class="hero">
  <div class="hero-inner">
    <div class="hero-text">
      <div class="basmala">بِسْمِ اللَّهِ الرَّحْمَنِ الرَّحِيمِ</div>
      <h1 id="heroTitle">دروس القرآن الكريم مع <em>ليلى عبدالله</em></h1>
      <p class="hero-tagline" id="heroTagline">دروس قرآنية خاصة وفردية عبر الإنترنت — مخصصة، ممتعة، ومركّزة عليك تماماً. من المستوى المبتدئ إلى التجويد المتقدم.</p>
      <div class="hero-badges" id="heroBadges">
        <span class="badge">✓ شهادة التلاوة وعلم التجويد برواية حفص عن عاصم — وزارة العدل والشؤون الإسلامية</span>
        <span class="badge">✓ تقدير ممتاز</span>
        <span class="badge">✓ أكثر من 6 سنوات خبرة</span>
        <span class="badge">✓ جميع الأعمار والمستويات</span>
        <span class="badge">✓ عبر Google Meet</span>
      </div>
    </div>
    <div class="hero-avatar-wrap">
      <div class="avatar-ring">
        <div class="avatar-inner">🌙</div>
        <div class="avatar-badge" id="avatarBadge">معلّمة معتمدة 🎓</div>
      </div>
    </div>
  </div>
  <div class="hero-wave"></div>
</div>

<!-- ── ABOUT ── -->

<div class="section">
  <div class="section-title" id="aboutTitle">تعرّف على <em>معلّمتك</em></div>
  <p class="section-sub" id="aboutSub">مؤهّلة، ذات خبرة، وشغوفة بجعل تعلّم القرآن تجربة حقيقية ومؤثرة</p>
  <div class="about-grid">
    <div class="about-card">
      <div class="about-icon">📜</div>
      <h3 id="cert-title">شهادة رسمية معتمدة</h3>
      <p id="cert-body">أحمل <strong>شهادة التلاوة وعلم التجويد برواية حفص عن عاصم</strong> الصادرة عن <strong>وزارة العدل والشؤون الإسلامية في البحرين</strong>، بتقدير <strong>ممتاز</strong> — وهي اعتراف رسمي بخبرتي في التلاوة وأحكام التجويد.</p>
    </div>
    <div class="about-card">
      <div class="about-icon">⏳</div>
      <h3 id="exp-title">6 سنوات من الخبرة</h3>
      <p id="exp-body">أُدرِّس القرآن الكريم منذ أكثر من <strong>6 سنوات</strong>، بما في ذلك الدروس الإلكترونية مع طلاب من مختلف الأعمار والمستويات. أعرف كيف أتأقلم مع إيقاع كل طالب وأسلوبه.</p>
    </div>
    <div class="about-card">
      <div class="about-icon">🗣️</div>
      <h3 id="tajweed-title">التجويد والنطق الصحيح</h3>
      <p id="tajweed-body">تركيزي الأساسي هو مساعدتك على <strong>نطق كل حرف من مخرجه الصحيح</strong> وتطبيق أحكام التجويد بدقة — لتكون تلاوتك جميلة وصحيحة ومؤثرة.</p>
    </div>
    <div class="about-card">
      <div class="about-icon">✨</div>
      <h3 id="fun-title">ممتعة ومعمّقة ومركّزة</h3>
      <p id="fun-body">أحرص على أن تكون الدروس <strong>شيّقة وممتعة</strong> مع تشجيعك على التأمّل في معاني ما تتلوه. تعلّم القرآن يجب أن يفتح عقلك وقلبك — لا لسانك فحسب.</p>
    </div>
    <div class="about-card full quote-card">
      <p id="quoteText">سواء كنت تبدأ من الصفر أو تصقل تلاوتك، أنا هنا لأرشدك بصبر واهتمام. دروسي صغيرة وشخصية ومبنية كلياً حولك — لأن كل طالب يستحق أن يشعر بفرحة الارتباط بكتاب الله.</p>
      <cite id="quoteCite">— ليلى عبدالله، معلّمة القرآن · البحرين</cite>
    </div>
  </div>
</div>

<!-- ── PRICING ── -->

<div class="pricing-bg">
<div class="section">
  <div class="section-title" id="pricingTitle">خيارات <em>الدروس</em></div>
  <p class="section-sub" id="pricingSub">جميع الدروس خاصة وفردية. اختر المدة التي تناسب جدولك واحتياجك.</p>
  <div class="pricing-grid">
    <div class="price-card">
      <div class="price-duration">30<span id="minLabel1"> دقيقة</span></div>
      <div class="price-label" id="p1label">جلسة مبتدئة</div>
      <div class="price-amount">8 BHD</div>
      <div class="price-per" id="perSession1">لكل جلسة</div>
      <ul class="price-features" id="p1features">
        <li>مثالية للمبتدئين والأطفال</li>
        <li>موضوع واحد واضح لكل درس</li>
        <li>قصيرة ومركّزة</li>
        <li>تناسب أي جدول مشغول</li>
      </ul>
    </div>
    <div class="price-card popular">
      <div class="pop-label" id="popLabel">⭐ الأكثر طلباً</div>
      <div class="price-duration">45<span id="minLabel2"> دقيقة</span></div>
      <div class="price-label" id="p2label">الجلسة المعيارية</div>
      <div class="price-amount">10 BHD</div>
      <div class="price-per" id="perSession2">لكل جلسة</div>
      <ul class="price-features" id="p2features">
        <li>أفضل قيمة مقابل السعر</li>
        <li>مراجعة ومادة جديدة</li>
        <li>مناسبة لجميع المستويات</li>
        <li>وتيرة تعلّم متوازنة</li>
      </ul>
    </div>
    <div class="price-card">
      <div class="price-duration">60<span id="minLabel3"> دقيقة</span></div>
      <div class="price-label" id="p3label">الجلسة الكاملة</div>
      <div class="price-amount">13 BHD</div>
      <div class="price-per" id="perSession3">لكل جلسة</div>
      <ul class="price-features" id="p3features">
        <li>تغطية معمّقة وشاملة</li>
        <li>مثالية للمتقدمين والحفظ</li>
        <li>وقت مراجعة واسع</li>
        <li>أقصى تقدم أسبوعي</li>
      </ul>
    </div>
  </div>
  <p id="paymentNote" style="text-align:center;font-size:13px;color:var(--muted);margin-top:22px;">💳 الدفع عبر <strong>BenefitPay</strong> — قبل كل درس وبعد التأكيد. لا يُطلب دفع أثناء التسجيل.</p>
</div>
</div>

<!-- ── BOOKING FORM ── -->

<div class="section">
  <div class="section-title" id="bookTitle">احجز <em>جلستك</em></div>
  <p class="section-sub" id="bookSub">أدخل تفاصيلك واختر التاريخ والوقت — سأؤكد خلال 24 ساعة. لا حاجة للدفع الآن.</p>
  <div class="form-card">

```
<div class="success-screen" id="successScreen">
  <div class="success-icon">🌙</div>
  <h2 id="successTitle">تم استلام طلبك!</h2>
  <p id="successMsg">جزاك الله خيراً! تم إرسال طلب الحجز. سأتواصل معك خلال 24 ساعة عبر البريد الإلكتروني أو واتساب لتأكيد موعدك. لا حاجة للدفع حتى يتم التأكيد. 🤲</p>
</div>

<form id="bookingForm" action="https://formspree.io/f/mvzbejoo" method="POST">
  <input type="hidden" name="selected_date" id="hiddenDate"/>
  <input type="hidden" name="selected_time" id="hiddenTime"/>
  <input type="hidden" name="selected_duration" id="hiddenDuration"/>
  <input type="hidden" name="_subject" value="📚 طلب حجز درس قرآن جديد — ليلى عبدالله"/>

  <!-- Personal Info -->
  <div class="form-section-label" id="step1Label">👤 معلوماتك الشخصية</div>
  <div class="form-row">
    <div class="field">
      <label id="nameLabel">الاسم الكامل *</label>
      <input type="text" name="name" id="studentName" placeholder="مثال: فاطمة حسن" required/>
    </div>
    <div class="field">
      <label id="ageLabel">العمر *</label>
      <input type="number" name="age" id="ageInput" placeholder="مثال: 24" min="4" max="99" required/>
    </div>
  </div>
  <div class="form-row">
    <div class="field">
      <label id="emailLabel">البريد الإلكتروني *</label>
      <input type="email" name="email" id="emailInput" placeholder="بريدك@الإلكتروني.com" required/>
    </div>
    <div class="field">
      <label id="waLabel">رقم واتساب *</label>
      <input type="tel" name="whatsapp" id="waInput" placeholder="+973 3xxx xxxx" required/>
    </div>
  </div>
  <div class="field">
    <label id="levelLabel">مستواك الحالي في القرآن *</label>
    <select name="quran_level" id="levelSelect" required>
      <option value="" disabled selected id="levelPlaceholder">— اختر مستواك —</option>
      <option value="مبتدئ — لا يعرف التجويد" id="lvl1">🌱 مبتدئ — لا يعرف التجويد</option>
      <option value="أساسي — يعرف التجويد الأساسي" id="lvl2">📖 أساسي — يعرف التجويد الأساسي</option>
      <option value="متوسط — لديه بعض المعرفة" id="lvl3">📚 متوسط — لديه بعض المعرفة</option>
      <option value="متقدم — يريد التحضير لامتحانات القرآن" id="lvl4">🏆 متقدم — يريد التحضير لامتحانات القرآن</option>
      <option value="حفظ القرآن — يريد المساعدة في الحفظ" id="lvl5">🤲 حفظ القرآن — أساعدك في الحفظ</option>
    </select>
  </div>
  <div class="field">
    <label id="goalLabel">هدفك من الدرس (اختياري)</label>
    <textarea name="goal" id="goalInput" placeholder="مثال: أريد أن أقرأ بطلاقة مع التجويد الصحيح، أو أريد حفظ سور معينة..."></textarea>
  </div>

  <hr class="divider"/>

  <!-- Duration -->
  <div class="form-section-label" id="step2Label">⏱️ اختر مدة الدرس</div>
  <div class="duration-cards">
    <div class="dur-card" data-minutes="30" data-duration-ar="30 دقيقة" data-duration-en="30 minutes" data-price="8 BHD" onclick="selectDuration(this)">
      <div class="dur-mins">30<span id="durSpan1"> د</span></div>
      <div class="dur-price">8 BHD</div>
      <div class="dur-note" id="durNote1">مبتدئة</div>
    </div>
    <div class="dur-card" data-minutes="45" data-duration-ar="45 دقيقة" data-duration-en="45 minutes" data-price="10 BHD" onclick="selectDuration(this)">
      <div class="dur-mins">45<span id="durSpan2"> د</span></div>
      <div class="dur-price">10 BHD</div>
      <div class="dur-note" id="durNote2">⭐ الأكثر طلباً</div>
    </div>
    <div class="dur-card" data-minutes="60" data-duration-ar="60 دقيقة" data-duration-en="60 minutes" data-price="13 BHD" onclick="selectDuration(this)">
      <div class="dur-mins">60<span id="durSpan3"> د</span></div>
      <div class="dur-price">13 BHD</div>
      <div class="dur-note" id="durNote3">كاملة</div>
    </div>
  </div>
  <div class="no-duration-notice" id="noDurationNotice">⚠️ يرجى اختيار مدة الدرس أولاً قبل تحديد التاريخ.</div>

  <hr class="divider"/>

  <!-- Calendar -->
  <div class="form-section-label" id="step3Label">📅 اختر تاريخاً</div>
  <p id="calIntroText" style="font-size:13.5px;color:var(--muted);margin-bottom:16px;line-height:1.8;">
    المواعيد المتاحة: <strong>صباح الجمعة والسبت</strong> (9:00 ص – 12:00 م) و<strong>مساء الثلاثاء والأربعاء</strong> (7:00 م – 9:00 م). التواريخ الخضراء متاحة للحجز.
  </p>
  <div class="cal-nav">
    <button type="button" id="prevMonth">&#8249;</button>
    <span class="cal-month-label" id="monthLabel"></span>
    <button type="button" id="nextMonth">&#8250;</button>
  </div>
  <div class="cal-grid" id="calHeaders"></div>
  <div class="cal-grid" id="calGrid"></div>
  <div class="legend">
    <div class="legend-item"><div class="leg-dot leg-avail"></div><span id="legendAvail">متاح</span></div>
    <div class="legend-item"><div class="leg-dot leg-sel"></div><span id="legendSel">محدد</span></div>
    <div class="legend-item"><div class="leg-dot leg-off"></div><span id="legendOff">غير متاح</span></div>
  </div>
  <div class="time-slots" id="timeSlots">
    <h4><span id="timeSlotsLabel">الأوقات المتاحة</span> — <span id="selectedDateLabel"></span></h4>
    <div class="slot-grid" id="slotGrid"></div>
  </div>
  <div class="summary-box" id="summaryBox"></div>

  <hr class="divider"/>

  <!-- T&C -->
  <div class="form-section-label" id="tcTitle">📋 الشروط والأحكام</div>
  <div class="tc-box" id="tcBox"></div>
  <div class="tc-accept">
    <input type="checkbox" id="tcCheck" name="agreed_to_terms" value="Yes" required/>
    <label for="tcCheck" id="tcAcceptLabel" style="text-transform:none;letter-spacing:0;font-size:13.5px;font-weight:400;color:var(--ink);cursor:pointer;line-height:1.7;">
      لقد قرأت وأوافق على الشروط والأحكام. أفهم أنه <strong>لا يُطلب أي دفع الآن</strong>، وأن الدفع سيتم عبر <strong>BenefitPay قبل كل جلسة مؤكدة</strong>.
    </label>
  </div>

  <hr class="divider"/>

  <button type="submit" class="submit-btn" id="submitBtn">✉️ إرسال طلب الحجز</button>
  <p class="submit-note" id="submitNote">سأراجع طلبك وأتواصل معك خلال 24 ساعة للتأكيد. 🤲 لا حاجة للدفع حتى يتم تأكيد موعدك.</p>
</form>
```

  </div>
</div>

<!-- ── FOOTER ── -->

<footer>
  <div class="footer-arabic">وَرَتِّلِ الْقُرْآنَ تَرْتِيلًا</div>
  <div id="footerVerse" style="font-size:11px;margin-bottom:14px;opacity:.45;">"وَرَتِّلِ الْقُرْآنَ تَرْتِيلًا" — سورة المزمل 73:4</div>
  <strong>ليلى عبدالله</strong> — <span id="footerDesc">معلّمة قرآن معتمدة · البحرين</span><br/>
  <span id="footerPlatform">الجلسات عبر Google Meet · الدفع عبر BenefitPay</span><br/>
  <span id="footerCopy" style="font-size:11px;margin-top:8px;display:block;opacity:.4;">© 2025 دروس ليلى عبدالله القرآنية. جميع الحقوق محفوظة.</span>
</footer>

<script>
// ── CONFIG ──────────────────────────────────────────────────
const DAY_WINDOWS = {
  5: { start: 9*60,  end: 12*60 },  // Friday morning
  6: { start: 9*60,  end: 12*60 },  // Saturday morning
  2: { start: 19*60, end: 21*60 },  // Tuesday evening
  3: { start: 19*60, end: 21*60 },  // Wednesday evening
};

function generateSlots(dow, durationMinutes) {
  const win = DAY_WINDOWS[dow];
  if (!win) return [];
  const slots = [];
  for (let t = win.start; t + durationMinutes <= win.end; t += durationMinutes) {
    const h = Math.floor(t/60), m = t%60;
    const ampm = h >= 12 ? 'PM' : 'AM';
    const h12 = h > 12 ? h-12 : (h===0?12:h);
    slots.push(`${h12}:${m===0?'00':m} ${ampm}`);
  }
  return slots;
}

// ── TRANSLATIONS ────────────────────────────────────────────
const T = {
  ar: {
    htmlLang:'ar', htmlDir:'rtl',
    pageTitle:'ليلى عبدالله — دروس القرآن الكريم أونلاين',
    heroTitle:'دروس القرآن الكريم مع <em>ليلى عبدالله</em>',
    heroTagline:'دروس قرآنية خاصة وفردية عبر الإنترنت — مخصصة، ممتعة، ومركّزة عليك تماماً. من المستوى المبتدئ إلى التجويد المتقدم.',
    badges:['✓ شهادة التلاوة وعلم التجويد برواية حفص عن عاصم — وزارة العدل والشؤون الإسلامية','✓ تقدير ممتاز','✓ أكثر من 6 سنوات خبرة','✓ جميع الأعمار والمستويات','✓ عبر Google Meet'],
    avatarBadge:'معلّمة معتمدة 🎓',
    aboutTitle:'تعرّف على <em>معلّمتك</em>',
    aboutSub:'مؤهّلة، ذات خبرة، وشغوفة بجعل تعلّم القرآن تجربة حقيقية ومؤثرة',
    certTitle:'شهادة رسمية معتمدة',
    certBody:'أحمل <strong>شهادة التلاوة وعلم التجويد برواية حفص عن عاصم</strong> الصادرة عن <strong>وزارة العدل والشؤون الإسلامية في البحرين</strong>، بتقدير <strong>ممتاز</strong> — وهي اعتراف رسمي بخبرتي في التلاوة وأحكام التجويد.',
    expTitle:'6 سنوات من الخبرة',
    expBody:'أُدرِّس القرآن الكريم منذ أكثر من <strong>6 سنوات</strong>، بما في ذلك الدروس الإلكترونية مع طلاب من مختلف الأعمار والمستويات. أعرف كيف أتأقلم مع إيقاع كل طالب وأسلوبه.',
    tajweedTitle:'التجويد والنطق الصحيح',
    tajweedBody:'تركيزي الأساسي هو مساعدتك على <strong>نطق كل حرف من مخرجه الصحيح</strong> وتطبيق أحكام التجويد بدقة — لتكون تلاوتك جميلة وصحيحة ومؤثرة.',
    funTitle:'ممتعة ومعمّقة ومركّزة',
    funBody:'أحرص على أن تكون الدروس <strong>شيّقة وممتعة</strong> مع تشجيعك على التأمّل في معاني ما تتلوه. تعلّم القرآن يجب أن يفتح عقلك وقلبك — لا لسانك فحسب.',
    quoteText:'سواء كنت تبدأ من الصفر أو تصقل تلاوتك، أنا هنا لأرشدك بصبر واهتمام. دروسي صغيرة وشخصية ومبنية كلياً حولك — لأن كل طالب يستحق أن يشعر بفرحة الارتباط بكتاب الله.',
    quoteCite:'— ليلى عبدالله، معلّمة القرآن · البحرين',
    pricingTitle:'خيارات <em>الدروس</em>',
    pricingSub:'جميع الدروس خاصة وفردية. اختر المدة التي تناسب جدولك واحتياجك.',
    minLabel:' دقيقة', durSpan:' د',
    p1label:'جلسة مبتدئة', p2label:'الجلسة المعيارية', p3label:'الجلسة الكاملة',
    perSession:'لكل جلسة', popLabel:'⭐ الأكثر طلباً',
    p1f:['مثالية للمبتدئين والأطفال','موضوع واحد واضح لكل درس','قصيرة ومركّزة','تناسب أي جدول مشغول'],
    p2f:['أفضل قيمة مقابل السعر','مراجعة ومادة جديدة','مناسبة لجميع المستويات','وتيرة تعلّم متوازنة'],
    p3f:['تغطية معمّقة وشاملة','مثالية للمتقدمين والحفظ','وقت مراجعة واسع','أقصى تقدم أسبوعي'],
    paymentNote:'💳 الدفع عبر <strong>BenefitPay</strong> — قبل كل درس وبعد التأكيد. لا يُطلب دفع أثناء التسجيل.',
    bookTitle:'احجز <em>جلستك</em>',
    bookSub:'أدخل تفاصيلك واختر التاريخ والوقت — سأؤكد خلال 24 ساعة. لا حاجة للدفع الآن.',
    step1Label:'👤 معلوماتك الشخصية',
    nameLabel:'الاسم الكامل *', agePlaceholder:'مثال: 24', namePlaceholder:'مثال: فاطمة حسن',
    ageLabel:'العمر *', emailLabel:'البريد الإلكتروني *', emailPlaceholder:'بريدك@الإلكتروني.com',
    waLabel:'رقم واتساب *', waPlaceholder:'+973 3xxx xxxx',
    levelLabel:'مستواك الحالي في القرآن *',
    levelPlaceholder:'— اختر مستواك —',
    levels:['🌱 مبتدئ — لا يعرف التجويد','📖 أساسي — يعرف التجويد الأساسي','📚 متوسط — لديه بعض المعرفة','🏆 متقدم — يريد التحضير لامتحانات القرآن','🤲 حفظ القرآن — أساعدك في الحفظ'],
    goalLabel:'هدفك من الدرس (اختياري)',
    goalPlaceholder:'مثال: أريد أن أقرأ بطلاقة مع التجويد الصحيح، أو أريد حفظ سور معينة...',
    step2Label:'⏱️ اختر مدة الدرس',
    durNote1:'مبتدئة', durNote2:'⭐ الأكثر طلباً', durNote3:'كاملة',
    noDurationNotice:'⚠️ يرجى اختيار مدة الدرس أولاً قبل تحديد التاريخ.',
    step3Label:'📅 اختر تاريخاً',
    calIntro:'المواعيد المتاحة: <strong>صباح الجمعة والسبت</strong> (9:00 ص – 12:00 م) و<strong>مساء الثلاثاء والأربعاء</strong> (7:00 م – 9:00 م). التواريخ الخضراء متاحة للحجز.',
    legendAvail:'متاح', legendSel:'محدد', legendOff:'غير متاح',
    timeSlotsLabel:'الأوقات المتاحة',
    until:'حتى',
    noSlots:'لا توجد أوقات متاحة لهذه المدة',
    tcTitle:'📋 الشروط والأحكام',
    tcAcceptLabel:'لقد قرأت وأوافق على الشروط والأحكام. أفهم أنه <strong>لا يُطلب أي دفع الآن</strong>، وأن الدفع سيتم عبر <strong>BenefitPay قبل كل جلسة مؤكدة</strong>.',
    submitBtn:'✉️ إرسال طلب الحجز',
    submitNote:'سأراجع طلبك وأتواصل معك خلال 24 ساعة للتأكيد. 🤲 لا حاجة للدفع حتى يتم تأكيد موعدك.',
    successTitle:'تم استلام طلبك! 🎉',
    successMsg:'جزاك الله خيراً! تم إرسال طلب الحجز بنجاح. سأتواصل معك خلال 24 ساعة عبر البريد الإلكتروني أو واتساب لتأكيد موعدك. لا حاجة للدفع حتى يتم التأكيد. 🤲',
    footerVerse:'"وَرَتِّلِ الْقُرْآنَ تَرْتِيلًا" — سورة المزمل 73:4',
    footerDesc:'معلّمة قرآن معتمدة · البحرين',
    footerPlatform:'الجلسات عبر Google Meet · الدفع عبر BenefitPay',
    footerCopy:'© 2025 دروس ليلى عبدالله القرآنية. جميع الحقوق محفوظة.',
    months:["يناير","فبراير","مارس","أبريل","مايو","يونيو","يوليو","أغسطس","سبتمبر","أكتوبر","نوفمبر","ديسمبر"],
    daysShort:["أحد","إثن","ثلا","أرب","خمس","جمع","سبت"],
    daysFull:["الأحد","الاثنين","الثلاثاء","الأربعاء","الخميس","الجمعة","السبت"],
    summaryDate:'التاريخ', summaryTime:'الوقت', summaryDuration:'المدة',
    alertDuration:'يرجى اختيار مدة الدرس أولاً.',
    alertSlot:'يرجى اختيار تاريخ ووقت من التقويم.',
    alertTC:'يرجى قراءة الشروط والأحكام والموافقة عليها.',
    sending:'جارٍ الإرسال…',
    errGeneral:'حدث خطأ. يرجى المحاولة مجدداً.',
    errNetwork:'خطأ في الشبكة. تحقق من اتصالك.',
    tcHTML:`
<h4>١. التسجيل والتأكيد</h4>
<ul>
  <li>إرسال هذا النموذج هو <strong>تسجيل أولي فقط</strong> — ولا يضمن حجزاً مؤكداً.</li>
  <li>ستتواصل معك ليلى خلال <strong>24 ساعة</strong> عبر البريد الإلكتروني أو واتساب لتأكيد الموعد.</li>
  <li>يُعتبر موعدك مؤكداً فقط بعد تلقّيك تأكيداً خطياً منها.</li>
  <li>⚠️ في حال عدم تلقّيك ردًا خلال <strong>48 ساعة</strong>، فهذا يعني أن الموعد المطلوب <strong>غير متاح</strong>. يُرجى إعادة التسجيل باختيار تاريخ أو وقت مختلف.</li>
</ul>
<h4>٢. الدفع</h4>
<ul>
  <li><strong>لا يُطلب أي دفع أثناء التسجيل.</strong></li>
  <li>يجب السداد <strong>قبل بدء كل درس</strong> لتأكيد الحجز نهائياً.</li>
  <li>يتم الدفع عبر <strong>BenefitPay</strong>. سيتم تزويدك بتفاصيل الدفع عند التأكيد.</li>
  <li>لن تبدأ الجلسة حتى يتم استلام الدفع وتأكيده.</li>
  <li>الرسوم: 30 دقيقة = 8 BHD · 45 دقيقة = 10 BHD · 60 دقيقة = 13 BHD (لكل جلسة).</li>
</ul>
<h4>٣. الإلغاء وإعادة الجدولة</h4>
<ul>
  <li>يُرجى الإبلاغ قبل <strong>24 ساعة على الأقل</strong> في حال الرغبة بالإلغاء أو تغيير الموعد.</li>
  <li>⚠️ <strong>لا يُسترد الدفع</strong> في حال الإلغاء بأقل من 24 ساعة من موعد الجلسة.</li>
  <li>إذا احتاجت ليلى إلى الإلغاء، ستُبلَّغ فوراً وسيتم ترتيب موعد بديل أو استرداد كامل.</li>
</ul>
<h4>٤. آداب الفصل</h4>
<ul>
  <li>تُعقد جميع الجلسات عبر <strong>Google Meet</strong>. سيُرسَل الرابط بعد التأكيد والدفع.</li>
  <li>يجب أن يكون الطالب في بيئة هادئة ومناسبة خلال الدرس.</li>
  <li>لا يُسمح بتسجيل الجلسات دون موافقة خطية مسبقة.</li>
  <li>يُتوقع احترام القرآن الكريم وبيئة التعلّم في جميع الأوقات.</li>
</ul>
<h4>٥. مسؤولية الطالب</h4>
<ul>
  <li>يُشجَّع الطلاب على التدرّب بين الجلسات لتحقيق أفضل النتائج.</li>
  <li>الاتصال الإنترنت المستقر هو مسؤولية الطالب أو ولي الأمر.</li>
  <li>للطلاب دون 18 سنة، يجب أن يكون أحد الوالدين أو الأوصياء حاضراً أو متاحاً خلال الدرس.</li>
</ul>
<h4>٦. الخصوصية</h4>
<ul>
  <li>لن تُستخدم معلوماتك الشخصية إلا لإدارة جلساتك ولن تُشارَك مع أي طرف ثالث.</li>
</ul>`
  },
  en: {
    htmlLang:'en', htmlDir:'ltr',
    pageTitle:'Layla Abdulla — Online Quran Lessons',
    heroTitle:'Online Quran with <em>Layla Abdulla</em>',
    heroTagline:'Private one-on-one Quran classes online — personalised, joyful, and focused entirely on you. From complete beginner to advanced Tajweed.',
    badges:['✓ Certificate of Recitation & Tajweed (Riwayat Hafs an Asim) — Ministry of Justice & Islamic Affairs, Bahrain','✓ Grade: Excellent','✓ 6+ Years Teaching Experience','✓ All Ages & Levels Welcome','✓ Via Google Meet'],
    avatarBadge:'Certified Teacher 🎓',
    aboutTitle:'Meet Your <em>Teacher</em>',
    aboutSub:'Qualified, experienced, and passionate about making Quran learning meaningful',
    certTitle:'Official Certification',
    certBody:'I hold the <strong>Certificate of Recitation & Tajweed — Riwayat Hafs an Asim</strong>, issued by the <strong>Ministry of Justice & Islamic Affairs in Bahrain</strong>, with a grade of <strong>Excellent</strong> — a formal recognition of my expertise in Quranic recitation and Tajweed rules.',
    expTitle:'6 Years of Experience',
    expBody:'I have been teaching Quran for over <strong>6 years</strong>, including online sessions with students of all ages and levels. I know how to adapt to every learner\'s pace and style.',
    tajweedTitle:'Correct Tajweed & Pronunciation',
    tajweedBody:'My focus is on helping you <strong>pronounce every letter from its correct origin</strong> and apply Tajweed rules properly — so your recitation is beautiful, accurate, and moving.',
    funTitle:'Fun, Focused & Thoughtful',
    funBody:'I make classes <strong>engaging and enjoyable</strong> while encouraging you to reflect on the meaning of what you recite. Learning the Quran should open your heart and mind — not just your tongue.',
    quoteText:'"Whether you are starting from scratch or refining your recitation, I am here to guide you with patience and care. My classes are small, personal, and built entirely around you — because every student deserves to feel the joy of connecting with the Book of Allah."',
    quoteCite:'— Layla Abdulla, Quran Teacher · Bahrain',
    pricingTitle:'<em>Class</em> Options',
    pricingSub:'All classes are fully private and one-on-one. Choose the duration that suits your schedule.',
    minLabel:' min', durSpan:' min',
    p1label:'Starter Session', p2label:'Standard Session', p3label:'Full Session',
    perSession:'per session', popLabel:'⭐ Most Popular',
    p1f:['Great for beginners & children','One clear topic per class','Short & focused','Fits any schedule'],
    p2f:['Best value option','Review + new material','Suits all levels','Balanced learning pace'],
    p3f:['Deep, thorough coverage','Ideal for advanced & Hifz','Extensive revision time','Maximum weekly progress'],
    paymentNote:'💳 Payment via <strong>BenefitPay</strong> — due before each class, after confirmation. No payment required during registration.',
    bookTitle:'Book Your <em>Session</em>',
    bookSub:'Fill in your details, pick a date and time — I\'ll confirm within 24 hours. No payment needed yet.',
    step1Label:'👤 Your Information',
    nameLabel:'Full Name *', namePlaceholder:'e.g. Fatima Hassan',
    ageLabel:'Age *', agePlaceholder:'e.g. 24',
    emailLabel:'Email Address *', emailPlaceholder:'your@email.com',
    waLabel:'WhatsApp Number *', waPlaceholder:'+973 3xxx xxxx',
    levelLabel:'Your Current Quran Level *',
    levelPlaceholder:'— Select your level —',
    levels:['🌱 Starter — No knowledge of Tajweed','📖 Beginner — Knows basic Tajweed','📚 Intermediate — Has some knowledge','🏆 Advanced — Preparing for Quran exams','🤲 Quran Memorisation — I can help you memorise'],
    goalLabel:'Your Goal (optional)',
    goalPlaceholder:'e.g. I want to read fluently with correct Tajweed, or I want to memorise specific Surahs...',
    step2Label:'⏱️ Choose Class Duration',
    durNote1:'Starter', durNote2:'⭐ Popular', durNote3:'Full Session',
    noDurationNotice:'⚠️ Please select a class duration first before choosing a date.',
    step3Label:'📅 Choose a Date',
    calIntro:'Available: <strong>Friday & Saturday mornings</strong> (9:00 AM – 12:00 PM) and <strong>Tuesday & Wednesday evenings</strong> (7:00 PM – 9:00 PM). Green dates are open.',
    legendAvail:'Available', legendSel:'Selected', legendOff:'Unavailable',
    timeSlotsLabel:'Available Times',
    until:'until',
    noSlots:'No slots available for this duration',
    tcTitle:'📋 Terms & Conditions',
    tcAcceptLabel:'I have read and agree to the Terms & Conditions above. I understand that <strong>no payment is required at this stage</strong>, and that payment will be made via <strong>BenefitPay before each confirmed session</strong>.',
    submitBtn:'✉️ Submit Booking Request',
    submitNote:'I\'ll review your request and get back to you within 24 hours to confirm. 🤲 No payment needed until your session is confirmed.',
    successTitle:'Request Received! 🎉',
    successMsg:'JazakAllahu Khayran! Your booking request has been submitted. I\'ll contact you within 24 hours via email or WhatsApp to confirm your session. No payment needed until confirmation. 🤲',
    footerVerse:'"And recite the Quran with measured recitation." — Surah Al-Muzzammil 73:4',
    footerDesc:'Certified Quran Teacher · Bahrain',
    footerPlatform:'Sessions via Google Meet · Payment via BenefitPay',
    footerCopy:'© 2025 Layla Abdulla Online Quran Lessons. All rights reserved.',
    months:["January","February","March","April","May","June","July","August","September","October","November","December"],
    daysShort:["Sun","Mon","Tue","Wed","Thu","Fri","Sat"],
    daysFull:["Sunday","Monday","Tuesday","Wednesday","Thursday","Friday","Saturday"],
    summaryDate:'Date', summaryTime:'Time', summaryDuration:'Duration',
    alertDuration:'Please choose a class duration (30, 45, or 60 minutes).',
    alertSlot:'Please select a date and time slot from the calendar.',
    alertTC:'Please read and accept the Terms & Conditions to continue.',
    sending:'Sending…',
    errGeneral:'Something went wrong. Please try again.',
    errNetwork:'Network error. Please check your connection.',
    tcHTML:`
<h4>1. Registration & Confirmation</h4>
<ul>
  <li>Submitting this form is an <strong>initial registration only</strong> — it does not guarantee a confirmed booking.</li>
  <li>Layla will contact you within <strong>24 hours</strong> via email or WhatsApp to confirm your slot.</li>
  <li>Your booking is only confirmed after you receive written confirmation from her.</li>
  <li>⚠️ If you do not receive a reply within <strong>48 hours</strong>, the requested slot is <strong>unavailable</strong>. Please submit a new request with a different date or time.</li>
</ul>
<h4>2. Payment</h4>
<ul>
  <li><strong>No payment is required during registration.</strong></li>
  <li>Payment must be made <strong>before each class begins</strong> in order to confirm your booking.</li>
  <li>All payments are made via <strong>BenefitPay</strong>. Payment details will be provided upon confirmation.</li>
  <li>The class will not begin until payment has been received and confirmed.</li>
  <li>Fees: 30 min = 8 BHD · 45 min = 10 BHD · 60 min = 13 BHD (per session).</li>
</ul>
<h4>3. Cancellation & Rescheduling</h4>
<ul>
  <li>Please provide at least <strong>24 hours' notice</strong> to cancel or reschedule without penalty.</li>
  <li>⚠️ <strong>No refunds</strong> will be given for cancellations made less than 24 hours before the session.</li>
  <li>If Layla needs to cancel, you will be notified immediately and offered a replacement slot or a full refund.</li>
</ul>
<h4>4. Class Conduct</h4>
<ul>
  <li>All sessions are held via <strong>Google Meet</strong>. A link will be sent after confirmation and payment.</li>
  <li>Students must be in a quiet, appropriate environment during class.</li>
  <li>Recording of sessions is not permitted without prior written consent.</li>
  <li>Respect for the Quran and the learning environment is expected at all times.</li>
</ul>
<h4>5. Student Responsibility</h4>
<ul>
  <li>Students are encouraged to practise between sessions for best results.</li>
  <li>A stable internet connection is the student's (or parent's) responsibility.</li>
  <li>For students under 18, a parent or guardian must be present or reachable during class.</li>
</ul>
<h4>6. Privacy</h4>
<ul>
  <li>Your personal information will only be used to manage your sessions and will never be shared with third parties.</li>
</ul>`
  }
};

// ── STATE ───────────────────────────────────────────────────
let currentLang = 'ar';
let today = new Date(), viewYear = today.getFullYear(), viewMonth = today.getMonth();
let selectedDay = null, selectedTime = null, selectedDurationMinutes = null, selectedDurationLabel = null;

// ── SET LANGUAGE ────────────────────────────────────────────
function setLang(lang) {
  currentLang = lang;
  const t = T[lang];
  const html = document.documentElement;
  html.lang = t.htmlLang;
  html.dir = t.htmlDir;
  document.title = t.pageTitle;

  document.getElementById('btnAR').classList.toggle('active', lang==='ar');
  document.getElementById('btnEN').classList.toggle('active', lang==='en');

  // Hero
  document.getElementById('heroTitle').innerHTML = t.heroTitle;
  document.getElementById('heroTagline').textContent = t.heroTagline;
  const badgesEl = document.getElementById('heroBadges');
  badgesEl.innerHTML = t.badges.map(b=>`<span class="badge">${b}</span>`).join('');
  document.getElementById('avatarBadge').textContent = t.avatarBadge;

  // About
  document.getElementById('aboutTitle').innerHTML = t.aboutTitle;
  document.getElementById('aboutSub').textContent = t.aboutSub;
  document.getElementById('cert-title').textContent = t.certTitle;
  document.getElementById('cert-body').innerHTML = t.certBody;
  document.getElementById('exp-title').textContent = t.expTitle;
  document.getElementById('exp-body').innerHTML = t.expBody;
  document.getElementById('tajweed-title').textContent = t.tajweedTitle;
  document.getElementById('tajweed-body').innerHTML = t.tajweedBody;
  document.getElementById('fun-title').textContent = t.funTitle;
  document.getElementById('fun-body').innerHTML = t.funBody;
  document.getElementById('quoteText').textContent = t.quoteText;
  document.getElementById('quoteCite').textContent = t.quoteCite;

  // Pricing
  document.getElementById('pricingTitle').innerHTML = t.pricingTitle;
  document.getElementById('pricingSub').textContent = t.pricingSub;
  ['1','2','3'].forEach(n => {
    document.getElementById('minLabel'+n).textContent = t.minLabel;
    document.getElementById('perSession'+n).textContent = t.perSession;
  });
  document.getElementById('p1label').textContent = t.p1label;
  document.getElementById('p2label').textContent = t.p2label;
  document.getElementById('p3label').textContent = t.p3label;
  document.getElementById('popLabel').textContent = t.popLabel;
  ['p1features','p2features','p3features'].forEach((id,i) => {
    const feats = [t.p1f, t.p2f, t.p3f][i];
    document.getElementById(id).innerHTML = feats.map(f=>`<li>${f}</li>`).join('');
  });
  document.getElementById('paymentNote').innerHTML = t.paymentNote;

  // Form
  document.getElementById('bookTitle').innerHTML = t.bookTitle;
  document.getElementById('bookSub').textContent = t.bookSub;
  document.getElementById('step1Label').textContent = t.step1Label;
  document.getElementById('nameLabel').textContent = t.nameLabel;
  document.getElementById('studentName').placeholder = t.namePlaceholder;
  document.getElementById('ageLabel').textContent = t.ageLabel;
  document.getElementById('ageInput').placeholder = t.agePlaceholder;
  document.getElementById('emailLabel').textContent = t.emailLabel;
  document.getElementById('emailInput').placeholder = t.emailPlaceholder;
  document.getElementById('waLabel').textContent = t.waLabel;
  document.getElementById('waInput').placeholder = t.waPlaceholder;
  document.getElementById('levelLabel').textContent = t.levelLabel;

  // Level options
  const sel = document.getElementById('levelSelect');
  const currentVal = sel.value;
  sel.innerHTML = `<option value="" disabled>${t.levelPlaceholder}</option>` +
    t.levels.map((l,i)=>`<option value="${l}">${l}</option>`).join('');
  sel.value = '';

  document.getElementById('goalLabel').textContent = t.goalLabel;
  document.getElementById('goalInput').placeholder = t.goalPlaceholder;
  document.getElementById('step2Label').textContent = t.step2Label;
  document.getElementById('durSpan1').textContent = ' '+t.durSpan;
  document.getElementById('durSpan2').textContent = ' '+t.durSpan;
  document.getElementById('durSpan3').textContent = ' '+t.durSpan;
  document.getElementById('durNote1').textContent = t.durNote1;
  document.getElementById('durNote2').textContent = t.durNote2;
  document.getElementById('durNote3').textContent = t.durNote3;
  document.getElementById('noDurationNotice').textContent = t.noDurationNotice;
  document.getElementById('step3Label').textContent = t.step3Label;
  document.getElementById('calIntroText').innerHTML = t.calIntro;
  document.getElementById('legendAvail').textContent = t.legendAvail;
  document.getElementById('legendSel').textContent = t.legendSel;
  document.getElementById('legendOff').textContent = t.legendOff;
  document.getElementById('timeSlotsLabel').textContent = t.timeSlotsLabel;
  document.getElementById('tcTitle').textContent = t.tcTitle;
  document.getElementById('tcBox').innerHTML = t.tcHTML;
  document.getElementById('tcAcceptLabel').innerHTML = t.tcAcceptLabel;
  document.getElementById('submitBtn').textContent = t.submitBtn;
  document.getElementById('submitNote').textContent = t.submitNote;
  document.getElementById('successTitle').textContent = t.successTitle;
  document.getElementById('successMsg').textContent = t.successMsg;
  document.getElementById('footerVerse').textContent = t.footerVerse;
  document.getElementById('footerDesc').textContent = t.footerDesc;
  document.getElementById('footerPlatform').textContent = t.footerPlatform;
  document.getElementById('footerCopy').textContent = t.footerCopy;

  // Duration label update
  if (selectedDurationMinutes) {
    const card = document.querySelector('.dur-card.selected');
    if (card) selectedDurationLabel = card.getAttribute('data-duration-'+lang) + ' — ' + card.dataset.price;
  }

  renderCalendarHeaders();
  renderCalendar();
  if (selectedDay) renderTimeSlots(selectedDay.d, selectedDay.m, selectedDay.y, selectedDay.dow);
  updateSummary();
}

// ── CALENDAR ────────────────────────────────────────────────
function renderCalendarHeaders() {
  const hdr = document.getElementById('calHeaders');
  hdr.innerHTML = '';
  T[currentLang].daysShort.forEach(d => {
    const el = document.createElement('div');
    el.className = 'cal-header';
    el.textContent = d;
    hdr.appendChild(el);
  });
}

function renderCalendar() {
  const grid = document.getElementById('calGrid');
  document.getElementById('monthLabel').textContent = T[currentLang].months[viewMonth] + ' ' + viewYear;
  grid.innerHTML = '';
  const firstDay = new Date(viewYear, viewMonth, 1).getDay();
  const days = new Date(viewYear, viewMonth+1, 0).getDate();
  for (let i=0; i<firstDay; i++) { const e=document.createElement('div');e.className='cal-day empty';grid.appendChild(e); }
  for (let d=1; d<=days; d++) {
    const cell = document.createElement('div'); cell.textContent = d;
    const dt = new Date(viewYear, viewMonth, d);
    const dow = dt.getDay();
    const isPast = dt < new Date(today.getFullYear(), today.getMonth(), today.getDate());
    const isToday = (d===today.getDate()&&viewMonth===today.getMonth()&&viewYear===today.getFullYear());
    const isAvail = DAY_WINDOWS[dow] && !isPast;
    const isSel = selectedDay&&selectedDay.d===d&&selectedDay.m===viewMonth&&selectedDay.y===viewYear;
    if (isSel) cell.className='cal-day selected';
    else if (isAvail) {
      cell.className='cal-day available';
      cell.addEventListener('click', () => {
        if (!selectedDurationMinutes) {
          document.getElementById('noDurationNotice').classList.add('visible');
          document.getElementById('noDurationNotice').scrollIntoView({behavior:'smooth',block:'center'});
          return;
        }
        selectDay(d, viewMonth, viewYear, dow);
      });
    } else cell.className='cal-day disabled';
    if (isToday) cell.classList.add('today-ring');
    grid.appendChild(cell);
  }
}

function selectDay(d,m,y,dow) {
  selectedDay={d,m,y,dow}; selectedTime=null;
  document.getElementById('hiddenDate').value='';
  document.getElementById('hiddenTime').value='';
  renderCalendar(); renderTimeSlots(d,m,y,dow); updateSummary();
}

function renderTimeSlots(d,m,y,dow) {
  const box=document.getElementById('timeSlots'),lbl=document.getElementById('selectedDateLabel'),sg=document.getElementById('slotGrid');
  const t=T[currentLang];
  const dt=new Date(y,m,d);
  lbl.textContent = t.daysFull[dt.getDay()] + ' ' + d + ' ' + t.months[m];
  sg.innerHTML='';
  const slots = generateSlots(dow, selectedDurationMinutes||30);
  if (!slots.length) {
    sg.innerHTML=`<span style="color:var(--muted);font-size:13px;">${t.noSlots}</span>`;
  }
  slots.forEach(s => {
    const btn=document.createElement('div'); btn.className='slot';
    const endStr=minutesToTime(timeToMinutes(s)+selectedDurationMinutes);
    btn.innerHTML=`${s}<span class="slot-duration-note">${t.until} ${endStr}</span>`;
    btn.addEventListener('click',()=>{
      document.querySelectorAll('.slot').forEach(x=>x.classList.remove('selected'));
      btn.classList.add('selected'); selectedTime=s;
      document.getElementById('hiddenDate').value=t.daysFull[dt.getDay()]+', '+d+' '+t.months[m]+' '+y;
      document.getElementById('hiddenTime').value=s+' – '+endStr;
      updateSummary();
    });
    sg.appendChild(btn);
  });
  box.classList.add('visible');
}

function timeToMinutes(t) {
  const [time,ampm]=t.split(' '); let [h,m]=time.split(':').map(Number);
  if(ampm==='PM'&&h!==12)h+=12; if(ampm==='AM'&&h===12)h=0;
  return h*60+m;
}
function minutesToTime(mins) {
  const h=Math.floor(mins/60),m=mins%60,ampm=h>=12?'PM':'AM';
  const h12=h>12?h-12:(h===0?12:h);
  return `${h12}:${m===0?'00':m} ${ampm}`;
}

function updateSummary() {
  const box=document.getElementById('summaryBox');
  if (selectedDay&&selectedTime&&selectedDurationMinutes) {
    const t=T[currentLang];
    const dt=new Date(selectedDay.y,selectedDay.m,selectedDay.d);
    const ds=t.daysFull[dt.getDay()]+' '+selectedDay.d+' '+t.months[selectedDay.m]+' '+selectedDay.y;
    const endStr=minutesToTime(timeToMinutes(selectedTime)+selectedDurationMinutes);
    box.innerHTML=`✅ <strong>${t.summaryDate}:</strong> ${ds} &nbsp;·&nbsp; <strong>${t.summaryTime}:</strong> ${selectedTime} – ${endStr} &nbsp;·&nbsp; <strong>${t.summaryDuration}:</strong> ${selectedDurationLabel}`;
    box.classList.add('visible');
  } else box.classList.remove('visible');
}

function selectDuration(el) {
  document.querySelectorAll('.dur-card').forEach(c=>c.classList.remove('selected'));
  el.classList.add('selected');
  selectedDurationMinutes=parseInt(el.dataset.minutes);
  selectedDurationLabel=el.getAttribute('data-duration-'+currentLang)+' — '+el.dataset.price;
  document.getElementById('hiddenDuration').value=selectedDurationLabel;
  document.getElementById('noDurationNotice').classList.remove('visible');
  if (selectedDay) {
    selectedTime=null; document.getElementById('hiddenTime').value='';
    renderTimeSlots(selectedDay.d,selectedDay.m,selectedDay.y,selectedDay.dow);
  }
  updateSummary();
}

document.getElementById('prevMonth').addEventListener('click',()=>{viewMonth--;if(viewMonth<0){viewMonth=11;viewYear--;}renderCalendar();});
document.getElementById('nextMonth').addEventListener('click',()=>{viewMonth++;if(viewMonth>11){viewMonth=0;viewYear++;}renderCalendar();});

document.getElementById('bookingForm').addEventListener('submit',async function(e){
  e.preventDefault();
  const t=T[currentLang];
  if (!selectedDurationMinutes){alert(t.alertDuration);return;}
  if (!selectedDay||!selectedTime){alert(t.alertSlot);return;}
  if (!document.getElementById('tcCheck').checked){alert(t.alertTC);return;}
  const btn=document.getElementById('submitBtn');
  btn.textContent=t.sending; btn.disabled=true;
  try {
    const res=await fetch(this.action,{method:'POST',body:new FormData(this),headers:{'Accept':'application/json'}});
    if (res.ok){
      this.style.display='none';
      document.getElementById('successScreen').style.display='block';
    } else {
      alert(t.errGeneral); btn.textContent=t.submitBtn; btn.disabled=false;
    }
  } catch {
    alert(t.errNetwork); btn.textContent=t.submitBtn; btn.disabled=false;
  }
});

// ── INIT ────────────────────────────────────────────────────
setLang('ar');
</script>

</body>
</html>
