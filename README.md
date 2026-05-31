<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>The Ultimate YouTuber Guide</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">
  <style>
    body { font-family: 'Segoe UI', system-ui, sans-serif; }
    .hero-bg {
      background: linear-gradient(135deg, #000000, #1a1a1a);
    }
    .card-hover {
      transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
    }
    .card-hover:hover {
      transform: translateY(-12px) scale(1.03);
      box-shadow: 0 25px 50px -12px rgb(249 115 22 / 0.3);
    }
    .fade-in {
      opacity: 0;
      transform: translateY(30px);
      transition: all 0.8s cubic-bezier(0.4, 0, 0.2, 1);
    }
    .fade-in.visible {
      opacity: 1;
      transform: translateY(0);
    }
  </style>
</head>
<body class="bg-zinc-950 text-white overflow-x-hidden">

  <!-- Navbar -->
  <nav class="fixed top-0 w-full bg-black/95 backdrop-blur-lg border-b border-zinc-800 z-50">
    <div class="max-w-7xl mx-auto px-6 py-5 flex justify-between items-center">
      <div class="flex items-center gap-3">
        <div class="w-9 h-9 bg-gradient-to-br from-orange-500 to-amber-500 rounded-2xl flex items-center justify-center text-3xl">
          🦁
        </div>
        <h1 class="text-3xl font-bold tracking-tighter">THE ULTIMATE<br><span class="text-orange-400 text-2xl">YOUTUBER GUIDE</span></h1>
      </div>
      <div class="hidden md:flex gap-8 text-sm font-medium">
        <a href="#metrics" class="hover:text-orange-400 transition-colors">Metrics</a>
        <a href="#retention" class="hover:text-orange-400 transition-colors">Retention</a>
        <a href="#structure" class="hover:text-orange-400 transition-colors">Structure</a>
        <button onclick="showQuiz()" class="bg-orange-500 hover:bg-orange-600 px-6 py-2 rounded-full font-semibold transition-all">
          Take Quiz
        </button>
      </div>
    </div>
  </nav>

  <!-- HERO -->
  <section class="hero-bg pt-32 pb-32 min-h-screen flex items-center">
    <div class="max-w-6xl mx-auto px-6 text-center">
      <div class="inline-flex items-center gap-2 bg-zinc-900 border border-orange-500/30 rounded-full px-6 py-2 mb-8">
        <i class="fas fa-fire text-orange-500 animate-pulse"></i>
        <span class="text-orange-400 font-medium">Inspired by MrBeast Production Guide</span>
      </div>
      <h1 class="text-6xl md:text-7xl font-bold tracking-tighter leading-none mb-6">THE ULTIMATE<br><span class="text-orange-400">YOUTUBER GUIDE</span></h1>
      <p class="text-2xl text-zinc-400 max-w-3xl mx-auto mb-12">Master YouTube Analytics & Virality with MrBeast's proven strategies</p>
      <button onclick="showQuiz()" class="bg-white text-black font-bold text-xl px-10 py-5 rounded-3xl hover:bg-orange-400 hover:text-white transition-all duration-300 flex items-center gap-3 mx-auto group">
        <span>START LEARNING →</span>
        <i class="fas fa-arrow-right group-hover:translate-x-2 transition"></i>
      </button>
    </div>
  </section>

  <!-- METRICS -->
  <section id="metrics" class="py-24 bg-zinc-900">
    <div class="max-w-6xl mx-auto px-6">
      <h2 class="text-5xl font-bold text-center mb-4">The 3 Metrics That Matter</h2>
      <p class="text-center text-zinc-400 text-xl mb-16">From Jimmy's 20,000+ hours studying virality</p>
      <div class="grid md:grid-cols-3 gap-8" id="metrics-grid"></div>
    </div>
  </section>

  <!-- RETENTION -->
  <section id="retention" class="py-24">
    <div class="max-w-6xl mx-auto px-6">
      <div class="grid md:grid-cols-2 gap-16 items-center">
        <div>
          <h2 class="text-5xl font-bold mb-8">Retention Graph Mastery</h2>
          <div class="space-y-8" id="retention-tips"></div>
        </div>
        <div class="bg-zinc-900 rounded-3xl p-8">
          <div class="text-center mb-4 text-zinc-400">Typical MrBeast Video Retention</div>
          <div class="h-80 flex items-end gap-2 px-8 relative bg-black/50 rounded-2xl overflow-hidden">
            <div class="w-full h-[88%] bg-gradient-to-t from-orange-500 to-amber-400 rounded-t"></div>
            <div class="w-full h-[72%] bg-gradient-to-t from-orange-500 to-amber-400 rounded-t"></div>
            <div class="w-full h-[65%] bg-gradient-to-t from-orange-500 to-amber-400 rounded-t"></div>
            <div class="w-full h-[60%] bg-gradient-to-t from-orange-500 to-amber-400 rounded-t"></div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- STRUCTURE -->
  <section id="structure" class="py-24 bg-zinc-900">
    <div class="max-w-6xl mx-auto px-6">
      <h2 class="text-5xl font-bold text-center mb-16">Video Structure Blueprint</h2>
      <div class="grid md:grid-cols-4 gap-6" id="structure-grid"></div>
    </div>
  </section>

  <!-- QUIZ -->
  <div id="quiz-page" class="hidden fixed inset-0 bg-zinc-950 z-[100] overflow-auto">
    <div class="max-w-2xl mx-auto py-20 px-6">
      <button onclick="hideQuiz()" class="mb-8 text-zinc-400 hover:text-white flex items-center gap-2">
        ← Back to Guide
      </button>
      
      <div class="text-center mb-12">
        <h2 class="text-5xl font-bold mb-4">MrBeast Analytics Quiz</h2>
        <p class="text-orange-400">Pass = $1,000 (in real life)</p>
      </div>
      <div id="quiz-content"></div>
      <div id="quiz-result" class="hidden text-center py-20">
        <h3 class="text-6xl font-bold mb-4" id="score"></h3>
        <p class="text-2xl text-zinc-400 mb-8" id="result-text"></p>
        <button onclick="restartQuiz()" class="bg-orange-500 px-10 py-4 rounded-2xl font-bold text-lg">
          Try Again
        </button>
      </div>
    </div>
  </div>

  <footer class="bg-black py-12 text-center text-zinc-500 text-sm">
    Fan-made educational project • Inspired by MrBeast's internal guide
  </footer>

  <script>
    // Data
    const metrics = [
      { icon: "fas fa-mouse-pointer", title: "CTR", subtitle: "Click-Through Rate", desc: "Percentage of people who click your thumbnail after seeing it.", example: '"I Spent 50 Hours in Ketchup" beats "I Spent 50 Hours in My Yard"' },
      { icon: "fas fa-clock", title: "AVD", subtitle: "Average View Duration", desc: "How long people actually watch. The #1 most important metric." },
      { icon: "fas fa-percentage", title: "AVP", subtitle: "Average View Percentage", desc: "What % of your video the audience watches on average." }
    ];

    const retentionTips = [
      { emoji: "📈", title: "Flat = Gold", desc: "Viewers are locked in." },
      { emoji: "📉", title: "Dips = Problems", desc: "Fix these moments immediately." },
      { emoji: "⚡", title: "Spikes = Wow Moments", desc: "Big spectacles and re-engagements." }
    ];

    const structure = [
      { time: "0:00", title: "First Minute", desc: "Match expectations. Hook hard. Most important 60 seconds." },
      { time: "1-3", title: "Crazy Progression", desc: "Compress time. Show multiple days fast." },
      { time: "3:00", title: "Re-engagement", desc: '"Only MrBeast can do this" moment.' },
      { time: "6:00+", title: "Back Half + Payoff", desc: "Keep them in the lull. Strong ending." }
    ];

    const quizQuestions = [
      { q: "What does CTR stand for?", a: ["Click-Through Rate", "Content Time Ratio", "Creator Trend Rating"], correct: 0 },
      { q: "Which minute of the video is the most important?", a: ["The first 60 seconds", "Minute 5-6", "The last 30 seconds"], correct: 0 },
      { q: "What is the 'Wow Factor'?", a: ["Doing things no other creator can do", "High production value", "Funny jokes"], correct: 0 },
      { q: "'Creativity Saves Money' — What does this mean?", a: ["Find cheaper but more creative solutions", "Spend as much money as possible", "Never use creativity"], correct: 0 },
      { q: "What should you do when scouting locations?", a: ["Video everything", "Just take mental notes", "Only take photos"], correct: 0 }
    ];

    let currentQuestion = 0;
    let score = 0;

    // Render Functions
    function renderMetrics() {
      document.getElementById('metrics-grid').innerHTML = metrics.map((m, i) => `
        <div class="bg-zinc-950 border border-zinc-800 rounded-3xl p-10 card-hover fade-in" style="animation-delay: ${i * 100}ms">
          <i class="${m.icon} text-5xl text-orange-500 mb-6"></i>
          <h3 class="text-4xl font-bold mb-2">${m.title}</h3>
          <p class="text-orange-400 text-2xl mb-4">${m.subtitle}</p>
          <p class="text-zinc-400">${m.desc}</p>
          ${m.example ? `<div class="mt-8 text-sm italic">${m.example}</div>` : ''}
        </div>
      `).join('');
    }

    function renderRetentionTips() {
      document.getElementById('retention-tips').innerHTML = retentionTips.map(t => `
        <div class="flex gap-6 fade-in">
          <span class="text-4xl">${t.emoji}</span>
          <div>
            <strong class="text-orange-400">${t.title}</strong>
            <p class="text-zinc-400">${t.desc}</p>
          </div>
        </div>
      `).join('');
    }

    function renderStructure() {
      document.getElementById('structure-grid').innerHTML = structure.map(s => `
        <div class="text-center p-8 bg-zinc-950 rounded-3xl card-hover fade-in">
          <div class="text-5xl font-mono text-orange-400 mb-4">${s.time}</div>
          <h4 class="font-bold text-xl">${s.title}</h4>
          <p class="text-sm text-zinc-400 mt-3">${s.desc}</p>
        </div>
      `).join('');
    }

    // Quiz Functions
    function showQuiz() {
      document.getElementById('quiz-page').classList.remove('hidden');
      currentQuestion = 0;
      score = 0;
      loadQuestion();
    }

    function hideQuiz() {
      document.getElementById('quiz-page').classList.add('hidden');
    }

    function loadQuestion() {
      const q = quizQuestions[currentQuestion];
      let html = `
        <div class="bg-zinc-900 rounded-3xl p-10">
          <p class="text-sm text-orange-400 mb-4">Question ${currentQuestion + 1} of ${quizQuestions.length}</p>
          <h3 class="text-3xl font-bold mb-8">${q.q}</h3>
          <div class="space-y-4">
      `;

      q.a.forEach((answer, i) => {
        html += `
          <button onclick="answerQuestion(${i})" class="w-full text-left p-6 rounded-2xl border border-zinc-700 hover:border-orange-500 hover:bg-zinc-800 transition-all text-lg">
            ${answer}
          </button>
        `;
      });

      html += `</div></div>`;
      document.getElementById('quiz-content').innerHTML = html;
    }

    function answerQuestion(selected) {
      if (selected === quizQuestions[currentQuestion].correct) score++;
      currentQuestion++;
      if (currentQuestion < quizQuestions.length) {
        loadQuestion();
      } else {
        showResult();
      }
    }

    function showResult() {
      const percentage = Math.round((score / quizQuestions.length) * 100);
      let message = percentage === 100 ? "You're ready to work at MrBeast! 🔥" :
                    percentage >= 80 ? "Excellent! You really understood the guide." :
                    percentage >= 60 ? "Good job! Keep studying." : "Review the guide and try again!";

      document.getElementById('quiz-content').classList.add('hidden');
      document.getElementById('quiz-result').classList.remove('hidden');
      document.getElementById('score').textContent = `${percentage}%`;
      document.getElementById('result-text').textContent = message;
    }

    function restartQuiz() {
      document.getElementById('quiz-content').classList.remove('hidden');
      document.getElementById('quiz-result').classList.add('hidden');
      currentQuestion = 0;
      score = 0;
      loadQuestion();
    }

    // Scroll Animation
    function animateOnScroll() {
      const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
          if (entry.isIntersecting) entry.target.classList.add('visible');
        });
      }, { threshold: 0.1 });

      document.querySelectorAll('.fade-in').forEach(el => observer.observe(el));
    }

    // Initialize
    window.onload = () => {
      renderMetrics();
      renderRetentionTips();
      renderStructure();
      animateOnScroll();
    };
  </script>
</body>
</html>
