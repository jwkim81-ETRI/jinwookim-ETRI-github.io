[index.html](https://github.com/user-attachments/files/22055846/index.html)
<!doctype html>
<html lang="ko" class="scroll-smooth">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>Jinwoo Kim — Autonomous Driving · VLM · LLM</title>
    <meta name="description" content="자율주행 · VLM · LLM · E2E R&D — 논문, 특허, 프로젝트와 관심 분야를 소개합니다." />

    <!-- Open Graph / Twitter -->
    <meta property="og:title" content="Jinwoo Kim — Autonomous Driving · VLM · LLM" />
    <meta property="og:description" content="자율주행 · VLM · LLM · E2E R&D — 논문, 특허, 프로젝트와 관심 분야를 소개합니다." />
    <meta property="og:type" content="website" />

    <!-- Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@300;400;600;700&family=Inter:wght@400;600;700&family=JetBrains+Mono:wght@400;600&display=swap" rel="stylesheet" />

    <!-- Tailwind (CDN) -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
      tailwind.config = {
        theme: {
          extend: {
            fontFamily: {
              sans: ["Inter", "Noto Sans KR", "system-ui", "-apple-system", "Segoe UI", "Roboto", "Noto Sans", "Ubuntu", "Cantarell", "Helvetica Neue", "Arial", "sans-serif"],
              mono: ["JetBrains Mono", "ui-monospace", "SFMono-Regular", "Menlo", "monospace"],
            }
          }
        }
      };
    </script>

    <style>
      :focus-visible { outline: 2px solid #0ea5e9; outline-offset: 2px; }
      .cv dt{min-width:8rem}
    </style>

    <!-- Dark mode bootstrap -->
    <script>
      (function() {
        const stored = localStorage.getItem('theme');
        if (stored === 'dark' || (!stored && window.matchMedia('(prefers-color-scheme: dark)').matches)) {
          document.documentElement.classList.add('dark');
        }
      })();
    </script>
  </head>
  <body class="font-sans text-slate-800 dark:text-slate-100 bg-white dark:bg-slate-950 min-h-screen">
    <!-- Top bar -->
    <header class="sticky top-0 z-50 backdrop-blur bg-white/80 dark:bg-slate-950/70 border-b border-slate-200/60 dark:border-slate-800">
      <div class="max-w-5xl mx-auto px-4 py-3 flex items-center justify-between">
        <a href="#home" class="font-bold">Jinwoo Kim</a>
        <nav class="hidden sm:flex gap-6 text-sm">
          <a href="#about" class="hover:text-sky-600">About</a>
          <a href="#interests" class="hover:text-sky-600">Interests</a>
          <a href="#pubs" class="hover:text-sky-600">Publications</a>
          <a href="#patents" class="hover:text-sky-600">Patents</a>
          <a href="#projects" class="hover:text-sky-600">Projects</a>
          <a href="#service" class="hover:text-sky-600">Service</a>
          <a href="#contact" class="hover:text-sky-600">Contact</a>
        </nav>
        <button id="themeToggle" class="rounded-lg border border-slate-300 dark:border-slate-700 px-3 py-1.5 text-sm">🌗</button>
      </div>
    </header>

    <!-- Hero / header block like an academic homepage -->
    <section id="home" class="max-w-5xl mx-auto px-4 py-10">
      <div class="grid md:grid-cols-[1fr,220px] gap-8 items-start">
        <div>
          <h1 class="text-3xl md:text-4xl font-bold">Jinwoo Kim</h1>
          <p class="mt-2 text-slate-600 dark:text-slate-300">Autonomous Driving · Vision-Language Models · Large Language Models</p>
          <p class="mt-4 leading-relaxed">자율주행을 위한 <strong>VLM 기반 엔드투엔드 지능</strong>에 집중합니다. 단일 전방 영상에서 위험 요소(공사구간, 불법 주정차 등)를 인지하고 <em>회피·감속·정지·경로생성</em>까지 연결되는 <strong>multi‑stage reasoning</strong>과 <strong>실시간 추론</strong>을 연구합니다.</p>
          <div class="mt-4 flex flex-wrap gap-3 text-sm">
            <a class="px-3 py-1.5 rounded border border-slate-300 dark:border-slate-700 hover:bg-slate-50 dark:hover:bg-slate-800" href="#pubs">Publications</a>
            <a class="px-3 py-1.5 rounded bg-sky-600 text-white hover:bg-sky-700" href="#projects">Projects</a>
          </div>
        </div>
        <div class="justify-self-end w-[180px] h-[180px] rounded-2xl bg-slate-100 dark:bg-slate-900 border border-slate-200 dark:border-slate-800 flex items-center justify-center text-slate-400">photo</div>
      </div>
    </section>

    <!-- Interests -->
    <section id="interests" class="max-w-5xl mx-auto px-4 py-8 border-t border-slate-200/60 dark:border-slate-800">
      <h2 class="text-2xl font-bold">Research Interests</h2>
      <ul class="mt-3 grid sm:grid-cols-2 gap-x-8 gap-y-2 list-disc ml-6">
        <li>Vision-Language Planning (VLP), End-to-End Autonomous Driving (E2E AD)</li>
        <li>Robustness under weather/night/OOD, Uncertainty</li>
        <li>Real-time inference, efficient CNN/VLM hybrid backbones</li>
        <li>Multi-stage reasoning, memory, selective routing</li>
        <li>HD-map aware action reasoning, lane constraints</li>
      </ul>
    </section>

    <!-- Publications -->
    <section id="pubs" class="max-w-5xl mx-auto px-4 py-8 border-t border-slate-200/60 dark:border-slate-800">
      <h2 class="text-2xl font-bold">Publications</h2>
      <ol class="mt-4 space-y-4 list-decimal ml-6">
        <li>
          <span class="font-semibold">SADWA: Fine-Grained Weather Awareness with Vision-Language Models for Real-Time Autonomous Driving</span>.
          <span class="text-slate-600 dark:text-slate-400">(2025) </span>
          <span class="text-sm">MobileCLIP을 SADWA 데이터셋으로 파인튜닝하여 악천후 인지와 주행 전략 생성을 수행.</span>
          <div class="text-sm mt-1 flex gap-3">
            <a class="text-sky-600 hover:underline" href="#">PDF</a>
            <a class="text-sky-600 hover:underline" href="#">arXiv</a>
            <a class="text-sky-600 hover:underline" href="#">Code</a>
          </div>
        </li>
        <li>
          <span class="font-semibold">VL‑iRoSA: Vision‑Language for Rapid Situation‑aware Planning</span>.
          <span class="text-sm">CDWSP 방식으로 빠르고 확실한 planning 가이드를 제공, 시뮬레이션 비교 포함.</span>
          <div class="text-sm mt-1 flex gap-3">
            <a class="text-sky-600 hover:underline" href="#">PDF</a>
            <a class="text-sky-600 hover:underline" href="#">Code</a>
          </div>
        </li>
      </ol>
      <p class="text-sm text-slate-500 mt-3">※ LinkedIn에 있는 전체 목록은 순차 반영 예정.</p>
    </section>

    <!-- Patents -->
    <section id="patents" class="max-w-5xl mx-auto px-4 py-8 border-t border-slate-200/60 dark:border-slate-800">
      <h2 class="text-2xl font-bold">Patents</h2>
      <ul class="mt-3 list-disc ml-6 space-y-2">
        <li class="text-sm">(예시) 자율주행 상황 인지 및 경로 생성 장치/방법 — 출원/등록 정보 기입</li>
      </ul>
    </section>

    <!-- Projects -->
    <section id="projects" class="max-w-5xl mx-auto px-4 py-8 border-t border-slate-200/60 dark:border-slate-800">
      <h2 class="text-2xl font-bold">Projects</h2>
      <div class="mt-5 grid md:grid-cols-3 gap-6">
        <article class="rounded-xl border border-slate-200 dark:border-slate-800 p-4">
          <h3 class="font-semibold">E2E Weather‑Robust Driving</h3>
          <p class="text-sm mt-1 text-slate-600 dark:text-slate-400">악천후/야간에서도 견고한 주행 전략 생성.</p>
          <div class="mt-2 text-[11px] flex flex-wrap gap-2">
            <span class="px-2 py-0.5 rounded bg-slate-100 dark:bg-slate-800">MobileCLIP</span>
            <span class="px-2 py-0.5 rounded bg-slate-100 dark:bg-slate-800">CNN+VLM</span>
            <span class="px-2 py-0.5 rounded bg-slate-100 dark:bg-slate-800">Realtime</span>
          </div>
        </article>
        <article class="rounded-xl border border-slate-200 dark:border-slate-800 p-4">
          <h3 class="font-semibold">Selective Routing Planner</h3>
          <p class="text-sm mt-1 text-slate-600 dark:text-slate-400">상황별 라우팅으로 레이턴시 절감.</p>
        </article>
        <article class="rounded-xl border border-slate-200 dark:border-slate-800 p-4">
          <h3 class="font-semibold">Map‑aware Action Reasoner</h3>
          <p class="text-sm mt-1 text-slate-600 dark:text-slate-400">정밀지도·차로 제약을 반영한 행동 추론.</p>
        </article>
      </div>
    </section>

    <!-- Service / Talks (optional) -->
    <section id="service" class="max-w-5xl mx-auto px-4 py-8 border-t border-slate-200/60 dark:border-slate-800">
      <h2 class="text-2xl font-bold">Professional Service</h2>
      <ul class="mt-3 list-disc ml-6 space-y-2 text-sm">
        <li>Conference/Journal Review: (예) ICCV, ECCV, ICRA — 연도 기입</li>
        <li>Invited Talks: (예) VLM for E2E Autonomous Driving</li>
      </ul>
    </section>

    <!-- Contact -->
    <section id="contact" class="max-w-5xl mx-auto px-4 py-8 border-t border-slate-200/60 dark:border-slate-800">
      <h2 class="text-2xl font-bold">Contact</h2>
      <ul class="mt-3 space-y-2">
        <li>🐙 GitHub: <a class="text-sky-600 hover:underline" href="https://github.com/jinwookim-ETRI">github.com/jinwookim-ETRI</a></li>
        <li>🔗 LinkedIn: <a class="text-sky-600 hover:underline" href="https://www.linkedin.com/in/jinwoo-kim-836a9b56/">linkedin.com/in/jinwoo-kim-836a9b56</a></li>
        <li class="text-sm text-slate-500">※ 이메일은 비공개(no‑reply) 정책을 사용합니다.</li>
      </ul>
    </section>

    <footer class="max-w-5xl mx-auto px-4 py-10 text-sm text-slate-500">
      <div class="flex items-center justify-between">
        <span>© <span id="year"></span> Jinwoo Kim. All rights reserved.</span>
        <a href="#home" class="hover:text-sky-600">맨 위로 ↑</a>
      </div>
    </footer>
[index.html](https://github.com/user-attachments/files/22055990/index.html)
<!doctype html>
<html lang="ko" class="scroll-smooth">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>Jinwoo Kim — Autonomous Driving Research Development</title>
    <meta name="description" content="Autonomous Driving Research Development · VLM · LLM · E2E R&D — 논문, 특허, 프로젝트와 연구 동영상을 소개합니다." />

    <!-- Fonts & Tailwind -->
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@300;400;600;700&family=Inter:wght@400;600;700&display=swap" rel="stylesheet" />
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
      tailwind.config = { theme: { extend: { fontFamily: { sans: ["Inter","Noto Sans KR","system-ui"] } } } };
    </script>
    <style>:focus-visible{outline:2px solid #0ea5e9;outline-offset:2px}</style>
  </head>
  <body class="font-sans text-slate-800 dark:text-slate-100 bg-white dark:bg-slate-950 min-h-screen">
    <header class="sticky top-0 z-50 backdrop-blur bg-white/80 dark:bg-slate-950/70 border-b border-slate-200/60 dark:border-slate-800">
      <div class="max-w-5xl mx-auto px-4 py-3 flex items-center justify-between">
        <a href="#home" class="font-bold">Jinwoo Kim</a>
        <nav class="hidden sm:flex gap-6 text-sm">
          <a href="#about">About</a>
          <a href="#interests">Interests</a>
          <a href="#pubs">Publications</a>
          <a href="#patents">Patents</a>
          <a href="#projects">Projects</a>
          <a href="#videos">연구 결과 동영상</a>
          <a href="#contact">Contact</a>
        </nav>
        <button id="themeToggle" class="rounded-lg border border-slate-300 dark:border-slate-700 px-3 py-1.5 text-sm">🌗</button>
      </div>
    </header>

    <section id="home" class="max-w-5xl mx-auto px-4 py-10">
      <h1 class="text-3xl md:text-4xl font-bold">Autonomous Driving Research Development</h1>
      <p class="mt-3 text-slate-600 dark:text-slate-300">Autonomous Driving · Vision-Language Models · Large Language Models</p>
    </section>

    <!-- Interests -->
    <section id="interests" class="max-w-5xl mx-auto px-4 py-8 border-t border-slate-200/60 dark:border-slate-800">
      <h2 class="text-2xl font-bold">Research Interests</h2>
      <ul class="mt-3 list-disc ml-6 space-y-1">
        <li>Vision-Language Planning, End-to-End Autonomous Driving</li>
        <li>Robustness under weather/night/OOD</li>
        <li>Real-time inference and efficient backbones</li>
        <li>Multi-stage reasoning, memory, selective routing</li>
        <li>HD-map aware action reasoning</li>
      </ul>
    </section>

    <!-- Publications -->
    <section id="pubs" class="max-w-5xl mx-auto px-4 py-8 border-t border-slate-200/60 dark:border-slate-800">
      <h2 class="text-2xl font-bold">Publications</h2>
      <ol class="mt-4 space-y-4 list-decimal ml-6">
        <li>
          <span class="font-semibold">RoSA Dataset: Road construct zone Segmentation for Autonomous Driving</span> — <span class="text-slate-600 dark:text-slate-400">ECCV Workshop, 2024-09-30</span>
          <div class="text-sm mt-1 flex gap-3">
            <a class="text-sky-600 hover:underline" href="https://www.springerprofessional.de/en/rosa-dataset-road-construct-zone-segmentation-for-autonomous-dri/51030158">[Publisher]</a>
          </div>
        </li>
        <li>
          <span class="font-semibold">Multi-sensor-based Detection and Tracking of Moving Objects for Relative Position Estimation in Autonomous Driving Conditions</span> — <span class="text-slate-600 dark:text-slate-400">Springer, 2020-10-01</span>
          <div class="text-sm mt-1 flex gap-3">
            <a class="text-sky-600 hover:underline" href="https://link.springer.com/article/10.1007/s11227-019-02811-y">[Publisher]</a>
          </div>
        </li>
        <li>
          <span class="font-semibold">Fusion of driver-information based driver status recognition for co-pilot system</span> — <span class="text-slate-600 dark:text-slate-400">IEEE Intelligent Vehicles Symposium, 2016-06-21</span>
          <div class="text-sm mt-1 flex gap-3">
            <a class="text-sky-600 hover:underline" href="https://ieeexplore.ieee.org/document/7535573">[IEEE Xplore]</a>
          </div>
        </li>
        <li>
          <span class="font-semibold">Multimodal Interface Based on Novel HMI UI/UX for In-Vehicle Infotainment System</span> — <span class="text-slate-600 dark:text-slate-400">ETRI Journal, 2015-01-01</span>
          <div class="text-sm mt-1 flex gap-3">
            <a class="text-sky-600 hover:underline" href="https://onlinelibrary.wiley.com/doi/full/10.4218/etrij.15.0114.0076">[Wiley/ETRI Journal]</a>
          </div>
        </li>
      </ol>
    </section>

    <!-- Patents -->
    <section id="patents" class="max-w-5xl mx-auto px-4 py-8 border-t border-slate-200/60 dark:border-slate-800">
      <h2 class="text-2xl font-bold">Patents</h2>
      <ul class="list-disc ml-6 mt-4 space-y-2 text-sm">
        <li><span class="font-medium">SYSTEM AND METHOD FOR FUSION RECOGNITION USING ACTIVE STICK FILTER</span> — US <strong>11790555</strong>, 2023-10-17</li>
        <li><span class="font-medium">THE APPARATUS AND METHOD FOR DRIVER STATUS RECOGNITION BASED ON DRIVING STATUS DECISION INFORMATION</span> — JP <strong>7154959</strong>, 2022-10-07</li>
        <li><span class="font-medium">APPARATUS AND METHOD OF LEARNING POSE OF MOVING OBJECT</span> — US <strong>10789717</strong>, 2020-09-29</li>
        <li><span class="font-medium">USER INTENTION ANALYSIS APPARATUS AND METHOD BASED ON IMAGE INFORMATION OF THREE-DIMENSIONAL SPACE</span> — US <strong>9886623</strong>, 2018-02-06</li>
        <li><span class="font-medium">SYSTEM AND METHOD FOR LEARNING DRIVING INFORMATION IN VEHICLE</span> — US <strong>9485474</strong>, 2016-11-01</li>
        <li><span class="font-medium">METHOD AND APPARATUS FOR ANALYZING CONCENTRATION LEVEL OF DRIVER</span> — US <strong>9355546</strong>, 2016-05-31</li>
        <li><span class="font-medium">AUGMENTED REALITY DISPLAY SYSTEM AND METHOD FOR VEHICLE</span> — US <strong>9075563</strong>, 2015-07-07</li>
      </ul>
    </section>

    <!-- Projects -->
    <section id="projects" class="max-w-5xl mx-auto px-4 py-8 border-t border-slate-200/60 dark:border-slate-800">
      <h2 class="text-2xl font-bold">Projects</h2>
      <ul class="list-disc ml-6 mt-3 space-y-1">
        <li>E2E Weather-Robust Driving</li>
        <li>Selective Routing Planner</li>
        <li>Map-aware Action Reasoner</li>
      </ul>
    </section>

    <!-- Research Videos -->
    <section id="videos" class="max-w-5xl mx-auto px-4 py-8 border-t border-slate-200/60 dark:border-slate-800">
      <h2 class="text-2xl font-bold">연구 결과 동영상</h2>
      <p class="mt-3 text-slate-600 dark:text-slate-300">LinkedIn에 게시한 연구 시연 동영상 모음입니다.</p>
      <ul class="list-disc ml-6 mt-3 space-y-2">
        <li><a href="https://www.linkedin.com/in/jinwoo-kim-836a9b56/details/featured/" class="text-sky-600 hover:underline">전체 동영상 보기 (LinkedIn Featured)</a></li>
      </ul>
    </section>

    <!-- Contact -->
    <section id="contact" class="max-w-5xl mx-auto px-4 py-8 border-t border-slate-200/60 dark:border-slate-800">
      <h2 class="text-2xl font-bold">Contact</h2>
      <ul class="mt-3 space-y-2">
        <li>🐙 GitHub: <a class="text-sky-600 hover:underline" href="https://github.com/jinwookim-ETRI">github.com/jinwookim-ETRI</a></li>
        <li>🔗 LinkedIn: <a class="text-sky-600 hover:underline" href="https://www.linkedin.com/in/jinwoo-kim-836a9b56/">linkedin.com/in/jinwoo-kim-836a9b56</a></li>
      </ul>
    </section>

    <footer class="max-w-5xl mx-auto px-4 py-10 text-sm text-slate-500">
      <div class="flex items-center justify-between">
        <span>© <span id="year"></span> Autonomous Driving Research Development</span>
        <a href="#home" class="hover:text-sky-600">맨 위로 ↑</a>
      </div>
    </footer>

    <script>
      document.getElementById('year').textContent = new Date().getFullYear();
      document.getElementById('themeToggle')?.addEventListener('click', () => {
        const d = document.documentElement.classList.toggle('dark');
        localStorage.setItem('theme', d ? 'dark' : 'light');
      });
    </script>
  </body>
</html>

    <script>
      document.getElementById('year').textContent = new Date().getFullYear();
      document.getElementById('themeToggle')?.addEventListener('click', () => {
        const d = document.documentElement.classList.toggle('dark');
        localStorage.setItem('theme', d ? 'dark' : 'light');
      });
    </script>
  </body>
</html>
