<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>وكالة وزارة الداخلية | النظام الإداري</title>
  <style>
    :root {
      --gold: #d4af37;
      --deep-blue: #020617;
      --glass: rgba(15, 23, 42, 0.9);
    }

    body {
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      /* خلفية مظلمة جداً مع تظليل احترافي */
      background: linear-gradient(rgba(2, 6, 23, 0.95), rgba(2, 6, 23, 0.95)), 
                  url('https://c.top4top.io/p_3045437871.jpg');
      background-size: cover;
      background-position: center;
      background-attachment: fixed;
      color: white;
      display: flex;
      flex-direction: column;
      align-items: center;
      min-height: 100vh;
    }

    header {
      text-align: center;
      padding: 50px 20px 10px;
    }

    header h1 {
      margin: 0;
      font-size: 2.8rem;
      color: var(--gold);
      text-shadow: 0 0 20px rgba(212, 175, 55, 0.5);
    }

    .time-bar {
      display: inline-flex;
      background: rgba(0, 0, 0, 0.5);
      border: 1px solid rgba(212, 175, 55, 0.3);
      padding: 8px 20px;
      border-radius: 10px;
      margin-top: 15px;
      gap: 15px;
      font-size: 0.9rem;
    }

    /* خانة الاستعلام المطورة */
    .search-section {
      width: 90%;
      max-width: 600px;
      margin-top: 30px;
      background: rgba(15, 23, 42, 0.7);
      padding: 15px;
      border-radius: 15px;
      border: 1px solid var(--gold);
      display: flex;
      gap: 10px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.5);
    }

    .search-section input {
      flex: 1;
      background: #000;
      border: 1px solid #333;
      border-radius: 8px;
      color: white;
      padding: 10px;
      text-align: center;
    }

    .search-section button {
      background: #ffcc00;
      color: black;
      border: none;
      padding: 0 20px;
      border-radius: 8px;
      font-weight: bold;
      cursor: pointer;
    }

    /* القوائم المركزية */
    .menu {
      width: 90%;
      max-width: 600px;
      margin-top: 20px;
      display: flex;
      flex-direction: column;
      gap: 12px;
      padding-bottom: 50px;
    }

    .item {
      background: var(--glass);
      border: 1px solid rgba(212, 175, 55, 0.2);
      border-radius: 12px;
      padding: 18px;
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 15px;
      color: white;
      text-decoration: none;
      font-size: 1.2rem;
      transition: 0.3s;
    }

    .item:hover {
      background: rgba(30, 41, 59, 0.9);
      border-color: var(--gold);
      transform: translateY(-3px);
    }

    .item i { color: var(--gold); order: 1; }
  </style>
</head>
<body>

<header>
  <h1>وكالة وزارة الداخلية</h1>
  <div class="time-bar">
    <span id="date-now">📅 --/--/----</span>
    <span id="time-now">🕒 --:--:--</span>
  </div>
</header>

<div class="search-section">
  <button onclick="alert('جاري الاستعلام...')">استعلام</button>
  <input type="text" placeholder="ادخل رقم الطلب أو الملف">
</div>

<div class="menu">
  <a class="item" href="https://docs.google.com/spreadsheets/d/1Ee9GMPOqHxCDhkBt5is3zKOQuCltZaKaRlUqF0lw2Sw/edit?gid=1195403074" target="_blank">
    <span>لائحة المفصولين</span><i>⬅</i>
  </a>
  <a class="item" href="https://docs.google.com/spreadsheets/d/1C0GfDF-tEjtcrVMF1dYMbzy6wDgHj7oxxSgVBaii1FA/edit?gid=0" target="_blank">
    <span>لائحة الوكالة</span><i>⬅</i>
  </a>
  <a class="item" href="https://docs.google.com/forms/d/1A9LpBKg3ISXqyCUeIFGY4CWmQqju6lvSZC2Kv5FP14Q/viewform" target="_blank">
    <span>طلب ترقية</span><i>✚</i>
  </a>
  <div class="item" style="cursor:pointer;"><span>شكوى إدارية</span><i>✖</i></div>
  <div class="item" style="cursor:pointer;"><span>تقديم اقتراح</span><i>💡</i></div>
</div>

<script>
  function updateClock() {
    const now = new Date();
    document.getElementById('time-now').innerText = "🕒 " + now.toLocaleTimeString('ar-EG');
    document.getElementById('date-now').innerText = "📅 " + now.toLocaleDateString('ar-EG');
  }
  setInterval(updateClock, 1000);
  updateClock();
</script>

</body>
</html>
