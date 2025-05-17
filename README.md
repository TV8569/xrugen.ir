<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>X-rugen - صفحه اصلی</title>
  <link href="https://fonts.googleapis.com/css2?family=Vazirmatn:wght@400;700&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      font-family: 'Vazirmatn', sans-serif;
      background: #0a0f1a;
      color: #f0f0f0;
      overflow-x: hidden;
    }

    ::-webkit-scrollbar {
      width: 0;
      background: transparent;
    }

    .topbar {
      display: flex;
      align-items: center;
      justify-content: space-between;
      background-color: #001a33;
      padding: 10px 20px;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.3);
      position: sticky;
      top: 0;
      z-index: 1000;
    }

    .topbar .logo {
      display: flex;
      align-items: center;
      gap: 10px;
    }

    .topbar img {
      width: 40px;
      height: 40px;
      border-radius: 8px;
    }

    .topbar .name {
      font-size: 1.4em;
      font-weight: bold;
      color: #33aaff;
    }

    .topbar .nav {
      display: flex;
      gap: 40px;
      justify-content: center;
      flex: 1;
      font-size: 1.3em;
    }

    .topbar .nav a {
      color: #f0f0f0;
      text-decoration: none;
      position: relative;
      padding-bottom: 5px;
      transition: color 0.3s;
    }

    .topbar .nav a:hover {
      color: #33aaff;
    }

    .main {
      text-align: center;
      padding: 50px 20px 100px;
      animation: fadeIn 1s ease-in-out;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .main h1 {
      font-size: 2.8em;
      color: #3399ff;
      text-shadow: 0 0 15px #3399ff99;
      margin-bottom: 20px;
    }

    .main p {
      font-size: 1.2em;
      color: #ccc;
      line-height: 2em;
      max-width: 800px;
      margin: 0 auto;
    }

    .start-dates {
      margin-top: 40px;
      text-align: center;
      animation: fadeIn 1.5s ease-in-out;
    }

    .start-dates ul {
      list-style: none;
      padding: 0;
      line-height: 2.2em;
      font-size: 1.2em;
    }

    .start-dates li span {
      color: #33aaff;
      font-weight: bold;
    }

    .copy-box {
      position: fixed;
      bottom: 20px;
      background: #001a33;
      color: #fff;
      padding: 12px 18px;
      border-radius: 12px;
      font-weight: bold;
      cursor: pointer;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.5);
      user-select: none;
      transition: background 0.3s;
      display: flex;
      align-items: center;
      gap: 10px;
    }

    .copy-box:hover {
      background: #002a55;
    }

    .copy-right {
      right: 20px;
    }

    .copy-left {
      left: 20px;
    }

    .copied-msg {
      position: fixed;
      bottom: 60px;
      right: 50%;
      transform: translateX(50%);
      background: #33cc77;
      color: white;
      padding: 8px 16px;
      border-radius: 10px;
      display: none;
      animation: fadeOut 2s forwards;
    }

    @keyframes fadeOut {
      0% { opacity: 1; }
      90% { opacity: 1; }
      100% { opacity: 0; transform: translateY(-10px); }
    }

    @media (max-width: 600px) {
      .topbar {
        flex-direction: column;
        align-items: flex-start;
        gap: 10px;
      }

      .topbar .nav {
        justify-content: center;
        flex-wrap: wrap;
        gap: 20px;
      }

      .copy-box {
        font-size: 0.9em;
        padding: 10px 14px;
      }
    }
  </style>
</head>
<body>
  <div class="topbar">
    <div class="logo">
      <img src="https://s5.uupload.ir/files/amirabbas8585/Xrugen/logo2.png" alt="X-rugen logo" />
      <div class="name">X-rugen</div>
    </div>
    <div class="nav">
      <a href="#">🏪 فروشگاه</a>
      <a href="https://www.xrugen.ir/punish/" target="_blank">⚖️ لیست مجازات‌ها</a>
    </div>
  </div>

  <div class="main">
    <h1>سرور Xrugen در حال توسعه است!</h1>
    <p>
      ما در حال آماده‌سازی یک تجربه‌ی بی‌نظیر و حرفه‌ای در دنیای ماینکرافت هستیم! با گیم‌مودهای متنوع، سیستم‌های سفارشی و پشتیبانی قدرتمند،
      قراره Xrugen یک سرور متفاوت باشه که هیچ‌جای دیگه نمی‌بینی!
    </p>

    <div class="start-dates">
      <ul>
        <li>📅 تاریخ شروع رسمی سرور: <span>1404/04/01</span></li>
        <li>🧱 گیم‌مود SMP Custom → <span>1404/04/01</span></li>
        <li>🛏️ BedWars → <span>1404/04/05</span></li>
        <li>☁️ SkyMine → <span>1404/04/10</span></li>
      </ul>
    </div>
  </div>

  <div class="copy-box copy-right" onclick="copyToClipboard('MC.Xrugen.IR', this)">
    🌐 IP سرور: MC.Xrugen.IR
  </div>

  <div class="copy-box copy-left" onclick="copyToClipboard('https://discord.gg/AJBF5CPmYx', this)">
    💬 دیسکورد: کلیک برای کپی
  </div>

  <div id="copied" class="copied-msg">کپی شد!</div>

  <script>
    function copyToClipboard(text, element) {
      navigator.clipboard.writeText(text).then(() => {
        const msg = document.getElementById("copied");
        msg.style.display = "block";
        setTimeout(() => { msg.style.display = "none"; }, 2000);
      });
    }
  </script>
</body>
</html>
