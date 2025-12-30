<!DOCTYPE html>
<html lang="he" dir="rtl">
<head>
  <meta charset="UTF-8" />
  <title>האחים מכונית בע"מ 🚗💦🧽</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: url('background.jpg') center/cover fixed no-repeat;
      /* גיבוי במקרה שאין תמונת רקע */
      background-color: #e8f2ff;
      color: #222;
    }

    header {
      position: relative;
      padding: 60px 20px;
      text-align: center;
      color: white;
    }

    header::before {
      content: "";
      position: absolute;
      inset: 0;
      background: rgba(10, 80, 160, 0.7);
    }

    header * {
      position: relative;
      z-index: 1;
    }

    .team-note {
      position: absolute;
      left: 20px;
      top: 20px;
      font-weight: bold;
    }

    section {
      background: white;
      max-width: 900px;
      margin: 20px auto;
      padding: 20px;
      border-radius: 12px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
    }

    h2 {
      color: #0a74da;
    }

    ul {
      line-height: 1.8;
    }

    button {
      background: #0a74da;
      color: white;
      border: none;
      padding: 12px;
      width: 100%;
      border-radius: 8px;
      font-size: 16px;
      cursor: pointer;
    }

    button:hover {
      background: #085bb0;
    }

    input, select, textarea {
      width: 100%;
      padding: 8px;
      margin-top: 5px;
      border-radius: 6px;
      border: 1px solid #ccc;
      box-sizing: border-box;
    }

    footer {
      text-align: center;
      padding: 15px;
      color: #666;
    }

    /* דירוג */
    .rating-box {
      position: fixed;
      right: 20px;
      top: 140px;
      width: 230px;
      background: #ffffffee;
      border-radius: 12px;
      padding: 12px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.2);
      z-index: 999;
    }

    .rating-box h3 {
      text-align: center;
      color: #0a74da;
      margin-top: 0;
    }

    .stars {
      text-align: center;
      font-size: 22px;
      cursor: pointer;
      user-select: none;
    }

    .stars span {
      filter: grayscale(100%);
      margin: 0 1px;
    }

    .stars span.active {
      filter: grayscale(0%);
    }

    .review {
      border-bottom: 1px solid #eee;
      padding: 10px 0;
    }

    .stars-view {
      color: gold;
      margin: 4px 0;
    }

    /* קצת ריווח בין קופסאות */
    .rating-box + .rating-box {
      margin-top: 10px;
    }

    /* מובייל */
    @media (max-width: 980px) {
      .rating-box {
        position: static;
        width: auto;
        max-width: 900px;
        margin: 10px auto;
      }
    }
  </style>
</head>

<body>

<header>
  <div class="team-note">👥 אנחנו 4 אנשים בעסק</div>
  <h1>האחים מכונית בע"מ 🚗💦🧽</h1>
  <p style="color:black;font-weight:bold;">
    (🚗💦🧽 יהיו ימי שישי שלא תתקיים שטיפה בשל סיבות פרטיות, בבקשה הבינו זאת)
  </p>
</header>

<div class="rating-box">
  <h3>דרגו אותנו ⭐</h3>
  <div class="stars" id="stars" aria-label="דירוג כוכבים">
    <span data-value="1" title="1">⭐</span>
    <span data-value="2" title="2">⭐</span>
    <span data-value="3" title="3">⭐</span>
    <span data-value="4" title="4">⭐</span>
    <span data-value="5" title="5">⭐</span>
  </div>
  <input type="text" id="reviewName" placeholder="השם שלכם" />
  <textarea id="feedback" placeholder="כתבו משוב קצר..."></textarea>
  <button type="button" onclick="sendFeedback()">שלח משוב</button>
</div>

<div class="rating-box" style="top:360px;">
  <h3>⭐ חוות דעת</h3>
  <div id="reviewsList"></div>
</div>

<section>
  <h2>שעות פתיחה</h2>
  <p>🕘 09:00 – 14:30</p>
  <p><strong>יום שישי בלבד</strong><br>חופשת פסח וחלק מהחופש הגדול</p>
</section>

<section>
  <h2>מחירים</h2>
  <ul>
    <li>🚗 פנים + חוץ – 60 ₪</li>
    <li>🚿 חוץ בלבד – 25 ₪</li>
    <li>🧼 פנים בלבד – 35 ₪</li>
  </ul>
</section>

<section>
  <h2>זמן שטיפה</h2>
  <ul>
    <li>פנים + חוץ: 30–35 דקות</li>
    <li>חוץ בלבד: 15–20 דקות</li>
    <li>פנים בלבד: 20–25 דקות</li>
  </ul>
</section>

<section>
  <h2>הזמנת שטיפה</h2>
  <p style="color:#c0392b;font-weight:bold;">
    ⚠️ (בחירת שעה לא מראה אם תפוס – אנחנו נעדכן אתכם)
  </p>

  <form onsubmit="sendWhatsApp(event)">
    <label for="name">שם מלא</label>
    <input id="name" required />

    <label for="phone">טלפון</label>
    <input id="phone" type="tel" required />

    <label for="service">סוג שטיפה</label>
    <select id="service">
      <option>פנים וחוץ – 60 ₪</option>
      <option>חוץ בלבד – 25 ₪</option>
      <option>פנים בלבד – 35 ₪</option>
    </select>

    <label for="time">שעה (מרווחים של 35 דקות)</label>
    <select id="time"></select>

    <button type="submit">שלח בוואטסאפ</button>
  </form>
</section>

<footer>
  © האחים מכונית בע"מ 🚗💦
</footer>

<script>
  // --- CONFIGURATION ---
  const CAL_API_URL = "https://script.google.com/macros/s/AKfycbyXvLZwr3MQSjNPKf6cjFtu8R7IX33jzKicFMVTII6j_ChF-vQ4OrD3JDqTyOjw95_6/exec";
  const CAL_TOKEN = "X9mP2qL8vR4nK7jW3yB5tH6dC1sF0gZ2xM8bV4lQ";
  // ---------------------
  // ---------------------------
  // תורים (שעות תפוסות מקומיות)
  // ---------------------------
  // חשוב לדעת: localStorage הוא לפי מכשיר/דפדפן ולא "שרת".
  // כדי שזה יהיה משותף לכל הלקוחות צריך צד-שרת (Database).
  let takenTimes = ['10:30', '11:15'];

  try {
    const saved = JSON.parse(localStorage.getItem('takenTimes')) || [];
    takenTimes = [...new Set([...takenTimes, ...saved])];
  } catch (e) {
    // אם יש ערך לא תקין ב-localStorage פשוט מתעלמים
  }

  // יצירת שעות
  const timeSelect = document.getElementById('time');
  let start = 9 * 60;           // 09:00
  const end = 14 * 60 + 30;     // 14:30

  while (start <= end) {
    const h = String(Math.floor(start / 60)).padStart(2, '0');
    const m = String(start % 60).padStart(2, '0');
    const t = `${h}:${m}`;

    const opt = document.createElement('option');
    opt.value = t;
    opt.textContent = t;

    if (takenTimes.includes(t)) {
      opt.disabled = true;
      opt.textContent += ' (תפוס)';
    }

    timeSelect.appendChild(opt);
    start += 35;
  }

  // שליחה לוואטסאפ
  function sendWhatsApp(e) {
    e.preventDefault();

    const fullName = document.getElementById('name').value.trim();
    const phone = document.getElementById('phone').value.trim();
    const service = document.getElementById('service').value;
    const time = document.getElementById('time').value;

    if (!fullName || !phone || !time) {
      alert('אנא מלאו שם, טלפון ושעה.');
      return;
    }

    // שמירת שעה כתפוסה (מקומית)
    takenTimes = [...new Set([...takenTimes, time])];
    localStorage.setItem('takenTimes', JSON.stringify(takenTimes));

    const msg =
`הזמנה חדשה:
שם: ${fullName}
טלפון: ${phone}
שירות: ${service}
שעה: ${time}`;

    const url = `https://wa.me/972585378542?text=${encodeURIComponent(msg)}`;
    window.location.href = url;
  }

  // ---------------------------
  // דירוג + חוות דעת
  // ---------------------------
  let selectedRating = 0;
  const starEls = Array.from(document.querySelectorAll('#stars span'));

  starEls.forEach((s, i) => {
    s.addEventListener('click', () => {
      selectedRating = i + 1;
      starEls.forEach((x, idx) => x.classList.toggle('active', idx < selectedRating));
    });
  });

  function loadReviews() {
    const list = document.getElementById('reviewsList');
    list.innerHTML = '';

    let reviews = [];
    try {
      reviews = JSON.parse(localStorage.getItem('reviews')) || [];
    } catch (e) {
      reviews = [];
    }

    if (!reviews.length) {
      list.innerHTML = '<div style="color:#777;">עדיין אין חוות דעת.</div>';
      return;
    }

    reviews.forEach(r => {
      const d = document.createElement('div');
      d.className = 'review';
      const safeName = (r.name || 'לקוח אנונימי');
      const safeText = (r.text || '');

      d.innerHTML = `
        <strong>${escapeHtml(safeName)}</strong>
        <div class="stars-view">${'⭐'.repeat(Number(r.rating || 0))}</div>
        <div>${escapeHtml(safeText)}</div>
      `;
      list.appendChild(d);
    });
  }

  function sendFeedback() {
    if (!selectedRating) {
      alert('בחר כוכבים');
      return;
    }

    const name = document.getElementById('reviewName').value.trim() || 'לקוח אנונימי';
    const text = document.getElementById('feedback').value.trim();

    if (!text) {
      alert('אנא כתבו משוב קצר לפני השליחה.');
      return;
    }

    let reviews = [];
    try {
      reviews = JSON.parse(localStorage.getItem('reviews')) || [];
    } catch (e) {
      reviews = [];
    }

    reviews.unshift({
      name,
      rating: selectedRating,
      text,
      createdAt: new Date().toISOString()
    });

    localStorage.setItem('reviews', JSON.stringify(reviews));

    // ניקוי טופס
    document.getElementById('reviewName').value = '';
    document.getElementById('feedback').value = '';
    selectedRating = 0;
    starEls.forEach(x => x.classList.remove('active'));

    loadReviews();
    alert('תודה! המשוב נשמר 👍');
  }

  // הגנה בסיסית נגד HTML בהדבקה
  function escapeHtml(str) {
    return String(str)
      .replaceAll('&', '&amp;')
      .replaceAll('<', '&lt;')
      .replaceAll('>', '&gt;')
      .replaceAll('"', '&quot;')
      .replaceAll("'", '&#039;');
  }

  // טעינה ראשונית
  loadReviews();
</script>

</body>
</html>

