# -<!DOCTYPE html>
<html lang="ja">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>危険物乙四 擬人化ヒップホップRPG</title>
<style>
  body { background: #111; color: #fff; font-family: sans-serif; text-align: center; margin: 0; padding: 10px; }
  #game-box { max-width: 500px; margin: 0 auto; border: 3px solid #ff4500; border-radius: 12px; padding: 15px; background: #222; }
  .status { display: flex; justify-content: space-between; font-weight: bold; font-size: 1.1em; color: #ffbc00; }
  .monster { font-size: 3em; margin: 20px 0; }
  .question { font-size: 1.1em; margin: 15px 0; text-align: left; background: #333; padding: 10px; border-radius: 8px; }
  button { width: 100%; padding: 12px; margin: 6px 0; font-size: 1em; border: none; border-radius: 6px; background: #444; color: #fff; cursor: pointer; }
  button:hover { background: #ff4500; }
  .btn-hint { background: #008b8b; width: 50%; margin-top: 10px; }
  #hint-box { color: #00ffff; margin: 10px 0; font-size: 0.9em; display: none; }
</style>
</head>
<body>

<div id="game-box">
  <h2>🔥 危険物乙四 HIP-HOP RPG 🔥</h2>
  <div class="status">
    <div>HERO HP: <span id="hp">100</span></div>
    <div>STAGE: <span id="stage">1</span></div>
  </div>

  <div class="monster" id="monster">👾 静電気スライム</div>

  <div class="question" id="question">問題が読み込まれます...</div>
  <div id="answers"></div>

  <button class="btn-hint" onclick="showHint()">💡 ヒントを見る</button>
  <div id="hint-box"></div>
</div>

<script>
// 音声合成（ボイス）
function speak(text) {
  if ('speechSynthesis' in window) {
    const uttr = new SpeechSynthesisUtterance(text);
    uttr.lang = 'ja-JP';
    speechSynthesis.speak(uttr);
  }
}

// スーファミ風SE（Web Audio API）
const audioCtx = new (window.AudioContext || window.webkitAudioContext)();
function play16BitSE(type) {
  const osc = audioCtx.createOscillator();
  const gain = audioCtx.createGain();
  osc.type = 'square'; // レトロな矩形波
  osc.connect(gain);
  gain.connect(audioCtx.destination);
  
  if(type === 'correct') {
    osc.frequency.setValueAtTime(523.25, audioCtx.currentTime); // C5
    osc.frequency.setValueAtTime(659.25, audioCtx.currentTime + 0.1); // E5
    gain.gain.fadeOut(audioCtx.currentTime + 0.3);
  } else {
    osc.frequency.setValueAtTime(150, audioCtx.currentTime);
    osc.frequency.setValueAtTime(100, audioCtx.currentTime + 0.1);
    gain.gain.fadeOut(audioCtx.currentTime + 0.3);
  }
  osc.start();
  osc.stop(audioCtx.currentTime + 0.3);
}

// 問題データ
const quizData = [
  {
    q: "ガソリンの指定数量として正しいものはどれ？",
    a: ["200L", "400L", "1000L", "2000L"],
    correct: 0,
    hint: "第1石油類の非水溶性は「200リットル」だよ！",
    voice: "正解！ガソリンの指定数量は200リットルよ！"
  },
  {
    q: "電気火災に効果的な消火方法はどれ？",
    a: ["霧状の水消火薬剤", "棒状の強化液", "注水消火", "泡消火剤"],
    correct: 0,
    hint: "感電を防ぐため、電気を通さない「霧状」にするのがコツ！",
    voice: "ナイス判断！霧状の水なら感電を防げるわ！"
  }
];

let currentIdx = 0;
let hp = 100;

function loadQuestion() {
  const q = quizData[currentIdx];
  document.getElementById('question').innerText = q.q;
  document.getElementById('hint-box').style.display = 'none';
  document.getElementById('hint-box').innerText = q.hint;
  
  const ansDiv = document.getElementById('answers');
  ansDiv.innerHTML = '';
  q.a.forEach((ans, idx) => {
    const btn = document.createElement('button');
    btn.innerText = ans;
    btn.onclick = () => checkAnswer(idx);
    ansDiv.appendChild(btn);
  });
}

function checkAnswer(idx) {
  const q = quizData[currentIdx];
  if (idx === q.correct) {
    play16BitSE('correct');
    speak(q.voice);
    alert("CRITICAL HIT! モンスターを倒した！");
    currentIdx = (currentIdx + 1) % quizData.length;
    loadQuestion();
  } else {
    play16BitSE('wrong');
    speak("きゃっきゃっ！ダメージを受けたわ！");
    hp -= 20;
    document.getElementById('hp').innerText = hp;
    alert("痛恨の一撃を受けた！");
  }
}

function showHint() {
  document.getElementById('hint-box').style.display = 'block';
}

loadQuestion();
</script>
</body>
</html>
