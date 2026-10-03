
<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<title>آزمون شیطان کش</title>
<link href="https://fonts.googleapis.com/css2?family=Vazirmatn:wght@400;500;700;900&display=swap" rel="stylesheet">
<style>
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    -webkit-tap-highlight-color: transparent;
  }

  html, body {
    height: 100%;
    overflow: hidden;
  }

  body {
    font-family: 'Vazirmatn', Tahoma, sans-serif;
    background: linear-gradient(135deg, #0a0505 0%, #1a0505 50%, #2a0808 100%);
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 10px;
    padding-top: 120px;
    color: #fff;
    position: relative;
  }

  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image:
      radial-gradient(circle at 15% 20%, rgba(255,60,60,0.18) 0%, transparent 40%),
      radial-gradient(circle at 85% 80%, rgba(255,140,40,0.12) 0%, transparent 40%),
      radial-gradient(circle at 50% 50%, rgba(80,150,255,0.06) 0%, transparent 60%);
    pointer-events: none;
    z-index: 0;
  }

  /* ===== SOCIAL ICONS BAR ===== */
  .social-bar {
    position: fixed;
    top: 12px;
    left: 50%;
    transform: translateX(-50%);
    z-index: 1000;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    gap: 20px;
    background: rgba(255, 255, 255, 0.92);
    backdrop-filter: blur(12px);
    -webkit-backdrop-filter: blur(12px);
    padding: 10px 24px;
    border-radius: 50px;
    box-shadow: 0 4px 20px rgba(0, 0, 0, 0.3);
    border: 1px solid rgba(255, 255, 255, 0.3);
    min-width: 200px;
    max-width: 94vw;
    width: auto;
    white-space: nowrap;
    flex-wrap: nowrap;
  }

  .social-bar .social-link {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    transition: transform 0.2s ease;
    text-decoration: none;
    flex-shrink: 0;
  }

  .social-bar .social-link:hover {
    transform: scale(1.08);
  }

  .social-bar .social-link img {
    width: 50px;
    height: 50px;
    border-radius: 50%;
    object-fit: cover;
    display: block;
    background: transparent;
    padding: 0;
    border: none;
    flex-shrink: 0;
  }

  .app {
    width: 100%;
    max-width: 480px;
    height: calc(100vh - 140px);
    max-height: calc(100vh - 140px);
    display: flex;
    flex-direction: column;
    background: #120808;
    border-radius: 12px;
    overflow: hidden;
    box-shadow: 0 20px 60px rgba(0,0,0,0.7), 0 0 40px rgba(255,50,50,0.15);
    position: relative;
    z-index: 1;
    border: 3px solid #5a0a0a;
  }

  /* ===== هدر ===== */
  .header {
    background: linear-gradient(135deg, #1a0505 0%, #4a0808 50%, #8a0a0a 100%);
    color: #fff;
    padding: 10px 16px 10px;
    flex-shrink: 0;
    border-bottom: 2px solid #ff3030;
    position: relative;
    box-shadow: 0 4px 20px rgba(255,50,50,0.3);
  }

  .header::after {
    content: '';
    position: absolute;
    bottom: -2px;
    left: 0;
    right: 0;
    height: 2px;
    background: linear-gradient(90deg, transparent, #ff3030, #ffa500, #ff3030, transparent);
    animation: glow 2s ease-in-out infinite;
  }

  @keyframes glow {
    0%, 100% { opacity: 0.5; }
    50% { opacity: 1; }
  }

  .header-top {
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-size: 13px;
    margin-bottom: 6px;
    opacity: 0.95;
  }

  .header-top .title {
    font-weight: 900;
    font-size: 16px;
    text-shadow: 0 0 12px rgba(255,80,80,0.9), 0 0 4px rgba(255,200,100,0.6);
    letter-spacing: 0.5px;
  }

  .score-badge {
    background: linear-gradient(135deg, rgba(255,50,50,0.4), rgba(255,150,50,0.3));
    padding: 3px 12px;
    border-radius: 20px;
    font-weight: 700;
    font-size: 12px;
    text-shadow: 0 0 8px rgba(255,80,80,0.8);
    border: 1px solid rgba(255,80,80,0.6);
  }

  .level-bar {
    display: flex;
    align-items: center;
    justify-content: space-between;
    background: rgba(255,80,80,0.12);
    padding: 6px 12px;
    border-radius: 8px;
    margin-bottom: 7px;
    font-size: 12px;
    font-weight: 700;
    border: 1px solid rgba(255,80,80,0.3);
  }

  .level-bar .level-label {
    display: flex;
    align-items: center;
    gap: 5px;
    text-shadow: 0 0 8px rgba(255,80,80,0.5);
  }

  .level-bar .level-value {
    background: linear-gradient(135deg, #8a0a0a, #ff3030);
    color: #fff;
    padding: 3px 12px;
    border-radius: 6px;
    font-weight: 900;
    font-size: 12px;
    border: 1px solid #ff6060;
    text-shadow: 0 0 6px rgba(255,255,255,0.5);
    box-shadow: 0 0 12px rgba(255,50,50,0.6);
  }

  .progress-bar {
    height: 7px;
    background: rgba(0,0,0,0.6);
    border-radius: 4px;
    overflow: hidden;
    border: 1px solid rgba(255,80,80,0.4);
  }

  .progress-fill {
    height: 100%;
    background: linear-gradient(90deg, #8a0a0a, #ff3030, #ffa500, #ffd700);
    border-radius: 4px;
    transition: width 0.4s ease;
    width: 0%;
    box-shadow: 0 0 12px rgba(255,100,50,0.9);
  }

  /* ===== بدنه ===== */
  .content {
    flex: 1;
    overflow-y: auto;
    padding: 14px 16px;
    display: flex;
    flex-direction: column;
    -webkit-overflow-scrolling: touch;
    background: #0a0505;
    background-image:
      radial-gradient(circle at 10% 10%, rgba(255,50,50,0.06) 0%, transparent 40%),
      radial-gradient(circle at 90% 90%, rgba(80,150,255,0.05) 0%, transparent 40%);
  }

  .question-card {
    background: linear-gradient(135deg, #1a0808 0%, #250a0a 100%);
    border-radius: 10px;
    padding: 16px 14px;
    border: 2px solid #8a0a0a;
    animation: popIn 0.35s ease;
    display: flex;
    flex-direction: column;
    box-shadow: 0 0 25px rgba(255,50,50,0.15), inset 0 0 30px rgba(0,0,0,0.6);
  }

  @keyframes popIn {
    from { opacity: 0; transform: scale(0.92); }
    to { opacity: 1; transform: scale(1); }
  }

  .q-label {
    display: inline-block;
    background: linear-gradient(135deg, #8a0a0a, #ff3030);
    color: #fff;
    font-size: 11px;
    font-weight: 900;
    padding: 4px 14px;
    border-radius: 4px;
    margin-bottom: 12px;
    align-self: flex-start;
    text-shadow: 0 0 5px rgba(0,0,0,0.6);
    border: 1px solid #ff6060;
    box-shadow: 0 0 12px rgba(255,50,50,0.5);
  }

  .question-text {
    font-size: 15px;
    font-weight: 700;
    color: #ffd5d5;
    line-height: 2;
    margin-bottom: 14px;
    text-align: right;
    direction: rtl;
  }

  /* ===== خط اعداد LTR ===== */
  .numbers-line {
    display: block;
    direction: ltr;
    text-align: center;
    font-family: 'Consolas', 'Monaco', monospace;
    font-size: 18px;
    font-weight: 900;
    color: #ffd700;
    background: rgba(255,80,80,0.08);
    padding: 10px 12px;
    border-radius: 6px;
    margin: 10px 0;
    border: 1px solid rgba(255,100,50,0.35);
    letter-spacing: 3px;
    text-shadow: 0 0 12px rgba(255,215,0,0.7);
    white-space: nowrap;
    overflow-x: auto;
  }

  /* ===== پاسخ کوتاه ===== */
  .short-answer-box {
    display: flex;
    gap: 8px;
    margin-bottom: 12px;
  }

  .short-input {
    flex: 1;
    padding: 12px 14px;
    border: 2px solid #8a0a0a;
    border-radius: 8px;
    font-family: 'Vazirmatn', Tahoma, sans-serif;
    font-size: 18px;
    font-weight: 900;
    color: #ffd700;
    direction: ltr;
    text-align: center;
    background: #1a0808;
    outline: none;
    transition: all 0.2s;
  }

  .short-input::placeholder { color: #884444; }

  .short-input:focus {
    border-color: #ff3030;
    box-shadow: 0 0 20px rgba(255,50,50,0.5);
  }

  .short-input.correct {
    border-color: #4ade80;
    background: #0a2010;
    color: #4ade80;
    box-shadow: 0 0 20px rgba(74,222,128,0.5);
  }

  .short-input.wrong {
    border-color: #ff3030;
    background: #2a0808;
    color: #ff6060;
    box-shadow: 0 0 20px rgba(255,50,50,0.5);
  }

  .submit-btn {
    padding: 12px 18px;
    border: 2px solid #ff6060;
    border-radius: 8px;
    font-family: 'Vazirmatn', Tahoma, sans-serif;
    font-size: 15px;
    font-weight: 900;
    cursor: pointer;
    color: #fff;
    background: linear-gradient(135deg, #8a0a0a 0%, #ff3030 100%);
    box-shadow: 0 0 15px rgba(255,50,50,0.5);
    transition: all 0.15s;
    white-space: nowrap;
    text-shadow: 0 0 5px rgba(0,0,0,0.6);
  }

  .submit-btn:active { transform: scale(0.96); }
  .submit-btn:disabled { opacity: 0.5; cursor: not-allowed; }

  /* ===== بازخورد ===== */
  .feedback {
    padding: 10px 14px;
    border-radius: 8px;
    font-size: 13px;
    font-weight: 700;
    display: none;
    justify-content: center;
    align-items: center;
    gap: 6px;
    animation: slideUp 0.3s ease;
    margin-top: 8px;
    border: 2px solid;
  }

  .feedback.show { display: flex; }

  .feedback.ok {
    background: rgba(74,222,128,0.1);
    color: #4ade80;
    border-color: #4ade80;
    box-shadow: 0 0 15px rgba(74,222,128,0.3);
  }

  .feedback.no {
    background: rgba(255,50,50,0.1);
    color: #ff6060;
    border-color: #ff3030;
    box-shadow: 0 0 15px rgba(255,50,50,0.3);
  }

  @keyframes slideUp {
    from { opacity: 0; transform: translateY(8px); }
    to { opacity: 1; transform: translateY(0); }
  }

  /* ===== راهنما ===== */
  .explain-box {
    margin-top: 10px;
    padding: 12px 14px;
    background: linear-gradient(135deg, rgba(255,165,0,0.08), rgba(255,80,80,0.06));
    border: 2px solid rgba(255,165,0,0.4);
    border-radius: 10px;
    display: none;
    animation: slideUp 0.4s ease;
    box-shadow: 0 0 20px rgba(255,165,0,0.15);
  }

  .explain-box.show { display: block; }

  .explain-title {
    font-size: 13px;
    font-weight: 900;
    color: #ffa500;
    margin-bottom: 8px;
    display: flex;
    align-items: center;
    gap: 6px;
    text-shadow: 0 0 10px rgba(255,165,0,0.5);
  }

  .explain-step { margin-bottom: 8px; }
  .explain-step:last-child { margin-bottom: 0; }

  .fa-line {
    font-size: 13px;
    color: #ffd5d5;
    font-weight: 600;
    line-height: 2;
    direction: rtl;
    text-align: right;
    margin-bottom: 4px;
  }

  .math-line {
    font-size: 15px;
    color: #ffd700;
    font-weight: 900;
    direction: ltr;
    text-align: left;
    background: rgba(255,80,80,0.1);
    padding: 8px 12px;
    border-radius: 6px;
    margin-bottom: 4px;
    display: block;
    border: 1px solid rgba(255,165,0,0.35);
    font-family: 'Consolas', 'Monaco', monospace;
    letter-spacing: 1px;
    overflow-x: auto;
    white-space: nowrap;
    text-shadow: 0 0 8px rgba(255,215,0,0.5);
  }

  .math-line .rtl-text {
    direction: rtl;
    unicode-bidi: embed;
    display: inline-block;
    font-family: 'Vazirmatn', Tahoma, sans-serif;
  }

  .explain-final {
    margin-top: 8px;
    padding-top: 8px;
    border-top: 1.5px dashed rgba(255,165,0,0.5);
    font-size: 13px;
    font-weight: 900;
    color: #ffa500;
    direction: rtl;
    text-align: right;
    display: flex;
    align-items: center;
    justify-content: flex-start;
    gap: 6px;
    flex-wrap: wrap;
  }

  .explain-final .num {
    color: #4ade80;
    font-size: 16px;
    text-shadow: 0 0 8px rgba(74,222,128,0.6);
  }

  /* ===== گزینه‌ها ===== */
  .options-bar {
    flex-shrink: 0;
    padding: 10px 14px 14px;
    background: linear-gradient(180deg, #1a0808 0%, #120505 100%);
    border-top: 2px solid #8a0a0a;
  }

  .options-title {
    font-size: 11px;
    color: #ffa500;
    text-align: center;
    margin-bottom: 8px;
    font-weight: 700;
    text-shadow: 0 0 8px rgba(255,165,0,0.5);
  }

  .options {
    display: flex;
    gap: 8px;
    justify-content: center;
    flex-wrap: wrap;
  }

  .opt-btn {
    flex: 1;
    min-width: 70px;
    max-width: 105px;
    min-height: 60px;
    border: 2px solid #8a0a0a;
    background: linear-gradient(135deg, #1a0808, #220a0a);
    border-radius: 8px;
    font-family: 'Vazirmatn', Tahoma, sans-serif;
    font-size: 14px;
    font-weight: 900;
    color: #ffd5d5;
    cursor: pointer;
    transition: all 0.15s ease;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 8px 6px;
    user-select: none;
    text-align: center;
    line-height: 1.5;
    direction: ltr;
    unicode-bidi: embed;
    box-shadow: 0 0 10px rgba(255,50,50,0.15);
  }

  .opt-btn:active { transform: scale(0.95); }
  .opt-btn:hover {
    border-color: #ff3030;
    background: linear-gradient(135deg, #2a0808, #3a0a0a);
    box-shadow: 0 0 15px rgba(255,50,50,0.4);
  }

  .opt-btn.correct {
    background: linear-gradient(135deg, #0a2a10, #1a4a20);
    border-color: #4ade80;
    color: #4ade80;
    animation: pulse 0.4s;
    box-shadow: 0 0 20px rgba(74,222,128,0.6);
    text-shadow: 0 0 8px rgba(74,222,128,0.6);
  }

  .opt-btn.wrong {
    background: linear-gradient(135deg, #2a0808, #4a0a0a);
    border-color: #ff3030;
    color: #ff6060;
    animation: shake 0.4s;
    box-shadow: 0 0 20px rgba(255,50,50,0.6);
    text-shadow: 0 0 8px rgba(255,80,80,0.6);
  }

  .opt-btn.long-text {
    font-size: 12px;
    line-height: 1.6;
    direction: rtl;
    unicode-bidi: normal;
    text-align: right;
    justify-content: flex-start;
    padding: 8px 10px;
    max-width: none;
    flex-basis: 100%;
    min-height: auto;
  }

  @keyframes pulse {
    0% { transform: scale(1); }
    50% { transform: scale(1.08); }
    100% { transform: scale(1); }
  }

  @keyframes shake {
    0%, 100% { transform: translateX(0); }
    25% { transform: translateX(-5px); }
    75% { transform: translateX(5px); }
  }

  .opt-btn:disabled { cursor: not-allowed; opacity: 0.5; }
  .opt-btn:disabled:hover { border-color: #8a0a0a; background: linear-gradient(135deg, #1a0808, #220a0a); }

  /* ===== صفحه نتیجه ===== */
  .result {
    display: none;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
    padding: 24px;
    height: 100%;
    animation: fadeIn 0.4s ease;
  }

  .result.show { display: flex; }

  @keyframes fadeIn {
    from { opacity: 0; transform: scale(0.95); }
    to { opacity: 1; transform: scale(1); }
  }

  .result .emoji {
    font-size: 80px;
    margin-bottom: 10px;
    animation: bounce 1.2s ease infinite;
    filter: drop-shadow(0 0 20px rgba(255,100,50,0.8));
  }

  @keyframes bounce {
    0%, 100% { transform: translateY(0); }
    50% { transform: translateY(-12px); }
  }

  .result h2 {
    font-size: 22px;
    color: #ffd5d5;
    margin-bottom: 4px;
  }

  .result .level-title {
    font-size: 26px;
    font-weight: 900;
    background: linear-gradient(135deg, #ff3030, #ffa500, #ffd700);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    margin: 8px 0;
    line-height: 1.4;
    filter: drop-shadow(0 0 10px rgba(255,100,50,0.5));
  }

  .result .score-big {
    font-size: 48px;
    font-weight: 900;
    color: #ffd700;
    margin: 4px 0;
    text-shadow: 0 0 20px rgba(255,215,0,0.6);
  }

  .result .score-text {
    font-size: 13px;
    color: #ffa500;
    margin-bottom: 18px;
    font-weight: 600;
    text-shadow: 0 0 8px rgba(255,165,0,0.4);
  }

  .result-stats {
    display: flex;
    gap: 12px;
    margin-bottom: 22px;
    width: 100%;
    justify-content: center;
  }

  .stat-box {
    flex: 1;
    max-width: 115px;
    background: linear-gradient(135deg, #1a0808, #220a0a);
    border-radius: 8px;
    padding: 12px 8px;
    border: 2px solid #8a0a0a;
    box-shadow: 0 0 15px rgba(255,50,50,0.2);
  }

  .stat-box .num { font-size: 26px; font-weight: 900; display: block; }
  .stat-box .lbl { font-size: 11px; color: #ffa500; margin-top: 2px; font-weight: 700; }
  .stat-box.green .num { color: #4ade80; text-shadow: 0 0 10px rgba(74,222,128,0.5); }
  .stat-box.red .num { color: #ff6060; text-shadow: 0 0 10px rgba(255,80,80,0.5); }

  .btn {
    width: 100%;
    max-width: 250px;
    padding: 13px;
    border: 2px solid #ff6060;
    border-radius: 8px;
    font-family: 'Vazirmatn', Tahoma, sans-serif;
    font-size: 15px;
    font-weight: 900;
    cursor: pointer;
    transition: all 0.15s;
    color: #fff;
    background: linear-gradient(135deg, #8a0a0a 0%, #ff3030 100%);
    box-shadow: 0 0 25px rgba(255,50,50,0.5);
    text-shadow: 0 0 5px rgba(0,0,0,0.6);
  }

  .btn:active { transform: scale(0.97); }

  .next-btn {
    width: 100%;
    margin-top: 10px;
    padding: 12px;
    border: 2px solid #ffa500;
    border-radius: 8px;
    font-family: 'Vazirmatn', Tahoma, sans-serif;
    font-size: 15px;
    font-weight: 900;
    cursor: pointer;
    transition: all 0.15s;
    color: #fff;
    background: linear-gradient(135deg, #8a0a0a 0%, #ffa500 100%);
    box-shadow: 0 0 20px rgba(255,165,0,0.5);
    display: none;
    animation: slideUp 0.3s ease;
    text-shadow: 0 0 5px rgba(0,0,0,0.6);
  }

  .next-btn.show { display: block; }
  .next-btn:active { transform: scale(0.97); }

  .content::-webkit-scrollbar { width: 6px; }
  .content::-webkit-scrollbar-thumb { background: #8a0a0a; border-radius: 4px; }
  .content::-webkit-scrollbar-track { background: #0a0505; }

  @media (max-height: 700px) {
    body { padding-top: 100px; }
    .app { height: calc(100vh - 120px); max-height: calc(100vh - 120px); }
    .social-bar { padding: 8px 16px; gap: 16px; }
    .social-bar .social-link img { width: 44px; height: 44px; }
    .question-text { font-size: 14px; }
    .opt-btn { min-height: 52px; font-size: 13px; }
    .question-card { padding: 12px 12px; }
    .content { padding: 10px 12px; }
    .options-bar { padding: 8px 12px 10px; }
    .fa-line { font-size: 12px; }
    .math-line { font-size: 13px; padding: 6px 10px; }
    .result .level-title { font-size: 20px; }
    .short-input { font-size: 16px; padding: 10px 12px; }
  }

  @media (max-height: 640px) {
    body { padding-top: 90px; }
    .app { height: calc(100vh - 105px); max-height: calc(100vh - 105px); }
    .social-bar { padding: 6px 12px; gap: 12px; border-radius: 35px; }
    .social-bar .social-link img { width: 38px; height: 38px; }
  }

  @media (max-width: 380px) {
    body { padding-top: 85px; }
    .app { height: calc(100vh - 100px); max-height: calc(100vh - 100px); }
    .social-bar { padding: 5px 10px; gap: 10px; border-radius: 30px; }
    .social-bar .social-link img { width: 32px; height: 32px; }
  }
</style>
</head>
<body>

  <!-- ===== SOCIAL ICONS BAR ===== -->
  <div class="social-bar">
    <a href="https://eitaa.com/riazzuu" target="_blank" class="social-link" title="ایتا">
      <img src="data:image/png;base64,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" alt="ایتا">
    </a>
    <a href="https://www.shad.ir/t/riazzuu" target="_blank" class="social-link" title="ریاضو">
      <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAGQAAABkCAYAAABw4pVUAAAcJ0lEQVR4nO2deZBdV33nP+fc5W29762lpbaMtVgYA/Ju44WxSQCbCeAwxKHIFEySmUwyS4pK8k8omEzVJDVFZcZMIFQCw5hhZ0zMkuAVhBdky7ZsybJk7WvLvW9vu8s5U+fc+1qP7lZLuCy5Hb2vqqtb771+75zf9/z23+1LAw000MCbB6K2Uq31a1m0BK4CbgW2AJcBK4ECkFnw6n9eqAJF4ATwCrAdeAx4BlC/6k6FSKh4rYSsAv4AuAdYveDZixvHgP8L/C/g+PkmpBP4LPBJwF/wbAP1CIC/A/4cGDsfhPxmynrXgmcaWAqjwL8HvrXEa+YIkQueWQgX+EL6hg0yfnUYmX0zlaF7tt8+m4bkUyLev+CZBl4Lfgh8BCgtIOIcTJZh83vAXQ3Rv654APgQENW/6bmYrM83yDgvuCuV7aI4k4Z8JLV7DZw//Bbwjdq7L2WyTGi7p+HAzzvGgQ3ACGcxWX/RIOOCoAP4L/M/aL6GDAD7Ae+f2+6XKULgUuDomTTk3zbIuKDwUpnPoV5DDDlH0jpVAxcOpt61RghhC5L1GnJVg4w3BKtS2VvUE3LbxbH/ZYlba4uqJ+SdF7tU3kBsqX10PSHrLyYJLDPMyb6ekP6LXSpvIOZkX09I88UkgWWGOdnXh70Lyr0NXDiINDNcrHTSwBuIBiHLDA1ClhkahCwzNAhZZmgQssxw1rGU5Q1t/yk0jlb2fCkcZPIjsdBINAyNo0pV4u5WREsT3lyAr9PAXyybXb65CdHCiNQO0jqme6AUOBIlQJeqVA4OEe/YT/GplwiFpvnOG2i542or/4RKQUyMi7NsKHlzEyK0JcTqgTb8CKT5LjXh1BSzX3uI0oPPUj50ErpayK0bQN5xNZEwCmRY0ZaI5aMfb3qTZYSpieIKByaHODh5irf1XEJvvg2RcdFDY1QOnkSXq3jlCDU2jQoCdMYzqTFCa1xDxzJi5E3t1KthwJGxY/zjvse495mv8FcPfZ4nTjzDbFTC7WhDXrke0dOO8Dx0EBO/OomeKOIqbTduNEots4rRm1pDpqtFHj34NP9929/zysTLyImAKwY3ctPAdbRpie5sQeQzGPcSByHx2DR6sojobrOmLjImjuVltt7UGiIcQYkKe0cP4voK3eyzc+JVYmUELMgaTTAa4EpwHeIwIgpCa66M9zHPuUI2fMjrha5sG1f2XUFn9yXo4QO4scfIzDRBHKNMRCskLpIoMAyFuFrgSmk1xoTGhhBtXMgyOpZv8ihLcGnHSv7q5t9jsjJGFEJz8wAduWYTByMoE+kQ5Qg8x0X4DqEDgVBkhUTGmlguLyEsuhalkkvkpEyOTq1VIkTqAHUMwiMGYpuWKaT9Z38bY5mFPXoRSkU4wk/NRIzAtVY7yQIUNmkw/5OaWDvWpjsqPbJOBMrF5Hy2WyA0oUh+xSExS12FLj52+V2EZs3SwTdX/nlVRKyJRA4hXRvixkqgIoFvP0PaFBIp7fucHdqGyIkQ5qmTTi8nTLaR5EIi2Y+ysvETeUR2eWd1VgsIMWSYXon5Ok1E7edkMSaOx+ZgESI0YknFI9IFp8IzYnOkQCnHLtySYYiSUUpfSrh5M2vPdTKl7/gJ6eZLBiCzhFoiRYRrHosdhHDtpqWObfjqOII0uyCwA4EuMZK4FkSle7D7MwfA5CBap0yfHeYQJEfNrhatFI6UyWN23THKRG1GE0k+1FPJ43af50DGooTUyKgnZu4w6GQjjhG6NKe3hCTP0VfGOPTSECcOjlCZCWjtbGH1ZStZu7GDnjVN9mTEWiZcaYUypGhhT3j9qdPmOaNRjouyj/k4sU58gUiWW5qKmTg6xamD0wwdHWdibMIKxWpsNSbnw62fvJyevgwyriBUaAVh9zE3YZ7u61wjXm0SzuTAWRKlQEuZPGbeT6VJqTma5mdDiUxIDIQgYy8F0fZAno2VRQmxp6eOjHpNYa5UoTi0fZbHf7SDl7YfZvjEBNVSjFAu0tX4LdvoHWzl8mvWc9c9V1HojkDn7LLMkJ49pebUmfKHiXSM4miBIzKpMRO4GpQlMWDy5CwvPXWCZ7ce4vj+cWZHQyoTZdBBUipBUpkNyeXg7e97C93d0iZ9UiRaUjtMYp5GnJOSpNxZDrW265wzuyL5GZHW0IwJk5YhjIOSnkiMxVzdbGksIKR+0afb7CJdTLq6ULHrFyf5+uce5/iuMUQcWZqctDokIklU1RwaHeXQzjLH9w3ziT+5gfaVGWtItfmyF6kKRGpYjSlT1gw4NRmACBDa46Wnh/npt19gzxNHKI6X7Wu10olVE+YAmNdHVhukzBFL1757bEyf49mFJ6bq9B4TYcpztVh2QWqOlTj5LlLjZDUnEZASmsjWb0yknXhXnQ6JCnn2qsACQlh48c4cGcqsKNaM7B7jq3/5KAd3jNOU9XE8j0pYTcyZ+WiVOO+cVyAoK7Z+/2XyOcm//tRt5LsKaMc4fQcR17RQJGQbU2BcoQpxpGc1cdfWQ9z/xW0cenYEXQ7wPZcw1lRMSOWBk3HIZQpIXcUxn59xrcmWUhERoVLhSfNlzEzq4+YChXOB3bzRVmE/wwjdBDgiNo85qQbE9nPNsTTakRxO4/O0tch2dFq8JpNVI4U6TUk3YALJUsCD33yJnU8eYaCnj0gFtpK6cmMXK9Z2ks1kKU2WOX5gjJHjszTlze9m+aev7+BtW9Zy1fs34Hsex/aPMbR/jLAU4bqSzhUtrH1rP15WWIOlQ83B58f59r0/Y/8zwxS8Ak42Q1ANyLZnWTnYQ/uKAm6sObpznMmTAa6bsVGOp5V1/kZjtDkcNteoBRDa2vr5pmspJCZUI4oVgkd3MDs1aR/NZHP412/G6e1AS8G+omLnZEg1VGSkpCsbcWtPTcTnVg9YQMhi0KkNjOOIo4dP8vADO+hsLeAITTEss/nmS7jxAxsZvLwPP+MzO1Fhz7PH+On9Ozm66wTdLV1MHivyk+/u4NItA3QXmtj5xGG23r+L2eEynid467vW0jPQRUs2A9ph7GSR7//1M7z0xCE6WrvQUUQkYvo3tHHFzevYcN0AXf1NTByf4puHt1IqV8kVHKux+YyX+qOsjcZqpyyMQoIgIKOVUUbS7HGRHf8yrDUyB3y6yNQXHmDkyDErj6auTrpXduH0daCEw5MjMV/YW6FSUXiux6bemHf15BOPaN5Av4awdw6aOadFqqKlySo7Ht/P6JER1q3r49RQkbdct4I7P3kNl13Vj5dJ+grda/L0DBbINXl89S+nmB4rsbKvnd3bjnFi/6u0rcwyearCsd1jTA8VcTxBx6o2oqqypqxSDnn24T08ev9O+lY3IZWmGle44l1reNeHNrPxmkFaOgooFVMsFimWykgnw0y5RP9gH7kmH1wfp9CM42eJhLTmNJqaITg1SkavsZGdDUh1InDqZDXnObVO/acxWTHxzCwzz+8hmJqFQFONEl9mTFKsNYeLMc9OKAgkjohxmxSRMNoaIW0utkDKC7CgaKB1LaJIg1Kd9ORiHVOdjjj81CwyziC1SyWqcP2vb2TFhi5kxkv7Ekk+kG/Ncfm1a9ly+3ompsfwsxCOS04cHCKoBOQLPs1NGdraM3T0NtPUkUc4MaoaM3J0hge/ug0vI/CzWSYmS2y+bh0f/sNb2PLe9RQ6M/awlGYCju0dZeLoJM2ZHOVSlb7VrXiZJDpzB1pwuppsOmpsrjw5SvTsXpuhGxMcyyR8UjYvSV2F1paoJCpLDqVRJFWsUN2+l+rUFIXmbnKiQGbTGkRbwcpnsqKYNkU0XyMykMtErCp4OMRJ8+wcY+wFhFhPNffLSahIKmSz2GKlhCg4lGZjWnokK9ZlaWpybBCoRIQWcarjkG/KctmmteDmKAcO0nWJqznTW0UI4/w84sgD5eMY0+LGlGYq7HjiJC+/MEbfmhYmpyK6B3P8y9+9lsFNPUksb0NZxbF9Uzx5/0GmixoKgjCo0nZlFzKfwY0jMpvX4m8YgIxnhR5PzFLa/grByRFLkAlATOkkTvNYoxGhrSektkXYmBFlcqEj44x/5REC6SFFnkgUyVy6AtmUtUweKWmOT0WIIEZKQUHD2oy0dQkTCdq87RxIWUBILdPQ6V8YsvmBqfsIBy0Uyg2IZYzIBoRRRHFGEAWJkTWJXa1gEAtFrGJK07PooILrxjhujDShqHCIbMIW4/qODXW1smeJUjli97YDhJUATzjMVk5x84fX072+FeWppDSjBDOjAbueOMLunx+mr72NuFhmZV8b1960AS8vbSRniPHXr8TpaEb5DkHeZeq5vbz6pR9AqWpNodmvb8oqaSLna4mvRVpp0Lixwh2dofyzlxnZ+hwtmU7KTEIhR/Mt7yTT1WXlc6AEh4qu9SXGhPV7WW5s96xcVCrT16YhKSX6l/Qkgec69K1uozypkD6URiW7nzzB5MikzT8860BdlNS2ljR+cpZtD79Ei+fhRmXiuETkThOYyqv1tSFhXCQKSzg6wvVdIkPy8CxtLRmKozP093dy3a+9nXxvs80vzGmsjJV4/Lsv8sMvbSXjhoQZxfh4mQ039LF2XTsZx4TOkkjFtL3nagpbLkOUqmRw8EJN+b7HKH35IUrVEo5KEjYnbViFUtvSkE38lCaeKjL94HOc/PP7yPtZZEuOeHKI9huvxN04AAUPUwjaPxFypGgKVq4tZzU3Ka7vEtZNOxr7mnMxWgsJ0Y59k9NJU1LzMSapqSPDte/aRHMhjxNn6Gpq5ecP7GTbT15h6tSU6QIhTXIXuQzvn+Wf7nuOPc8O0dnRixJ5ylFMW3s7OT+HazJy5dkv6UryBZf25hxRucrkyCy+U6A0m2X1wApyuYxNvGQkOLBtiC9/9lG+c+/jREVFvruTsZEZcn0+93zmQ/h52DFynIdP7mC0OgNre2i98waybx2kPDOLcCThTJGT//U+Sn/2f9DP7iOIQkLjYzRWO8y2wzCk/OJBhj/7NYb++G+hPAu9rUwO7UN5TXT9yd34q7psaP34SMATwyGTYWSjt4IU9HfH9GaTYMAmlfb6ztcS9qZOziZTzCWk1rllcg6XXNnLxhtaePmxV7lkcC2jpRLf+ZvtHN0zwVuvWUNzR57xoWm2P/QKzz1+lOaWAsqLCN0cTZ2t7Ht+lFzmMCf3TZjzip/J2hxh8tUyzz14mLHjUzZszDRJYr9MsdLGnqeGUNuPsO/5I7zw84OMnSyT95vI5JoZPTVLa17zu59+LytWF+xav35gK4/s+iH/7fZP8e6111N47ztpHR0j/Nx3cIYnbXtXz5QYvu9Bhh7dTtcdV9Ny+VrCrlaTShKNTFN9/gCVp3YTHTyFa0xaZ5ZweISsyND313+Mc8U6Aq+CEFl+MFRmu7EajjG9ZQbyDnf1t9iiq3YCmyy6amGheDEsvBzBEhLPVTYTRXPSSCQgrgpe/Nl+Pvvx75PHp6mjQEyA0i4y4yK8gLhSQZR9XKcJkS8h4gpRthVRqRo/jm8sT2ROvJcmwTHCi9G+wgldSqGgIMpUdYCXz6Ejn7BcJayGZN2s9WeVaoXZYoWu7iY++AfXc8NHN5Mr5Hhx5ggf+96n2Df0NB/f8m/4j1d9nA1dqwhfHWP62z9l6t5/IBgaxc3mCHMuBLHdZT6XMTY5qWQHEboUoKLY9lBMTqOmZnDyDv1/+jv4n7gDr63J+syvDIX8z51ldk8lVd+cU+F9Kx3ufXs3rVlsC8IU+W0esoSC1C5HWERDdFK+rNGpk8eSfMTFy2g2Xb+OT376X3D/559gYmSGbHOIJzxk6KUxvYvrx3hehVBJa36qQYVmV1KqBATVDNIzJERWO0yxUYUx4YzCjV1Ei4/WMRkKhJUSalYjIoEj85TKgqBcwvUjNl47wM13v42r7xjEa8twvDrKnz3yOQ5N7CXMtvGDfY+wrn0tzbn3saKnnba7b8ZpzTP5dz8mfOYAXkWiXZfAmLGiToqDpiZIUiLSsSKumikVh9w7LqX9Y79O/jeuJejIoUXAk6+6fHNPwL6iIM4IVKB5SyHPnQNZ2n1hgwSTHog4puoK2xlZgpMzmCy7JomY8+gyHbZJe50iJtsMt969mZZCga0/eJHDLx+nPGW6DxGZQoasqW9p00aNbM/AFKBLo2UCHaN1GVdX6pyctNGbXaiSCKWIyhXK2pBlIrXIOl7PdVFuiNMM667o5IrrBrny5ktZtambpjYfpUyJPOJ48SShOdnNHQwXS9z3wv+z5N+96Q4G+nvssJzb002wdRfFrc8RvnwEN0zWGitta1Bmx4FJrJsLFNatpnDDJvLvuQLvik2IzjwmiH58BP7HngrbJyQVqdFhRH9OcNsaj5t6fLSMbWHRUYrY9I2shpzdhyxusnQSujomOVTJy2yPyTr4MKnsxB5xSbD3xWMc2H2cmZGQ2VNVju07xfCJcbRy8T2HMIyZKc6yYrCf3pWtSBGkCZc8i5PTmOaC6fKZHKXQlKfZJJGr86zc0MHA+h7a+5sTjTR5iVJUVZHv7PkJf/rIlxgNp3FcD10tsblzDR/Z/H4+uP52Lm1bjQhjolMTVHbsR+05RPXEDHp8mkp5BiEiMtkCdLUjBvrIX7aK3KZVOGt7bKvAHJ0fDFX56t4qW8c0U66PCCsUVJUPrsnxRxuaeFurizQdUJsox5YUHGeup7oYaibrjITYxp4hIK33JF3VpOppKqexqXSmHj+olikOV9n7xAl+/g8vsm/nCYQ0WuIyNT1D55os9/znO+geaLXCs41Aqc56YHSa4ZrPy+YcmpqzNLVlcfNJt9BUXXV68rStTynCapVP/+I+vvL89xhTE6YcjBfCpYVe3nPJjbx/4y1c2X8ZrW7BJqhRtUI0Oo07WSaozFoBerkcTnsror0NJ+/Zg1GKHPZNBTw56XDfviI7piNC6dhcxmjwLb2C/3BZjtt7fBwTrgnHZh6mFO8nnWiWmm9ZkpDTNf7YZrRJIykRjIg8qy2mvjM1U6I8WWXsyBRHd43y8tPHOLxnhMp0iAo1xXKFlj6PD//hjdx+zzuIbDvNurikuHcW2HJ/MtFG8pcnNLWen9a1XoSYa8s6JnlVgqHSCJ956u95YPePGVFlhMwgqop2J8tVA5fza5fdxNW9G7ikfTVNJtggwDWNNZn03s1nmNpUKRZMhZqhSsjuKdh6sspD4x5DxRA3J+w0S3Ml4p0r8vz++gy39wqa/Chp3Ro5udIeGtcky6aXf2YFORshOh21THNM0wPQSUl85OAskyb7jmJGjo1zat8Eu546yrG944QVyOay9uSHUYX2gTx3/PY7eN8nrkEZ82NJNVqX2tOzkhKlgq+NUIj6BacVGqO1pvMh8E0b17y10uyZPsoXt32DH+17mBOlSWInn+wlrNCZb+L6lRu4bfU1bFn1Drb0DuJo3wpsb0kyXNTMBDHDARwqKV6cCHl6VDM8G+KYjN+XeJGiU2mu6nH5vY15bux2yDqRPTgm89exQ+wl1QvXyNKMuyzRDjkzIbUBfy3THnLS3DcwbdT7/+ZJdv10P3FVU5kKKM2WbeyeLRSQrk+lYuLukMErO7nz49dy3Z0bbRpssxqTJEnz3s5cFXlpVEhyaDctzYhkgCAta+i0u2EcnVQJcaaJZAYQTDnjWDDC11/4MQ/seIC944eZcjMoNwdqEhFM4Fbz3HD5u/nW+z9Dl9dqNfEv9le4/0CZ45WQaaMpoYOKMgipcbOmyBviB9DrCD4w4PLv1nusa/XSNEHh2Zazk1qVMNFm4eKY+t0SbvPMYW8KmRbYVNo2MO9Vmi7z3FN72fX0SXp6C+RzAq/gkXdaqAYxU+UJOvtdrr59Mzf95lW85W3dNsJQscQ3n2c1wyGSpgJqoqIldNieDb+2GBuJ1SYOU71I5nJtedtBxSHCM3GNl5o5zRqvm/901T28tXuQ/739uzx1bAcT0TRVRyD8NuI45EQ8nFRzpSDSsHtW8dKUQ6hdMKG5qePlPCRlZDWiR0re0t7Mv7rU5UOrFb1eskBTXzOfHlMbMFGISNkxpMCJwXHPafBkASG1knPtNKYVahsSmkJgR0sHeXecfK6Z6co0YWAGDSL6Bjp49y1Xc9sHN7NhSz/KT9JLZXISU8yJAzveE6t0TONcOmjCtcGDpS0pxyYmLD1qtthpru+wPsYnJMJPa1NRHNrozBcu7x28iSv7LuWh49v41guP8ov9z1ENxtAVTUvQaetbJjTOOJBzYhwvJoqkzUvcSONUAwoZ2LyihQ+tivnoWpc2YXxIovXSjZMSfyxxY4F2FUqYQmrWbiNjV3ZuWEBIojm1QYM49ScSx5qaqo1i4qBKXmRYu2mQwSt76d/YxOYb1tG3ttPOFBibLs3EhZmdErabgnaSv80vTdnbpOsiTUCXgDFBjltX6dS/3HqVOlmrqSAo18c3Q3Um5jeHx/VsT92MixpTsirTxe8M3sVd/e/mqeEXeWzoZ/zkxW0oM91oqgSuJDTGNlY4sUsXHitbQzZ2hVzd5rOluZlres3FPdVENirC9wK09E1IYMNcEznao2ZMsilupgbAVR6OrBovd9ZDuIgPWYjaU+VSmRNHXmVseJbunk46u9rIZJOpD9dPhZeIatG65fnDOfRG09eYfCXSEdU4oFQp227jmu5e2xaoasGxqQrTFUUh69Gadck5ioyJlKSLL5n3WTpNms+lbLj0q87o1Ot5mT+9aMJL05PWSuJ5Do7jpBMVtdGh2olfPgP+8/dTe6y2N1PV9b2kLGTMTqC09U0mKfbMlImdqlTpxMj5wxkJWQzzR0pFetXR/CGzxTa/HLFwPzWSZK3ZmVjUNHhIJHV+93NGQs4k1DPxlWxq/mMLXrbsMH8acy6UPD0bWJchn//Vn5GQuv/Xv3jusZpp0un1F6fVf3kSsdj46PzndTrQcfqa3hpkOjJ6/j3iWf8a0FLaUb/J099rz7FAY5YzRG0ctH7SpG4W+EJvZVFCzmSeTmOh034z/7mt+p2cvuJwXqnmAmFB6FA7GcwzVb+0gXm9yOR5Pc9sLQ/7dTZzZefPTHHSFLKEnPMhcwZ9bnL9zO/zemKBhsy/JmQp1BOXfNU2usQvXWDUH6b6w/ZLe64tum7MpsbD6QrzhcEZnXoDFxaNP/G3TNEgZJmhnpDgYhfGG4g52dcTMnMxSWCZYU729YQMXexSeQMxJ/t6QvZeTBJYZpiTfT0hz17sUnkDsb320fWEPHYxSWCZYU729Ylh45ZHbwzOeMsj88DXLiJBLBd8rb7mX68hpNpxoHGv9AsGk3+sM1pyptvmHU9vyt7AhcGXU5nPYb6GkN56dW/6vYHzh7H0Vkfm+5K3Xh1L75DfwPnFH9XIqMdihJDeKfpvFzzawOuFLwFfX+y9FjNZNRjH/p3GPdVfd5gb3N89v5i7lMmqwfzCR4F/XPBMA68VP0plesbK+lKEGJSADzTM1+sCI8PfSGV6RpxLg8pc5PD7KbOjC55t4GwwMvutVIbhWV77K3UMjaPfCHxxKZVrYA5BKisjs2+cq1iWcupLYVUaGv82sHKJ112MOJGWQz4/P+lbCnMDh6+RkBpkeuvp29KbG1+WktV0Edwo35if2VTor6Tti0eBZ875T//UYTkPpzfQQAMNLAbg/wPaHyAkxyN6GgAAAABJRU5ErkJggg==" alt="ریاضو">
    </a>
    <a href="https://www.aparat.com/Riazzuu" target="_blank" class="social-link" title="آپارات">
      <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAGQAAABkCAYAAABw4pVUAAAgAElEQVR4nO2dB7hdZZX3f+8up5/bc1uSm55QQtDQu6hY0IGBgKKMBUFU1Jl5nEdEvhksoOiIA+OIoDPDR0eKfiogIChNRIQASSCQxk2/ub2duuv3rHefc7kkgYTkJjhMFs/hnpyyz97velf/r7XZR/toH+2j/zmkqmcahuGunLQBHAacCBwKzAUmA2kgvs2n315UBvLAJmAl8AzwMPA0ELzZK1UqYsWuMmQK8EXgbGDqNu/+76YNwC3A1cDGPc2QRuDbwHlAbJt399F4coD/Ai4B+vcEQz5S4XrTNu/sozeiPuBLwO1v8JkxhhjbvLMtWcA1lQPuY8abJ1mzn1fW0NrRt3ckIakKIz68zTv7aFfoHuCjQGEbRuyEyhJu/gI4Zd/STyj9BlgEeOMPujMq68d7mxlBEGz3+duMTqms7Xbp9STkoxW9t8epuvCGse3ekPe29/rbhD4O3Fa9lDdSWeLavvxWGfDqeVRP8G1MA8B+QC87UFmX7U1mVBkg0iAPOTF5VP/9NqYG4NKtL29rCekAVgP23mTI1tKwvdfepuQCs4H1rychX9ibzKAiquMlYbwte5tLCJW1/sL4F8ZLiDBnXSVPtddovDSMf+77PqZp7s1TeatI8l3TlFJ6942PHA/b28yokuM4PPXUUzzyyCNs2bKFeDzOggULePe7301HR8c2n3+b0ZTK2j/FVgx59564zuquf82OD0LRVfT29PDDK6/i9w/cz6rlL1NyipSNitwGMKetg455+zGrYzpHHHIos2fPZMa8OUyd2UEYHRwlKq6q5kS6VPT9gJAQhUeIiUJhjOln/U4oDkSol2C8e73d893zdGKVIeMX7q5wD5HneWMHDoIgDIMwvOc3d4ctk5plzcJ0PBFOnTo1nLnf3HBKx9Rw/qy5YVO6JkSZ+n3LVOH0aVPDj37sI+Ev7/lVmHNKoVc5ru/rw+l/lyuPsV+TN3wvDN0wDEthGDrRa97YZ/yxc/PlQONIznPr1/Yg3VXlw3gJmben9kF1p1V330+vuZYLLriAWCzGgTPmkA9crJgNBYfBrj42umVmzJzJ6SecyCEnHslxRx/D3FlztA/ihT6WMjFF44YmvomWFqPyeNUoRg/fUJQNn8Aydb1AHvq7huQuDIxIdY85F1W3u/rYSzS29uONel8lKJxQEtGXC6uqhKeffpojDj+c2ppaWlpacLwyKjTYvHkzJdflqGOP5eT3vo/zP3UOzVPao4VVvLrqUqobyjHa1YszNEyi4OC6rv4NK53EqE1BXRprUi1WKk3C88Ey8YWZvocdmhhG1XEIMG1jGzf7LXC7+5VSOvYbLyHZbT42ATSeGcVikfPPPx/LtGhtbdXMyhXyjPQMMn/egXzmc5/lgn/8Er4slnweHys0ya/tYmTZKtwVa8mtWEfulXWowVHMsoeRl32utBT6lqJkhIR1KWqnt9M4tZ3ywlnUzZtB7YEzsOIxDOFsIIuuwH7V6/c8Tx9jvGTsRcaMrf14Cdkm3TvRdN1113Huuecy/4ADGR0dZcOGDWTTSS666GK+9pULUQmbYuhjmwqzu581DzxO+NhyupavJLd2I3XKJJNOYsYNiJt6Oxl2jWZs6Eeqx1YGgedTyhf0BjDyIXZTLbF5U4gddQBN7zuC+oPnEhpxRJGG49TUeEMuDLKsHZYvJoxUhfN7hSHi1oq9OPXUU7nnnnuor61jeHiY448/nn+96t845KCDwRCPCIJNfXTedg+5B54i9+JqUrE46WyKeE2GouFRDB2UZWIqMHzZ7QbKMAiNVwNMYYrYCSMI8TCJBYpS/zB9fX3YU5tpfN9R1J5yLI3HHYKwRRghUvxWxkB7jSFVse/p6eGQQw7RtkLc3gsvvJDLv/c97bKWDUXcDXnh2rsYvvVBWLmO2qYsNCYoxWMoxyfmq8jNtWPanPh+SMyyCVQp+o1xCTo/CBCNpO2KghK+ZmLaU1iDLt29AxRr00w5fAGJyz6lY53qeT766KMsXbqU008/ncmTJ29zPXuKqgzZ8zKplF7AZcuW0LVxI4ZlcMNtt/HxRR8de79/8TJ6Lr2e0lNLyNSmSR/YznDgkSaGrXxKdqh3cNIRRrg4tqy2rz2ksgqxlML1vEhyxE8OQ0zLwg0DLNcgZVh4jk8pbuI2KNJ1rUwqeYz+7nE2v7wY55OnM/uCTyICt/+8+dzzwL3Mnb8f8w84iL89cxEnHnkMM2fOpKF5EpZw2gsRTudUSHosBIp+Vx5yrrtaOtjzKku0iu/zmfPP44YbbuDe++7j5Pe8T/902YQNV99G6ft3UArKqDlNZEKFQ4DrKxKhhSqUKCgfG4u0svCSNrl4QOh7pFywPIVhW+QMX/9czJXwxcAzQAUhgeGN5cdMZaG8QJ+PYdqagf7AKLkNvbSdfALTf/QVvKZaLA9uvvF6PnXeOTqgzMYSNDZP4r2nfIjzzzuPhQe9Q6tYR0Vu9NaLX5W2N8OUvWdDwoD+gUEW7H8QV131I077yOmYpiJQPs9/9d8pXn83tR0tUJsgUfIppC3MnAu9RfrcIjVTW7WqKRoBg/0DJPvz1DXWEbRm8UMPwzexMSiZoXZv7YILpqGZaoeKYtLHcENtV8TuB4YZ2QcvxAwV8rUgFjL04mpi+81i9nXfpHbWNCQ8uePXd3L26R8hbSVIZzNsHurTv/GVL/8DV3zv+yjLwg9ea2/GxzJvhvYaQzx8nnz0Cdas7OTTn/lUJDHK5Y+f+Sbh/U/T1lHPQFpRS5w4Fs7GIdZZHi3HLaTxXYfQfsAcnNYaSoHHwMud5J58AefBZzFe6aK2vYnhjE3CCfFdF5IWoedjBRUVIpIShMQ9SIjaCgNy4lDHLCRrolwfz5KUq4tvhJTX9BA2TWL6zd+gbt5sEpj8/Je388mzPk5z0yRSNVn6hgYYHBzkhGOO47e/uZtUXY2Og2z7tUnyN8uYvehlBRTzJex0KorvHJ8XvvBdrLv+iHHQZJTh4IYhCZWg9EofgzMmMe8bn6XpvUdg6lyVIq8C0kqH1jgWFNetZ90Pf07+zsdIt9eSqs1qT05sRiiucBg9fFMR90z9ui8RvnZjRWW5Wq1JLkscimRgaMMfs0zyKzfh1GQ48K4raJg7i6IZ8N1LL+WyS77J3Okz9ffKvsfatWv50AdP5p7f3jumosbHLW/Wbd6LKiv6lQI+KTfg2W9dS/mqX9K4cDZ5o0zoeKTTWQZXbMacP5uZ//fr1LY0o/wQZSjyhGSUouSFJMXXdcCLg1VyWHrVLTg/upNkayOx+gyFQkHvVE/+E4MuKgufmngSo1QW/1vHK2WnhBEG2JZFEM/gJGIkJAANC2QsE2dDH/2JNAt+fw0NrU0aHnLyh0/m4Xvv14lOI25T8BzWrV3L5d+9nIsuumiMAbtiP/YuQ9wQ31aYnse6635F/z9dqyVjJOXTVFSUEyZhT4GysjjoF5eTmT0NV4EVhgQS5evdFmDJjtYubahtEDrJ67H03EsYfXI5zY1N5K2AVGDg4lGy0LbHsw2cwVG8QglisSil0lCL47kURkaxuwok8mVqWurxEiFlMyBdCOkZHEHNm8pRN18FWZu1fZt5x/4HYroBDU2NWh2KK9/Q0MCzzz6r/7IbAWWVIXse0qGUhojnn36RLd+6nszUJhKWoq6sCFVAvOTjDo4y6Zz3k5k+lbJkNDwfhU+Ig/LK2JbsnEB8XnGVNOy86Jd0QDj9O+fjZxOQK1G20OrE8iLXUwI8VvWSx6D+kx9mv1suY86vruSAu/6Nd95yFYdedyVTvnsB1jEH0tu1Ga/sEAY2w9kENa0NxB99jsd/fJ0utE5paedHP7ma4dwIjufp4zc1NLJu3Tod7FaDUmGGPN/V/b37EqKjNAmLjUoGtRLcRCkjCRdQYYnnPvB5zM5uzKmTKXmBhkSWrBLGiE8xneHAX1+B1Viva5pWBesfD3ZmywS8+PnLKf3uLwQdDSTcKFJPOj5rujoxjz6WY792Lv7CmTiEpKU2Ukk4BprlPnZosPpnd7PhBzdSm7Wwa2wajDjDo0WKG7rouPdfmXToYboA/qEjj+fJp/7ErOkzKBCybl0npy06nTvvvPPVJanalPELvAOaMAmRAFrcTHFvJRLQDqAnsUcYRcsGLLvyFrrXbiDWXD+mW/0w0EGc6P3MtBay2VqS8v0onMD1nW1+a3skScLWwxeQD118MyQ0FTkzpK+rl8ZjD+OE6y7BWDhTMy4jdsnXILAoeRxKrKMwlcG8T5zKjO+fTzlXJD3qky+Vsesy1GSyvHTJfxEWSrrh5btXX6Vd8IFSHtO2SCQSrF+/XufmqpIxlpzkze/x3WaI+PuB+JCVi9QkjLBUtAPXbWHgxgeoj6Xw0onoRwNfShk6FhAjqxoyESdFIrxKgGfunB72lcKcMomsHccolEhZFkZfDmdKMwdf/o+MpuOMBg6mX8nfG+AYCjdK+epjuPInCbMWnUTLuafQ3zukSwLizorDkHhyFevuekhvsiMOWcj7TzuFzd1d+v1sNktvb+9YmWF8pnhXaLcZYsohgujHy4Grs6fCEF9DKhSrb7mbZPcITU3NlAvFKJEnFsKo5J4CTzPBMyuMtE3NJF1w3QnQieVW/gYBdXLkYgkGCkw+71Ty0yeT9QJqVAzTMPEDDzfwNO+1i2CIHTPlD6VQbJRB2xcXYc/tICh6GF7AoOWTbmlk9KbfEZQKUPL5wvmf09cdMxSlUkljAMR2bI2gUTutsF6l3WaILcKhosWzDEsbWtELgbzQM8TAL/9AormWQuiR8E0dkNmSe3JdDMPCtk3i/RKuBRR8T5+RToVv80uvQybk1nUxWC4Qxi2cfBFvWiOZkw4lITV1I1Kdoj4koraVhemhDb8O3mThKk6A4zuks7U0vfcoRgaHdRwj5+hOSuM8t4K19z2q0/4fPP69HHn44Wzq6tKq6uCDDyaZTEZM2Coe2esMUVXJlAi5gk4oS01D8Kh3PEBy0wB+UxpXhcQtG8s2tH2Q524QkspmGH1lE2FnF/FKQnBM3HciAz6kPEaXrCBmmwwaHk65jLF/Bw1TpmAEUDYMDXQQ9SnlXAE7ibssdk/HCbKhooQbMSumVVXqHbOxTJNABcSKHgnDIN6UYeSORyggpQSbvz1jEUXZBGHIe97znrH0yWvU1lthQ6gadqMSM/gephEl8YYfXoyVNHFCF9uwtVciFyA70xYVIiccM8n1D7Dlhge0QRdp01XGnbycxNpu+v60hMZJDcRDhV/ySNRmtZPhGtLgorADdN7K012aAb5tarUqzA9EVZnCHwk6A0qiRTMpnR+TQNIyTMqiqhoSGM+uwnt5I14QcMJxxyPaSeo8RxxxRFQkq2R7d4d2myHy+7rRwTL0xUl5VtTV0KpOWNNNrK2OhOSN/BBXgkDPx07YeMWyTpGLWqiprWXjrQ8y2rkRJVdpqOjvTkj9iq//BGsoRyFpkikrYlYc5WkXipjYNnHJwygeMnV7sIElO8iTmomhvXWRGHF//XigJVtyXLJpTMtgNHShJqlthDlYoPc3jxNaBoctOIR5c2dTX1/P3Llz9blMRLl391WWKfFCqC/ak/JpYOhUeeGx51E93fh2XKe9JQiMuX6U8BOX2Db1hTumSToTp350hCXnfB1n9St4BFh+1agHkeflRY6CuESy3uUw5Pl/+U8Kj/yJuslNhJ4iHzfxMybJNZsIXUd7U7Lo4gqjo/9IxYqHJzkxrWQCg0BZJH0bQ+yL62H09FFyy5ihpYPSuGfh+QqjJUVu8RJsArykybTpMzlg/oHa9a2mScYzRe2CsEyIygor4DQzcvG12BS39Gs9vSMxNgMDRxg6p5Wwb4Tnz/8e6++4H8fWkCxyeiVNPCvUhl92vruyk9Wfuxzv2t+Qmd6iF1HZFp4bYCaTbFnZSfeyNdgeeiNIXcQJfIoqwNP/hpin9PGj8zYoGEHEf8ug/8FnSGXS2qUXVeQ5LoZlYpgmpb4h/P4Rfa1tbW26Cso4Rsi16gzBLkrMxFUMxYsUz0Vqpo5Lcc1mrIT1hsyQE/ZQJH0oxQyyU1sxOnvpv/Aaun7xEJP/5nhqD9ifoaSl81OF3gHcXz7O2keegpE8HXNaGSrncF0Pt+xQl0zjZmzCriF6rr+P1n+fr+MPOSdb19bRxrtkeBiWpYtLxQrYUXJgUnAa/ssyhh56mmRLrX5DkpWuI56awkwl8LcM0r9sNU0nHKqhrqKyqgzYGrWyKzQhDKmmCSTylVNzRvL467uxEjse5pANLPLJEOW4pIo+flOGetMiv3gNXU++SH+yQRev0iWPkfwI8bJD85RGjGya4fVdGK3NGG1NOINDbHllC81tjTS0NTL668fpPHI/Jp/9N1oNCAYrLhkFTBJ+JNV55ZOWACiAfEzD8Oj5+nU64RkXZ8TwUY5HEJgErkvcMnQBzOncgnoXnHLKKZoJ44GAjHN92QUpmTAJEY/JqjCm0NsPAzlUTAz9qxKyvZNTrocp2dxEjLKoB53HclDNaVJWhpphgwFKuGmDeCKJYdZgByaDG/rIfuS9tJ17Oo0dUxncvIX1N9xN952/oznbSLY2Ru93/hunrYF5Rx9BkLAYCHwyyiQmUhFAyjS1LYl5YOdyvHzBDym/3En7rFaGbY9E0dPnHEvE8QIfL/CwvRBrqKhtZl1dnb6G8Sn33UWrTFi216j8zw9DSgPDBMUigbljWKaTNgmMQFf5JDKOkIUWdjKB64fk6gxdYvXx8dIxXQcvbh4ks+jdzPnBV4jvNwMvFaNudgcHX/xF2j/yPgbXbsBpStDoh2z+/JWsv+pW1PotNAgzqvvDRB8zhkfXn55i9TmX03/vYyRnNzNqeFhFWXylwdxifySmketxAx8/XxrDdwsTqiprfP1j/OtvhiZGQoIQQxbciNIFkr7QQALj9e1HlXy3qBe55JUldIjKr305QsPAyti6Zp1MZbAcF78U6kAtV5ei4+/PJB6YkhjTNsArhQRJxfQvncnw3Y9RLnmYrTW0DTh0/eTn9Nz9CNnjF8J+7cSzaWLlssZqjTy/iv4/PItlGTQdMofBQo5kXOBFhq67GH6AE/okfAPPUrgmlAWAVzl/YcLWHlYVebIrNCEMGYPwVyTFrLj+xviE4+uQKZ7YcIH8UAErncaozRLMaNE1B1F7QdcwZrpMeVIGQ6A3FMlOaqR2UqM2uvHA0WA4KxEFnulJ9cRnd1Bcthq3JYFfr0jW1qLyBUZvvR+v7GLELQIzxHfKJI0kTTNawHMxh/O0GhYFJ6CsS72mTvNIVlccFt/38CxDG3jUa6Gm22tp2BUo0O4zROIPU2nf3PQ1Ok3HCBI8Se7KNX1kP2WIoUplHCvAtUVj2CjfoLBqmGByPXWffj+ti05ETZlEDItEYDE4MMDgk8/T/d/3kl62ltz+NdRbPkO9Gxjp66NhSodARvTuls2QChWDg8Pk1vaSTaX1a2EQJf2MrEEiGcO045TLjq6ZSInXsxWu7xOLJyi5BVwril1syRpIOddXWn0V0gbJkkcu8HFDPwqKrFcrHuMXvvp8V6Rk9xkiCTodbwQRpFN4UpcmsCIojhcamKKSyi5uyiLr+drQS5LWWduN+sDhLPziR4ktnI3keE0vxDVNPAUNDe3UzGqlY9EJrLn8BuwbHyBsSIjnyrorbydz5VcjCKhImiNoEkX/D24ntqkHa24bsbKDaduUiwKySDIq8BPlYSYMCq6LlYyTGvUZigc4gUs6HtdBqVxTyrA1+E7iHpGQUrGokzmh62FlU5GEBNE1TyTtPkMkOifCX0neR54n25uws1nKXh7LiuuAzYhZmIS4YhsMg4G13TrOmHnNP+nATC5OuqeUZehClV4XCcwMsOMJZlz6eXqa69j4vRvJzGonf8cjrPYDpp9zFuHUOpz8ED0/+w0Ddz5Ew5w2Cm4Jw3EJ+ke0UTYHRqmNpzRj3IxFSVzgXBHfTpCM2XiuG9U0dL3NqHhVgd5odtwmFgqeWFSYTVCfrZRWtu+o7A7tPkN8X7IPOllIlEIiUV9DalI95Q0FEmacwHG1gQwdgYFCsr9Eak4Hc37wZXxlaadABYoUxlijjfil0geZKAUQj0ZzNX75DEZfXMfovY8zrb2N3P1/4U9PvkQ8ncAcHiZb9misr8HvGiTnlkhNayO2/1ysTIzA9Qi6h9mydDVGD6TbJ+GnkhQcD7scavWlyzOVql/Jd3VKJPBcXSqIYeI4JV2vUc21OqFqhn+NDNFokJD+vj4G+oaZO3cOmUwtdvskistXU8gmiBkmhhtQjFvEPZ9c9wD13/gUo9kU2aLkhQwcwyQVVofjid2RrLGNlTD1JLBEMSCVjNH2tbMZ+dMyBvwCtCVpGnEwRl0sWaiYxfDabtKHHcCk04+j9QNHY7S3UlPJMo/4RWJPvcDwjb+n/8GnqUtlaK5PM6Rc7UnFDVMbbA0hsiwtWTENlgh0Xsr3fMK6DE1zZ0bXLrZETazK2v1sr6StQ58H77ufm66/Ab9U8b1nt+K6vs4xiY0pmbLzfNyhHOb+U5h+2rvIhuAmDZ12T0kOUUHRCvEsU0uWsNpBkXA09FAvSmJGB+mTj8QdKVIKPZIxA5U2tVD1rO0i9fGTOODnlzHzM4uoa2qjRg4qLQuhSY2ZpvmYI1nw04tY8M0L8Ioe5Y29+DGTIGnj+h6+OAgas2vopKbUbqqwHt8NCNoadDOQQFDDPYDZ2e1DSso9rkxeWLqMJ554AjMZ2ZHwoOkaDGCWypRDV2dYbQmWCgXSRx+gd794KpZutNHf0Ak7qfKJ2lM6JlHoKnzMAin/qmiy5qQD5+KWXTKhRSlt6eSk1zVM+6dPZd4P/xHSmah3xEZDRTXJZg4U8UBSlCZ1Z51Iy81fY33Kp9Q7RG1g6cyoXYmFpKiVsCJVKRtBqgGF0QLxOZMJEnZFkideZe02Q3T5NoRVL6/g+eefpxxEBatJhx1Aw5R2rNGylqJEOdD43ISg2utqdPXOt8ZV2ORvEOrgUP4ZVqJ+vfW9AD8dpxT5QGQa63B0x1OA74U4gwXM+XPouPxz0lKlsV1UavRSnfEFkWIHeGZU1bTcAGyTxqMOZsZnTyE+UKB2oKxfs52ANJYGbwteWKSj2u4m1PGO+RobJuflvvnhoztez21eeZOki7a5Mn9Z/TKD+SGe/NXd+rXa+lacIw5mc3lQ1zZKpqLWsBiRrJcb0ykSyeBqUZC6t7xuCHw0SpcracjUQZfAe+Q1g7QfFYndfI66ikHVgGk3oE0id4lgggjPpQEGXnSJpmlrT078PF0fkN5CZZDAYOoFZ+PM62DQzUNQwjFcnWhsyAV4MVMfT1SyWyoTTG5h0geP1uFHoFEsEz8HdPdxWWHAkuUvMNDdq6XloT/8AdePVNSMk44i7lgk3JCkMsj5Htl4En9jt8ZRJXyLIFRaHYhYBJUSsEaDiN0xpCHH1IUjo4xGpki0XBoYZCAoEyZjUCiTnTmZmuMXRDrdCXCMQLdPezvhsth2gvp37sdQLo9yQ227ZOerRAzlexRxqbET9Hb3kj7sQGhq1Gl6w1bE3nyqaoe0+2ZJGSxe8jzFfF73A/76vnsp5gvaM2p4z6FkF76DcGM/QUzp+rMEjYOPPY23aYtmWqjTK4aO2k3HwA6jljVhjKi3eGDoOrgYE9Fg4l33P76ETE0aK+8Q5EskO1pw0kn9m1Gp1tCR+M6QbPSaw/bXkhM3YtobEze3rLyo4mcocrkcdck6Os76AJ5dyeZqdTrxHJkAXBZ09/bowKpt6hRe6lzFvb/+jcbiOjED64wTKfoeSsJrZeIkLR0zDNz0ACX5vhcdQwYAOLHICPu6NGzgmaEGKmS0QRH4EPQ/8TybHvoztTU12s0NA49UfQ3JCqRHDLkpFb5QYQU7kdw0wGxt1GVmcXfF/U1aMZ3VVeJdmBbupkGyJ7yDhsMX6O9Il5a4WZ418fj03ZcQPxxzCwXFkchmuPZHP9ZNmrLQc8/4AL0Lp+F19mvIplBi8iQ23vhbYs90UrAiMINgo6qXZzk+lh9V9ySn5HuBjpjc4SFe/OdraKit0fkzqfZJ6sTNFTWwLqyWk3U6Y+cNbrFnUNfgAzE70nEtzaJh1PseL4aYnkHis+/X72kehFFd3/xrNOpCggKXerNA/GU6w1PP/IXrrv2pzvpaNsy9+Fx63DLGYFGrrbxA/m2bp8//Ft6LqwXDr8usYsy1ERWPRtrQRT8ZULLB7drCn//++6RWbCLVUk9JifNqYsRshjdsiq5EsqxBqAcIBIGvQQ47IjHL/vJOnSIJK50+XqkceVWuz2hnL6nzTqb9iHdqJkh6y48ZerMo969QQkSb7D9vnm5RlgKTL/FBbS3/+h9XEQisU4bDH3sYNeeewnBPP0pKofE0sZZ6Un39/HnRV9lw3S+xcgVso9L3YURzuj09rKTM8K8e5tG/u5j0/c/SPGuyDjCl3iLJSJVJaBs1sHi53tnVJXqjWv5rKF/CeXYVdjpO6LtRl60ZJUml0Fae3kbHRZ+I6jTSXm1HsZcltRh74me97XY7gvYsS2WNvlizZg1TJ0+haIas61zDP1/4f/jn71xG3EfDNF887ly8LT3Y06ZEMUfCx+gq0jcySuM7DyJ+7AK8jkm6+SYslujZshnjsRcYfGIJcVtRM6WJcrmo3VhJUtplHz8B7vItlM56F8dceRGOISVZvxIrRPjdN6JXHv0TG87+Fi0dzXhWoB0CT+yJ45J/ZTOz/vtS2k4+Bl+yxAJDNkWKrQhKpNSE3QJiwjqoqkWYK664gq9+9avMmTNHZ01lrEVXVxcP//lxjjviaIoEJBd38ujHv06LpNdbkzjKxS5BIpbE7R6kMJjDTdkEYpgrtfYgndQdsJLoE6Nbnbqgz9nzdZdtwzBsGS4w7eJzmPrpUytwUTCcyhXGKsNTBN4Vi3S/xC8jQz2s/CSiWyoAAAlOSURBVOBXiY0WsSbX43sOvmkSK0P3SxuYedEnmPa1c6rr85rxGxM97WFCW9qk4VIW6cgjj9TtXdJkLycrjZFzJk/hyReXkU2k9Gd77n2MZZ//Lh2JFMPTJCZOYuZKqITofkki+tqIOqFBwohTtKJjS7Tvj+u/UJVFSvk+5YSN01ekZ2SU+ZddQMMnPoCPqXdvEJaIKYsSltbPsUrjqLN0LS98/gqsTa/gzmuladSDuKXrNvlVXdgffReH/PgiqQfo1jVxXKpta3uCJqxhRyREDLUw4NZbb6WxsVGrLlmsadOmsaLzFc46ZVHEuNCn7sPHcsB3v8QWp0iwOY9d9AhTlq4/xMpB5IlZJlY6wYAVdc5q76cKPjOjU66iWYb1zBOF0xSnvSZL/yX/xdoLf0T++WUYoUNMJchhRZ1Zns9Ifw+bfnI7Kz93KWrLRmqmt2A7rk6VGDmX0Zc2kj79BOb/+GvklKWbcX74wx++5pqr4IVdATHsiHZbQsaPkxBavnw5Z5xxBi+99JJmTqaung2da/n4mR/lpttu1nkuI3Do+eWjLPmnq2i1FNkpLXp2iVP28FO2LgxZgli3Re1UkI8iFVVmSGgfVOrZUhST1EvgkbEsRoZG8QcLWA319M+fTNP8+UxvbiE/PMTw2k24i1+m9HInqZYaPXzALXvUxVN4vaP0vbKJzGc+xPwr/gHbTGgtd8Shh3LSSSdx+eWXjzFBNt9Ej26aUJW1NVMksr3sssu4/vrr6e7pjZplDPjsOefys6uvwTFdLGVQuPcpXv7WfzC4uZeW9nbSmYy2PV7c0L3k9YLXtdQYEC/gVViqbvxXUf1bxm9IvbxflcjYCWKjrs5veTmH4aCgPSeJM8SrTTfWYTbW6eZQQSvK8Ub7BymOFGn78iJmXPQZmdKl82EfO+0sbr/7Dq1629vbx5CJ7IHxTRPGkK2N2/idIx2qv7jtTp59YSlPLFnMxuWrOPzQhdz+6//HlJY2ClKq2LSFpRf9B+bvnqGpvga3OR2NySiGZK2ENvyisoIK07XjVD3tMNQDzty4IsgVMaWuUWl1KJhRhllc4bKggq1I3YX6fC1dz7A9g+51vRi1aaZ+73xaTj4WS9mUDZNzzjqbn99+B4cdvlBPTK2SW8kAaxjsBDJlwvvUx09kk+fyN5opAgULwuERHnroIW64/TYOnb+AT557Hs2T26Isueez8pqfs+WaO0gMF3VNPlaTpSgxS0VPB6raVVBJ11f6TOS5gCliKooJpFlIflf6GEUiir7CTtqYnqtzT56A8gTS0zdMfniUye85iYZvnk16zjRdf+nu7+Njp53BI088rhH6/3LRxXz729/eZvH/alXW1upqe++LT+TryFqvGLliTtcxauvqdD2++s3yyk423nAPG+96ADOfJ9tYQ6KuUasqKnBVxi2GdPFK8Ssl3pikO8rRkBkZeilhSEmwuTGLeNHRKtLxPdz1g7qOYhy3gGnn/S2N7zuaUQWJMOCP9/2ev/vCufSt38R+06azdMMr3HbLbZx55pmvsRt74q4Ne3Wi3BtSWJnjK26tbHzPI7fsFbp//Uf6HnkO1q7RYUQ2nSGejlMWXJfYFQFN+EFUZwwjkIJRKXIFMl1OOqQkF5Z3cEouQ8OjWE0NNBw+n8kfPoG6DxxNIWHrOr5AfEQKJJYSkoFmYgeFCYufe5ampqbXjM1gOyOZdpf+ahgiaCeJF6Tk6inpA4zskWRszVyZnsf/zPonniP31IukukZJlD2NBJF6ianbHZQ28CItAt8RLFXBLWvmyuhZo66W2NzJ1L77EDLHLqBmvznRUALpog3h1ltu4Tvf+Q4vvfwSrS2t1EgWWSlWrFzBxV+/mEu++Q3t1vM66MSJor8ahui5VkQAhrHRB9WxsNXxfyJBgzlynRsZXNlJobMLr6sfRovEpf1M+uFVqHG3UrRKNNfT0NFOQ2szQ++cQXN7W1QXjsDHFAol7r7nt1x99dX88bE/EI/FdfONZAOqGQbp+1i8eDHtUyaPMYCt8Lt7miHlt+TehJXxGW4YGWg9Fnzc1tBIyHCcZqt0uqmKCyygEhlkZktlkagrSscplZ0sGeFKGMPSpS/w0IMPctMNN/LCsqV6IHPbtMlj80mkOUdmz+fzee666y49tLOK0xo/JDPcQYvFLpCjlNJpsfE+2+ieGKS8QxrzniJnVlXaifVCCwSoUnIQwIPYDb3I1WZOw9QLHVOxSiolekjc09XVzZIXljE00KczBw8//DDLli2jt7eH2kyGaR2TsU1L45DFVogXtWLFCn38m266STODKmB8qzs4TCAjqjRafTKeIV1vBUMklS372lIVzsg8EokRDKWxCDKRThZYJCfQLnDUzOjq9zySkgCrDqIMK7i1EDasX88fH3mUP9x/P4ufe0bPrZSPxeO2rt34RkDJyTM6UtTN/0LSoiYRebVvcLwk7OFbMXVVn4xXWXdVbue2dyl89Uz8cf/U8UnV+xp7vVLAgrE5v1ZlyKYscrVFoLpw2ggrg1UrV2oJeX7pEl5e/hKda9ZQGs1rFdc+Zwbz5s3jQx/6EB/72MfGDHc1lhpbqB00Hu0m/UIpdQZbScjit4Ih4llZFb0lI/0CDfOqTAlRFS5Vpgq9BtwcREOIPOXrQTd+5QYVhqrOGAm1GZEM/Mx5c5k9b270qg9r165naGiIWDzO9BlTSKfT+pDjR7xWg9ztje/bA9LyTPXJeAk5Enhym4/uo71BRyqlntqaIW/JLY/20WtveTQ+1JQXbt63Pnudbh4PkRkvIVSkY82+e6XvNRITN0ukpGqPtk7GbKzclH0f7R26rrLmY7S1hFCJRVa8JUHi/y7qr9zqSP7yehJC5QNf2ubVfTTR9PdVZoyn7TGEyp2if7rNq/toouhnwK3bO9b2VFaVxLDfue8G9xNOcoP7MysGfYzeSGVVSb7wMeC+bd7ZR7tK91bW9HWHEr8RQ4QKwKn71NeEkKzhaZU1fV3amRqkDF34fIWzfdu8u492RLJmH6+sobuDz74p5KIY+v2Ba99I5PbRGDmVtZI1u21nl+WNjPob0ZSKa/x3wN67ldn/DNpUSYf8eOug742oatR3lSFVMiq3npY7TUtVZ26FWZm9faP8t4BE/eQqi76yUr74g9xd9k21b1VoL9/qdR/to320j3abgP8PxnLYciqgH4YAAAAASUVORK5CYII=" alt="آپارات">
    </a>
  </div>

<div class="app">
  <div class="header">
    <div class="header-top">
      <span class="title">🗡️ آزمون شیطان کش</span>
      <span class="score-badge" id="scoreBadge">🔥 ۰</span>
    </div>
    <div class="level-bar">
      <span class="level-label">🎯 سطح فعلی:</span>
      <span class="level-value" id="levelBadge">🌸 تازه‌کار</span>
    </div>
    <div class="progress-bar">
      <div class="progress-fill" id="progress"></div>
    </div>
  </div>

  <div class="content" id="content">
    <div id="quizArea" style="display:flex; flex-direction:column; flex:1;">
      <div class="question-card">
        <span class="q-label" id="qLabel">سوال ۱ از ۱۰</span>
        <div class="question-text" id="questionText"></div>
        <div id="answerArea"></div>
        <div class="feedback" id="feedback"></div>
        <div class="explain-box" id="explainBox">
          <div class="explain-title">📖 راهنمای تنفس</div>
          <div id="explainContent"></div>
        </div>
        <button class="next-btn" id="nextBtn" onclick="goNext()">سوال بعدی ←</button>
      </div>
    </div>

    <div class="result" id="resultScreen">
      <div class="emoji" id="resultEmoji">🔥</div>
      <h2 id="resultTitle">آفرین!</h2>
      <div class="level-title" id="levelTitle"></div>
      <div class="score-big" id="resultScore">۰٪</div>
      <div class="score-text" id="resultText"></div>
      <div class="result-stats">
        <div class="stat-box green">
          <span class="num" id="correctCount">۰</span>
          <span class="lbl">صحیح</span>
        </div>
        <div class="stat-box red">
          <span class="num" id="wrongCount">۰</span>
          <span class="lbl">غلط</span>
        </div>
      </div>
      <button class="btn" onclick="restartQuiz()">🔄 شروع دوباره</button>
    </div>
  </div>

  <div class="options-bar" id="optionsBar">
    <div class="options-title" id="optionsTitle">👇 پاسخ درست را انتخاب کن</div>
    <div class="options" id="options"></div>
  </div>
</div>

<script>
/* ===== تبدیل اعداد ===== */
function toFa(n) {
  return String(n).replace(/\d/g, d => '۰۱۲۳۴۵۶۷۸۹'[d]);
}
function faNum(n) {
  return toFa(Number(n).toLocaleString('en-US'));
}
function parseFa(str) {
  const faDigits = '۰۱۲۳۴۵۶۷۸۹';
  const enDigits = '0123456789';
  let result = String(str).trim();
  for (let i = 0; i < 10; i++) {
    result = result.split(faDigits[i]).join(enDigits[i]);
  }
  result = result.replace(/[،,٬\s]/g, '');
  return result;
}

/* ===== سطوح شیطان کش ===== */
function getLevelInfo(percent) {
  if (percent >= 80) return { badge: '🔥 هاشیرا', emoji: '🔥', title: 'در حد هاشیرا! 🔥', sub: 'فوق‌العاده! تو یک ستون شکارچیانی!' };
  if (percent >= 60) return { badge: '🗡️ شکارچی شیطان', emoji: '🗡️', title: 'در حد شکارچی شیطان! 🗡️', sub: 'عالی بود! نزدیک به کامل!' };
  if (percent >= 40) return { badge: '⚡ شاگرد تن‌گن', emoji: '⚡', title: 'در حد شاگرد تن‌گن! ⚡', sub: 'خوب بود! با تمرین بهتر می‌شوی.' };
  return { badge: '🌸 تازه‌کار', emoji: '🌸', title: 'در حد تازه‌کار! 🌸', sub: 'نیاز به تمرین بیشتر داری.' };
}

/* ===== بانک ۱۰ سوال به ترتیب ===== */
const questions = [
  {
    type: 'short',
    q: 'تانجیرو در شب اول ۱ شیطان، شب دوم ۴ شیطان، شب سوم ۷ شیطان و شب چهارم ۱۰ شیطان را شکست داد. اگر همین روند ادامه پیدا کند، شب پنجم چند شیطان شکست می‌دهد؟',
    answer: 13,
    numbersLine: '1 , 4 , 7 , 10 , ...',
    explain: [
      { fa: 'هر شب ۳ شیطان بیشتر از شب قبل شکست می‌دهد.', math: '1 -> 4 -> 7 -> 10' },
      { fa: 'پس شب پنجم:', math: '10 + 3 = 13' }
    ]
  },
  {
    type: 'mc',
    q: 'قدرت هاشیراها در جلسه‌ی مخفی به ترتیب زیر افزایش می‌یابد. قدرت بعدی کدام است؟',
    answer: '۲۵',
    distractors: ['۲۰', '۲۴', '۳۶'],
    numbersLine: '1 , 4 , 9 , 16 , ...',
    explain: [
      { fa: 'این اعداد توان دوم هستند.', math: '1^2 , 2^2 , 3^2 , 4^2' },
      { fa: 'قدرت بعدی:', math: '5^2 = 25' }
    ]
  },
  {
    type: 'short',
    q: 'زنیتسو در تمرین تنفس رعد، هر روز انرژی خود را نصف می‌کند. اگر روز اول ۶۴ واحد، روز دوم ۳۲ واحد، روز سوم ۱۶ واحد و روز چهارم ۸ واحد انرژی داشت، روز پنجم چند واحد انرژی دارد؟',
    answer: 4,
    numbersLine: '64 , 32 , 16 , 8 , ...',
    explain: [
      { fa: 'هر روز انرژی نصف می‌شود.', math: '64 / 2 = 32' },
      { fa: 'پس روز پنجم:', math: '8 / 2 = 4' }
    ]
  },
  {
    type: 'mc',
    q: 'تانجیرو در ۴ شب متوالی به ترتیب ۱، ۴، ۷ و ۱۰ شیطان را شکست داده است. کدام رابطه بین تعداد شیطان‌ها وجود دارد؟',
    answer: 'هر شب ۳ شیطان بیشتر می‌شود',
    distractors: ['هر شب ۲ برابر می‌شود', 'هر شب ۴ شیطان بیشتر می‌شود', 'تعداد شیطان‌ها تصادفی است'],
    numbersLine: '1 , 4 , 7 , 10',
    explain: [
      { fa: 'اختلاف هر دو عدد متوالی ۳ است.', math: '4 - 1 = 3' },
      { fa: 'پس هر شب ۳ شیطان بیشتر می‌شود.', math: '' }
    ]
  },
  {
    type: 'mc',
    q: 'شینوبو برای تمرین، داروهای خود را به شکل مثلث می‌چیند. برای مثلث اول ۴ دارو، مثلث دوم ۷ دارو و مثلث سوم ۱۰ دارو لازم دارد. برای مثلث پنجم چند دارو لازم است؟',
    answer: '۱۶',
    distractors: ['۱۳', '۱۹', '۲۲'],
    numbersLine: '4 , 7 , 10 , ...',
    explain: [
      { fa: 'هر مثلث ۳ دارو بیشتر از قبلی لازم دارد.', math: '4 , 7 , 10' },
      { fa: 'ردیف اعداد:', math: '4 , 7 , 10 , 13 , 16' },
      { fa: 'پس مثلث پنجم:', math: '16 دارو' }
    ]
  },
  {
    type: 'short',
    q: 'رنگ‌کو برای تمرین شمشیرزنی، تیغه‌ها را به ترتیب زیر می‌چیند (۴، ۷، ۱۰، ...). برای ردیف دهم چند تیغه لازم است؟',
    answer: 31,
    numbersLine: '4 , 7 , 10 , ...',
    explain: [
      { fa: 'رابطه: ۳ برابر شماره ردیف به‌علاوه ۱', math: '3n + 1' },
      { fa: 'برای ردیف دهم:', math: '3 * 10 + 1 = 31' }
    ]
  },
  {
    type: 'mc',
    q: 'گیو در تمرین با شمشیرهای چوبی، ردیف‌هایی به این ترتیب می‌سازد (۴، ۷، ۱۰، ۱۳، ۱۶، ...). ردیف ششم چند شمشیر چوبی دارد؟',
    answer: '۱۹',
    distractors: ['۲۱', '۲۲', '۲۵'],
    numbersLine: '4 , 7 , 10 , 13 , 16 , ...',
    explain: [
      { fa: 'هر ردیف ۳ شمشیر بیشتر از قبلی دارد.', math: '4 , 7 , 10 , 13 , 16' },
      { fa: 'ردیف ششم:', math: '16 + 3 = 19' }
    ]
  },
  {
    type: 'mc',
    q: 'تانجیرو در یک مزرعه ۲۰ حیوان (مرغ و گوسفند) دیده. اگر تعداد پاهای کل ۵۶ باشد، چند گوسفند در مزرعه وجود دارد؟',
    answer: '۸',
    distractors: ['۵', '۱۰', '۱۲'],
    numbersLine: '20 animals , 56 legs',
    explain: [
      { fa: 'مرغ ۲ پا و گوسفند ۴ پا دارد.', math: 'مرغ = 2 / گوسفند = 4' },
      { fa: 'حدس: ۱۲ مرغ + ۸ گوسفند', math: '12 * 2 + 8 * 4 = 24 + 32 = 56' },
      { fa: 'پس ۸ گوسفند داریم.', math: '' }
    ]
  },
  {
    type: 'short',
    q: 'دو زاویه مکمل یکدیگرند (مجموعشان ۱۸۰ درجه است). اگر یکی از آن‌ها ۳۰ درجه باشد، زاویه‌ی دیگر چند درجه است؟',
    answer: 150,
    numbersLine: '90 - x = y',
    explain: [
      { fa: 'دو زاویه مکمل مجموعشان ۱۸۰ درجه است.', math: 'x + y = 180' },
      { fa: 'اگر یکی ۳۰ باشد:', math: '180 - 30 = 150' }
    ]
  },
  {
    type: 'mc',
    q: 'اگر در عبارت ۳x + ۱۰ به جای x عددی بگذاریم و حاصل ۴۶ شود، x چند است؟',
    answer: '۱۲',
    distractors: ['۱۰', '۱۴', '۱۶'],
    numbersLine: '3x + 10 = 46',
    explain: [
      { fa: 'ابتدا ۱۰ را از دو طرف کم می‌کنیم.', math: '3x = 46 - 10 = 36' },
      { fa: 'حالا بر ۳ تقسیم می‌کنیم.', math: 'x = 36 / 3 = 12' }
    ]
  }
];

/* ===== وضعیت ===== */
let current = 0;
let score = 0;
let wrong = 0;
let answered = false;

const questionText = document.getElementById('questionText');
const answerArea = document.getElementById('answerArea');
const optionsEl = document.getElementById('options');
const feedbackEl = document.getElementById('feedback');
const qLabel = document.getElementById('qLabel');
const progress = document.getElementById('progress');
const scoreBadge = document.getElementById('scoreBadge');
const levelBadge = document.getElementById('levelBadge');
const quizArea = document.getElementById('quizArea');
const resultScreen = document.getElementById('resultScreen');
const content = document.getElementById('content');
const explainBox = document.getElementById('explainBox');
const explainContent = document.getElementById('explainContent');
const nextBtn = document.getElementById('nextBtn');
const optionsTitle = document.getElementById('optionsTitle');
const optionsBar = document.getElementById('optionsBar');

function shuffle(arr) {
  const a = arr.slice();
  for (let i = a.length - 1; i > 0; i--) {
    const j = Math.floor(Math.random() * (i + 1));
    [a[i], a[j]] = [a[j], a[i]];
  }
  return a;
}

function updateLevelBadge() {
  const total = questions.length;
  const percent = Math.round(score / total * 100);
  const info = getLevelInfo(percent);
  levelBadge.textContent = info.badge;
}

function renderQuestion() {
  answered = false;
  const q = questions[current];

  qLabel.textContent = 'سوال ' + toFa(current + 1) + ' از ' + toFa(questions.length);
  questionText.textContent = q.q;

  // اضافه کردن خط اعداد اگر وجود دارد
  const existingNumLine = document.getElementById('numbersLine');
  if (existingNumLine) existingNumLine.remove();

  if (q.numbersLine) {
    const numLine = document.createElement('div');
    numLine.className = 'numbers-line';
    numLine.id = 'numbersLine';
    numLine.textContent = q.numbersLine;
    questionText.insertAdjacentElement('afterend', numLine);
  }

  answerArea.innerHTML = '';
  optionsEl.innerHTML = '';
  optionsTitle.textContent = '';

  if (q.type === 'mc') {
    optionsTitle.textContent = '👇 پاسخ درست را انتخاب کن';
    optionsBar.style.display = 'block';
    const allOpts = shuffle([q.answer, ...q.distractors]);
    allOpts.forEach(opt => {
      const btn = document.createElement('button');
      btn.className = 'opt-btn';
      if (opt.length > 15) {
        btn.classList.add('long-text');
      }
      btn.textContent = opt;
      btn.dataset.value = opt;
      btn.onclick = () => chooseOption(opt, btn);
      optionsEl.appendChild(btn);
    });
  } else if (q.type === 'short') {
    optionsTitle.textContent = '✍️ پاسخ را با ارقام بنویس';
    optionsBar.style.display = 'block';
    const box = document.createElement('div');
    box.className = 'short-answer-box';
    box.innerHTML = `
      <input type="text" class="short-input" id="shortInput" placeholder="پاسخ عددی..." inputmode="numeric" autocomplete="off">
      <button class="submit-btn" id="submitBtn" onclick="submitShort()">ثبت</button>
    `;
    answerArea.appendChild(box);
    setTimeout(() => {
      const input = document.getElementById('shortInput');
      if (input) {
        input.focus();
        input.addEventListener('keydown', (e) => {
          if (e.key === 'Enter') submitShort();
        });
      }
    }, 100);
  }

  feedbackEl.className = 'feedback';
  feedbackEl.innerHTML = '';
  explainBox.classList.remove('show');
  explainContent.innerHTML = '';
  nextBtn.classList.remove('show');

  progress.style.width = (current / questions.length * 100) + '%';
  content.scrollTop = 0;

  const card = document.querySelector('.question-card');
  card.style.animation = 'none';
  void card.offsetWidth;
  card.style.animation = 'popIn 0.35s ease';
}

function chooseOption(value, btn) {
  if (answered) return;
  answered = true;
  const q = questions[current];
  const isCorrect = (value === q.answer);

  document.querySelectorAll('.opt-btn').forEach(b => {
    b.disabled = true;
    b.style.pointerEvents = 'none';
  });

  if (isCorrect) {
    score++;
    btn.classList.add('correct');
    feedbackEl.className = 'feedback show ok';
    feedbackEl.innerHTML = '🔥 عالی! مثل هاشیرا پاسخ دادی!';
    scoreBadge.textContent = '🔥 ' + toFa(score);
  } else {
    wrong++;
    btn.classList.add('wrong');
    document.querySelectorAll('.opt-btn').forEach(b => {
      if (b.dataset.value === q.answer) b.classList.add('correct');
    });
    feedbackEl.className = 'feedback show no';
    feedbackEl.innerHTML = '💀 پاسخ درست: ' + q.answer;
  }

  updateLevelBadge();
  showExplanation(q);
}

function submitShort() {
  if (answered) return;
  const input = document.getElementById('shortInput');
  if (!input) return;

  const userAnswer = parseFa(input.value);
  if (userAnswer === '') {
    input.focus();
    return;
  }

  answered = true;
  const q = questions[current];
  const isCorrect = (Number(userAnswer) === q.answer);

  input.disabled = true;
  const submitBtn = document.getElementById('submitBtn');
  if (submitBtn) submitBtn.disabled = true;

  if (isCorrect) {
    score++;
    input.classList.add('correct');
    feedbackEl.className = 'feedback show ok';
    feedbackEl.innerHTML = '🔥 عالی! مثل هاشیرا پاسخ دادی!';
    scoreBadge.textContent = '🔥 ' + toFa(score);
  } else {
    wrong++;
    input.classList.add('wrong');
    feedbackEl.className = 'feedback show no';
    feedbackEl.innerHTML = '💀 پاسخ درست: ' + faNum(q.answer);
  }

  updateLevelBadge();
  showExplanation(q);
}

function showExplanation(q) {
  setTimeout(() => {
    explainContent.innerHTML = buildExplanation(q);
    explainBox.classList.add('show');
    nextBtn.classList.add('show');
    nextBtn.textContent = (current === questions.length - 1) ? 'مشاهده نتیجه 🗡️' : 'سوال بعدی ←';
    setTimeout(() => {
      explainBox.scrollIntoView({ behavior: 'smooth', block: 'end' });
    }, 100);
  }, 400);
}

function buildExplanation(q) {
  let html = '';
  q.explain.forEach(step => {
    html += '<div class="explain-step">';
    if (step.fa) html += '<div class="fa-line">' + step.fa + '</div>';
    if (step.math) {
      const hasPersian = /[\u0600-\u06FF]/.test(step.math);
      if (hasPersian) {
        html += '<div class="math-line"><span class="rtl-text">' + step.math + '</span></div>';
      } else {
        html += '<div class="math-line">' + step.math + '</div>';
      }
    }
    html += '</div>';
  });

  let ansText = (q.type === 'short') ? faNum(q.answer) : q.answer;
  html += '<div class="explain-final">✅ پاسخ درست: <span class="num">' + ansText + '</span></div>';
  return html;
}

function goNext() {
  current++;
  if (current < questions.length) {
    renderQuestion();
  } else {
    showResult();
  }
}

function showResult() {
  progress.style.width = '100%';
  quizArea.style.display = 'none';
  optionsBar.style.display = 'none';
  resultScreen.classList.add('show');
  content.scrollTop = 0;

  const total = questions.length;
  const percent = Math.round(score / total * 100);

  document.getElementById('resultScore').textContent = toFa(percent) + '٪';
  document.getElementById('correctCount').textContent = toFa(score);
  document.getElementById('wrongCount').textContent = toFa(wrong);

  const info = getLevelInfo(percent);
  document.getElementById('resultEmoji').textContent = info.emoji;
  document.getElementById('resultTitle').textContent = info.sub;
  document.getElementById('levelTitle').textContent = info.title;
  document.getElementById('resultText').textContent =
    'به ' + toFa(score) + ' سوال از ' + toFa(total) + ' سوال درست پاسخ دادی.';
}

function restartQuiz() {
  current = 0;
  score = 0;
  wrong = 0;
  scoreBadge.textContent = '🔥 ۰';
  resultScreen.classList.remove('show');
  quizArea.style.display = 'flex';
  optionsBar.style.display = 'block';
  updateLevelBadge();
  renderQuestion();
}

updateLevelBadge();
renderQuestion();
</script>
</body>
</html>
