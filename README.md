<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>وكالة وزارة الداخلية | النظام الإداري</title>
  <style>
    :root {
      --gold: #d4af37;
      --gold-glow: rgba(212, 175, 55, 0.6);
      --deep-blue: #020617; /* لون أزرق داكن جداً للخلفية */
      --glass-blue: rgba(15, 23, 42, 0.85);
    }

    body {
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      /* خلفية مظلمة مع تدرج أزرق وصورة مركز الشرطة مظللة */
      background: linear-gradient(rgba(2, 6, 23, 0.92), rgba(2, 6, 23, 0.92)), 
                  url('https://c.top4top.io/p_3045437871.jpg');
      background-size: cover;
      background-position: center;
      background-attachment: fixed;
      color: white;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
    }

    header {
      text-align: center;
      padding: 60px 20px 30px;
    }

    /* العنوان باللون الذهبي مع توهج وظلال */
    header h1 {
      margin: 0;
      font-size: 3.2rem;
      color: var(--gold);
      font-weight: bold;
      text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.8), 
                   0 0 25px var(--gold-glow);
      letter-spacing: 1px;
    }

    /* شريط الوقت الذهبي والأزرق */
    .time-container {
      display: inline-flex;
      background: rgba(0, 0, 0, 0.4);
      border: 1px solid rgba(212, 175, 55, 0.3);
      padding: 12px 30px;
      border-radius: 50px;
      margin-top: 25px;
      gap: 25px;
      backdrop-filter: blur(8px);
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
    }

    .time-item {
      display: flex;
      align-items: center;
      gap: 12px;
      font-size: 1.1rem;
      color: #cbd5e1;
    }

    .time-item span { 
      color: var(--gold); 
      font-size: 1.3rem; 
      filter: drop-shadow(0 0 5px var(--gold));
    }

    .menu {
      width: 90%;
      max-width: 650px;
      margin-top: 20px;
      display: flex;
      flex-direction: column;
      gap: 18px;
    }

    /* الأزرار مع تأثير الظل والخلفية الزرقاء الزجاجية */
    .item {
      background: var(--glass-blue);
      backdrop-filter: blur(15px);
      border: 1px solid rgba(212, 175, 55, 0.15);
      border-radius: 15px;
      padding: 22px;
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 15px;
      cursor: pointer;
      text-decoration: none;
      color: white;
      font-size: 1.3rem;
      font-weight: 500;
      transition: all 0.4s ease;
      /* ظل خارجي لإعطاء عمق */
      box-shadow: 0 15px 35px rgba(0, 0, 0, 0.4);
    }

    .item:hover {
      transform: translateY(-5px);
      border-color: var(--gold);
      background: rgba(30, 41, 59, 0.95);
      box-shadow: 0 20px 40px rgba(0, 0, 0, 0.6), 
                   0 0 15px rgba(212, 175, 55, 0.2);
    }

    .item i {
      color: var(--gold);
      font-size: 1.5rem;
      order: 1; /* الأيقونة بجانب النص */
      filter: drop-shadow(0 0 3px rgba(212, 175, 55, 0.5));
    }

    .section {
      display: none;
      width: 90%;
      max-width: 650px;
      background: rgba(15, 23, 42, 0.98);
      border-radius: 20px;
      padding: 35px;
      border: 1px solid var(--gold);
      margin-top: 30px;
      text-align: center;
      box-shadow: 0 0 50px rgba(0,0,0,0.8);
      animation: fadeIn 0.5s ease;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .active { display: block; }

    .btn-submit {
      background: linear-gradient(135deg, #b8860b, var(--gold));
      color: black;
      border: none;
      padding: 15px;
      border-radius: 10px;
      font-weight: bold;
      width: 100%;
      cursor: pointer;
      font-size: 1.2rem;
      margin-top: 20px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.3);
    }

    textarea {
      width: 100%; height: 120px; background: #020617; border: 1px solid #1e293b;
      border-radius: 10px; color: white; padding: 15px; resize: none; font-family: inherit;
    }
  </style>
</head>
<body>

<header>
  <h1>وكالة وزارة الداخلية</h1>
  
  <div class="time-container">
    <div class="time-item"><span>📅</span> <div id="current-date">--/--/----</div></div>
    <div class="time-item"><span>🕒</span> <div id="current-time">--:--:--</div></div>
  </div>
</header>

<div class="menu">
  <a class="item" href="https://docs.google.com/spreadsheets/d/1Ee9GMPOqHxCDhkBt5is3zKOQuCltZaKaRlUqF0lw2Sw/edit?gid=1195403074" target="_blank">
    <span>لائحة المفصولين</span>
    <i>⬅</i>
  </a>

  <a class="item" href="https://docs.google.com/spreadsheets/d/1C0GfDF-tEjtcrVMF1dYMbzy6wDgHj7oxxSgVBaii1FA/edit?gid=0" target="_blank">
    <span>لائحة الوكالة</span>
    <i>⬅</i>
  </a>

  <a class="item" href="https://docs.google.com/forms/d/1A9LpBKg3ISXqyCUeIFGY4CWmQqju6lvSZC2Kv5FP14Q/viewform" target="_blank">
    <span>طلب ترقية</span>
    <i>✚</i>
  </a>

  <div class="item" onclick="toggleSection('complaint')">
    <span>شكوى إدارية</span>
    <i>✖</i>
  </div>

  <div class="item" onclick="toggleSection('suggestion')">
    <span>تقديم اقتراح</span>
    <i>💡</i>
  </div>
</div>

<div id="complaint" class="section">
  <h2 style="color: var(--gold);">تقديم شكوى رسمية</h2>
  <textarea placeholder="اكتب تفاصيل الشكوى هنا..."></textarea>
  <button class="btn-submit">إرسال البلاغ</button>
</div>

<div id="suggestion" class="section">
  <h2 style="color: var(--gold);">تقديم اقتراح تطويري</h2>
  <textarea placeholder="شاركنا أفكارك لتحسين العمل..."></textarea>
  <button class="btn-submit">إرسال المقترح</button>
</div>

<script>
  function updateClock() {
    const now = new Date();
    document.getElementById('current-time').innerText = now.toLocaleTimeString('ar-EG', { hour: '2-digit', minute: '2-digit', second: '2-digit' });
    document.getElementById('current-date').innerText = now.toLocaleDateString('ar-EG', { day: '2-digit', month: '2-digit', year: 'numeric' });
  }
  setInterval(updateClock, 1000);
  updateClock();

  function toggleSection(id) {
    document.querySelectorAll('.section').forEach(s => s.classList.remove('active'));
    document.getElementById(id).classList.add('active');
    document.getElementById(id).scrollIntoView({ behavior: 'smooth' });
  }
</script>

</body>
</html>
