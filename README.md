<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>숨을 고르고, 나를 만나는 시간 | 김정연</title>
  <!-- Tailwind CSS CDN -->
  <script src="https://cdn.tailwindcss.com"></script>
  <!-- 구글 폰트: 배달의민족 도현 & 본고딕 (Pretendard 스타일의 굵직한 한글 폰트를 위해 Noto Sans KR 고중량 세팅) -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Do+Hyeon&family=Noto+Sans+KR:wght@500;700;900&display=swap" rel="stylesheet">
  
  <script>
    tailwind.config = {
      theme: {
        extend: {
          fontFamily: {
            dohyeon: ['"Do Hyeon"', 'sans-serif'],
            sans: ['"Noto Sans KR"', 'sans-serif'],
          },
          colors: {
            brand: {
              light: '#E0F2FE', // 스카이블루 연한톤
              DEFAULT: '#0284C7', // 메인 스카이블루
              dark: '#0369A1', // 딥블루
              ocean: '#0C4A6E', // 심해블루
              pool: '#bae6fd' // 풀장 물빛
            }
          }
        }
      }
    }
  </script>
  <style>
    /* 스크롤바 커스텀 */
    ::-webkit-scrollbar {
      width: 10px;
    }
    ::-webkit-scrollbar-track {
      background: #e0f2fe;
    }
    ::-webkit-scrollbar-thumb {
      background: #0284C7;
      border-radius: 5px;
      border: 2px solid #e0f2fe;
    }

    /* 찰랑거리는 물결 일렁임 애니메이션 (특정 구역에서만 포인트 요소로 사용) */
    @keyframes ripple {
      0%, 100% { transform: translateY(0) scale(1) rotate(0deg); opacity: 0.2; }
      50% { transform: translateY(-8px) scale(1.03) rotate(1deg); opacity: 0.35; }
    }
    .water-ripple {
      animation: ripple 6s ease-in-out infinite;
    }

    @keyframes pulse-slow {
      0%, 100% { opacity: 0.3; transform: scale(1); }
      50% { opacity: 0.6; transform: scale(1.08); }
    }
    .pool-light-reflect {
      animation: pulse-slow 4s ease-in-out infinite;
    }

    /* 쿠키 흔들리는 효과 */
    @keyframes wiggle {
      0%, 100% { transform: rotate(0deg); }
      25% { transform: rotate(-8deg); }
      75% { transform: rotate(8deg); }
    }
    .wiggle-hover:hover {
      animation: wiggle 0.4s ease-in-out infinite;
    }
  </style>
</head>
<body class="bg-gradient-to-b from-[#f0f9ff] via-[#ffffff] to-[#f0f9ff] text-slate-900 font-sans overflow-x-hidden selection:bg-brand selection:text-white min-h-screen relative">

  <!-- 네비게이션 바 (가시성 고정 강화) -->
  <nav class="fixed top-0 left-0 w-full bg-white/95 backdrop-blur-md z-50 border-b-4 border-brand shadow-md">
    <div class="max-w-6xl mx-auto px-6 py-4 flex justify-between items-center">
      <a href="#" class="font-dohyeon text-3xl text-brand tracking-wider drop-shadow-sm">KIM JEONG YEON</a>
      <div class="hidden md:flex space-x-8 font-extrabold text-slate-800 text-lg">
        <a href="#about" class="hover:text-brand transition-colors relative group">
          나의 이야기
          <span class="absolute bottom-0 left-0 w-full h-1 bg-brand scale-x-0 group-hover:scale-x-100 transition-transform"></span>
        </a>
        <a href="#strengths" class="hover:text-brand transition-colors relative group">
          체력과 신뢰
          <span class="absolute bottom-0 left-0 w-full h-1 bg-brand scale-x-0 group-hover:scale-x-100 transition-transform"></span>
        </a>
        <a href="#exercise-recommender" class="hover:text-brand transition-colors relative group">
          기분 맞춤 운동 추천
          <span class="absolute bottom-0 left-0 w-full h-1 bg-brand scale-x-0 group-hover:scale-x-100 transition-transform"></span>
        </a>
        <a href="#mind-pool" class="hover:text-brand transition-colors relative group">
          생각 비우기 방
          <span class="absolute bottom-0 left-0 w-full h-1 bg-brand scale-x-0 group-hover:scale-x-100 transition-transform"></span>
        </a>
      </div>
      <a href="#mind-pool" class="font-dohyeon text-lg bg-brand text-white px-6 py-2.5 rounded-full hover:bg-brand-dark transition-all transform hover:scale-105 shadow-md shadow-sky-300">
        스트레스 비우기 🏊‍♀️
      </a>
    </div>
  </nav>

  <!-- 1. 히어로 섹션 (Hero) -->
  <header class="relative min-h-screen flex items-center justify-center pt-24 overflow-hidden">
    <!-- 물 밑 반사광 데코 효과 (단백한 배경 위 포인트 비주얼) -->
    <div class="absolute inset-0 bg-gradient-to-b from-sky-200/30 via-sky-100/10 to-transparent pointer-events-none"></div>
    <div class="absolute top-1/3 left-1/4 w-96 h-96 bg-cyan-200/30 rounded-full blur-3xl pool-light-reflect pointer-events-none"></div>
    <div class="absolute bottom-1/4 right-1/4 w-[500px] h-[500px] bg-sky-300/20 rounded-full blur-3xl pool-light-reflect pointer-events-none"></div>

    <div class="max-w-5xl mx-auto px-6 text-center z-10 py-12">
      <!-- 서브 뱃지 -->
      <span class="inline-block bg-slate-900 border-2 border-brand text-sky-300 font-extrabold px-6 py-2 rounded-full text-sm md:text-base mb-8 uppercase tracking-widest shadow-md">
        🏊‍♀️ PHYSICAL & MENTAL SWIMMING POOL
      </span>
      
      <!-- 캐치프레이즈 메인 타이틀 (가시성 극대화) -->
      <h1 class="font-dohyeon text-5xl md:text-8xl text-slate-900 leading-tight mb-8 drop-shadow-[0_2px_4px_rgba(0,0,0,0.1)]">
        몸을 움직여 머리를 비울 때,<br>
        비로소 <span class="text-brand relative inline-block">진짜 내가<span class="absolute bottom-2 left-0 w-full h-5 bg-brand/25 -z-10"></span></span> 보입니다.
      </h1>

      <p class="text-xl md:text-2xl text-slate-800 max-w-4xl mx-auto leading-relaxed mb-12 font-bold bg-white/90 backdrop-blur-sm p-6 rounded-2xl border-2 border-sky-100 shadow-md">
        안녕하세요! 매일 좋아하는 한 가지 운동으로 스트레스를 산뜻하게 비워내고, <br class="hidden md:block">
        탄탄해진 체력을 바탕으로 주위 사람들에게 <span class="text-brand-dark font-extrabold underline decoration-brand decoration-4">맑은 에너지와 흔들리지 않는 중심</span>을 나누는 <strong class="font-black text-slate-900">김정연</strong>입니다.
      </p>

      <div class="flex flex-col sm:flex-row gap-5 justify-center">
        <a href="#about" class="font-dohyeon text-xl bg-slate-900 text-white px-10 py-5 rounded-2xl hover:bg-slate-800 transition-all transform hover:-translate-y-1 shadow-lg shadow-slate-400">
          김정연 스토리 읽어보기
        </a>
        <a href="#mind-pool" class="font-dohyeon text-xl bg-brand text-white border-2 border-brand-dark px-10 py-5 rounded-2xl hover:bg-brand-dark transition-all transform hover:-translate-y-1 shadow-lg shadow-sky-300">
          물속에 고민 던지기 💦
        </a>
      </div>
    </div>
  </header>

  <!-- 2. 소개 섹션 (Intro / Timeline) -->
  <section id="about" class="py-24 relative">
    <div class="max-w-5xl mx-auto px-6 relative z-10">
      
      <!-- 섹션 헤더 -->
      <div class="text-center mb-16">
        <h2 class="font-dohyeon text-4xl md:text-6xl text-slate-900 mb-4 drop-shadow-sm">나와 친해지게 해준 움직임들</h2>
        <p class="text-slate-800 font-extrabold text-lg md:text-xl max-w-2xl mx-auto bg-white/90 p-3 rounded-lg inline-block border border-sky-100 shadow-sm">
          🌊 머리를 비우고 스스로에게 오롯이 집중하게 해 준 세 가지 운동의 타임라인입니다.
        </p>
      </div>

      <!-- 인터랙티브 탭 메뉴 구조 -->
      <div class="bg-white rounded-3xl p-8 md:p-12 border-4 border-brand shadow-xl relative overflow-hidden">
        <!-- 수영장 수면 일렁임 그래픽 효과 내부 적용 -->
        <div class="absolute inset-0 bg-gradient-to-b from-sky-100/20 to-transparent pointer-events-none"></div>
        
        <div class="grid grid-cols-3 gap-2 md:gap-4 mb-10 bg-slate-100 p-2 rounded-2xl relative z-10">
          <button onclick="switchTab('running')" id="tab-running" class="tab-btn active py-4 px-2 md:px-6 rounded-xl font-dohyeon text-base md:text-2xl transition-all focus:outline-none bg-brand text-white shadow-md">
            🏃‍♀️ START : 러닝
          </button>
          <button onclick="switchTab('stair')" id="tab-stair" class="tab-btn py-4 px-2 md:px-6 rounded-xl font-dohyeon text-base md:text-2xl transition-all focus:outline-none text-slate-800 hover:text-brand">
            🧗‍♀️ PEAK : 천국의 계단
          </button>
          <button onclick="switchTab('swim')" id="tab-swim" class="tab-btn py-4 px-2 md:px-6 rounded-xl font-dohyeon text-base md:text-2xl transition-all focus:outline-none text-slate-800 hover:text-brand">
            🏊‍♀️ PRESENT : 수영
          </button>
        </div>

        <!-- 탭 내용 1: 러닝 -->
        <div id="content-running" class="tab-content block fade-in-up relative z-10">
          <div class="grid md:grid-cols-2 gap-8 items-center">
            <div class="space-y-5">
              <span class="inline-block bg-slate-900 text-sky-300 font-extrabold px-4 py-1.5 rounded-full text-sm">체력 증진의 소중한 시작</span>
              <h3 class="font-dohyeon text-3xl md:text-4xl text-slate-900 leading-snug">"운동에 재미를 붙이게 해준 고마운 첫 발자국"</h3>
              <p class="text-slate-800 font-bold leading-relaxed text-base md:text-lg">
                머릿속이 수많은 생각과 걱정으로 엉켜 옴짝달싹할 수 없을 때, 무작정 운동화 끈을 묶고 밖으로 나갔습니다. 숨이 턱 끝까지 찰 만큼 전력으로 달리며, 마침내 복잡하던 잡념들이 맑게 개어가는 정신적 쾌감을 발견했습니다.
              </p>
              <div class="bg-sky-50 p-5 rounded-2xl border-2 border-brand-light text-slate-900 font-extrabold text-sm md:text-base">
                💡 <strong class="text-brand text-lg">Jeongyeon's Insight:</strong> 일상이 복잡할 때 해답은 단순합니다. 그저 한 걸음 먼저 내디디며 움직이는 것뿐입니다.
              </div>
            </div>
            <div class="bg-gradient-to-br from-sky-400 via-sky-600 to-brand-dark h-80 rounded-2xl flex flex-col items-center justify-center text-white p-8 text-center shadow-lg relative overflow-hidden">
              <div class="absolute inset-0 bg-white/10 opacity-20 pointer-events-none"></div>
              <span class="text-6xl mb-4 animate-bounce">🏃‍♀️</span>
              <p class="font-dohyeon text-2xl md:text-3xl">"달릴 때 비로소 잡념이 흘러간다"</p>
              <p class="text-sm md:text-base mt-2 opacity-90 font-bold">러닝이 전수해준 멘탈 리셋의 위력</p>
            </div>
          </div>
        </div>

        <!-- 탭 내용 2: 천국의 계단 -->
        <div id="content-stair" class="tab-content hidden relative z-10">
          <div class="grid md:grid-cols-2 gap-8 items-center">
            <div class="space-y-5">
              <span class="inline-block bg-slate-900 text-sky-300 font-extrabold px-4 py-1.5 rounded-full text-sm">드라마틱한 성장과 끈기</span>
              <h3 class="font-dohyeon text-3xl md:text-4xl text-slate-900 leading-snug">"가장 강력한 효율, 매일 한 계단씩 단단해지기"</h3>
              <p class="text-slate-800 font-bold leading-relaxed text-base md:text-lg">
                체력이 극대화되는 것을 눈으로 확인하게 해 준 고마운 파트너는 '천국의 계단(클라이밀)'이었습니다. 계단을 꾹꾹 디디며 올라가는 단순하고 묵직한 고강도 노동은 복잡한 뇌를 비우고 심플한 멘탈을 쟁취하는 지름길이었습니다.
              </p>
              <div class="bg-sky-50 p-5 rounded-2xl border-2 border-brand-light text-slate-900 font-extrabold text-sm md:text-base">
                💡 <strong class="text-brand text-lg">Jeongyeon's Insight:</strong> 아찔하게 높은 경사처럼 버겁게 느껴지는 일상의 장벽도, 하나씩 우직하게 디디다 보면 반드시 극복해 냅니다.
              </div>
            </div>
            <div class="bg-gradient-to-br from-sky-500 via-blue-600 to-brand-ocean h-80 rounded-2xl flex flex-col items-center justify-center text-white p-8 text-center shadow-lg relative overflow-hidden">
              <span class="text-6xl mb-4 animate-bounce">🧗‍♀️</span>
              <p class="font-dohyeon text-2xl md:text-3xl">"계단을 정복하며 기른 단단한 신체"</p>
              <p class="text-sm md:text-base mt-2 opacity-90 font-bold">성실한 움직임이 가져온 일상의 든든함</p>
            </div>
          </div>
        </div>

        <!-- 탭 내용 3: 수영 -->
        <div id="content-swim" class="tab-content hidden relative z-10">
          <div class="grid md:grid-cols-2 gap-8 items-center">
            <div class="space-y-5">
              <span class="inline-block bg-slate-900 text-sky-300 font-extrabold px-4 py-1.5 rounded-full text-sm">완벽한 평온과 집중</span>
              <h3 class="font-dohyeon text-3xl md:text-4xl text-slate-900 leading-snug">"고요한 물밑에서 진정한 나와 대면하는 시간"</h3>
              <p class="text-slate-800 font-bold leading-relaxed text-base md:text-lg">
                요즘 저의 일상을 가장 건강하게 지켜주는 메인 운동은 '수영'입니다. 깊고 투명한 풀 속에 잠수하면 물소리와 오직 나의 숨소리만 남습니다. 스마트폰 알림도 소음도 존재하지 않는 수중은 나 자신과 오롯이 교감하기 위한 완벽한 성지입니다.
              </p>
              <div class="bg-sky-50 p-5 rounded-2xl border-2 border-brand-light text-slate-900 font-extrabold text-sm md:text-base">
                💡 <strong class="text-brand text-lg">Jeongyeon's Insight:</strong> 일정한 호흡으로 차분히 물길을 가르는 규칙적인 감각은, 물 밖의 삶 속에서도 언제나 저를 지탱해 주는 여유를 줍니다.
              </div>
            </div>
            <div class="bg-gradient-to-br from-blue-400 via-brand to-brand-ocean h-80 rounded-2xl flex flex-col items-center justify-center text-white p-8 text-center shadow-lg relative overflow-hidden">
              <div class="absolute inset-0 bg-[radial-gradient(ellipse_at_top,_var(--tw-gradient-stops))] from-sky-200/30 via-transparent to-transparent water-ripple pointer-events-none"></div>
              <span class="text-6xl mb-4 animate-bounce">🏊‍♀️</span>
              <p class="font-dohyeon text-2xl md:text-3xl">"나의 폐활량만큼 정직하게 나아간다"</p>
              <p class="text-sm md:text-base mt-2 opacity-90 font-bold">평온한 규칙성과 몰입이 주는 긍정 시너지</p>
            </div>
          </div>
        </div>

      </div>

    </div>
  </section>

  <!-- 3. 강점 카드 섹션 (Strengths / Target Advantage) -->
  <section id="strengths" class="py-24 relative">
    <div class="max-w-6xl mx-auto px-6 relative z-10">
      
      <!-- 섹션 헤더 (가시성 및 굵기 업그레이드) -->
      <div class="text-center mb-20">
        <h2 class="font-dohyeon text-4xl md:text-6xl text-slate-900 mb-4 drop-shadow-sm">좋은 체력이 만드는 명쾌한 소통의 선순환</h2>
        <p class="text-slate-800 font-extrabold text-lg md:text-xl max-w-2xl mx-auto bg-white/90 p-3 rounded-lg border border-sky-100 shadow-sm">
          🤝 체력이 부족하면 마음의 여유도 메마르기 마련입니다. 단단하게 길러진 기초 체력은 협업 시 지치지 않고 명쾌한 솔루션을 제안하는 '협업 시너지'로 환원됩니다.
        </p>
      </div>

      <!-- 인터랙티브 강점 카드 그리드 (카드 디자인 수영장 킥판 스타일로 변경) -->
      <div class="grid md:grid-cols-3 gap-8">
        
        <!-- 카드 1: 마인드 셋팅 -->
        <div class="bg-white p-8 rounded-3xl shadow-lg border-4 border-slate-200 hover:border-brand transition-all duration-300 hover:shadow-2xl hover:-translate-y-2 group cursor-pointer relative overflow-hidden" onclick="toggleDetail('strength-1')">
          <div class="absolute -right-6 -bottom-6 text-sky-100 opacity-20 text-9xl font-bold select-none">01</div>
          <div class="w-16 h-16 bg-sky-100 rounded-2xl flex items-center justify-center mb-6 text-brand text-3xl group-hover:bg-brand group-hover:text-white transition-all duration-300 shadow-inner">
            ☀️
          </div>
          <h3 class="font-dohyeon text-2xl text-slate-900 mb-4">어떤 변수 앞에서도 긍정 회복</h3>
          <p class="text-slate-800 font-bold text-base leading-relaxed mb-4">
            스트레스나 복잡한 피로를 마음에 담아두지 않는 회복 탄력성을 지녔습니다. 팀워크 중 예기치 못한 이슈를 마주해도 위트 넘치게 극복 방법을 찾습니다.
          </p>
          <div id="strength-1" class="hidden text-sm text-brand-dark bg-sky-50/90 p-4 rounded-xl border-2 border-brand/30 transition-all font-bold">
            🏊‍♀️ <strong>협업 메리트:</strong> 위축되기 쉬운 팀 분위기 속에서도 긍정의 활력을 돌려 상황을 객관적이고 빠르게 극복하게 만듭니다.
          </div>
          <span class="text-sm text-brand block mt-4 font-black group-hover:underline">클릭하여 자세히 보기 &rarr;</span>
        </div>

        <!-- 카드 2: 단순 & 깊은 몰입 -->
        <div class="bg-white p-8 rounded-3xl shadow-lg border-4 border-slate-200 hover:border-brand transition-all duration-300 hover:shadow-2xl hover:-translate-y-2 group cursor-pointer relative overflow-hidden" onclick="toggleDetail('strength-2')">
          <div class="absolute -right-6 -bottom-6 text-sky-100 opacity-20 text-9xl font-bold select-none">02</div>
          <div class="w-16 h-16 bg-sky-100 rounded-2xl flex items-center justify-center mb-6 text-brand text-3xl group-hover:bg-brand group-hover:text-white transition-all duration-300 shadow-inner">
            🧠
          </div>
          <h3 class="font-dohyeon text-2xl text-slate-900 mb-4">생각은 심플하게, 정답은 명확하게</h3>
          <p class="text-slate-800 font-bold text-base leading-relaxed mb-4">
            과도한 잡념은 운동으로 말끔히 해소합니다. 쓸데없는 군더더기를 걷어내고, 문제를 관통하는 핵심 솔루션을 도출해내는 담백한 기획력을 발휘합니다.
          </p>
          <div id="strength-2" class="hidden text-sm text-brand-dark bg-sky-50/90 p-4 rounded-xl border-2 border-brand/30 transition-all font-bold">
                        🏊‍♀️ <strong>협업 메리트:</strong> 논쟁이 장기화되거나 소통 정체가 일어날 때, 복잡한 사안을 일목요연하게 정리하고 추진력 있게 전진합니다.
          </div>
          <span class="text-sm text-brand block mt-4 font-black group-hover:underline">클릭하여 자세히 보기 &rarr;</span>
        </div>

        <!-- 카드 3: 체력에서 우러나는 배려 -->
        <div class="bg-white p-8 rounded-3xl shadow-lg border-4 border-slate-200 hover:border-brand transition-all duration-300 hover:shadow-2xl hover:-translate-y-2 group cursor-pointer relative overflow-hidden" onclick="toggleDetail('strength-3')">
          <div class="absolute -right-6 -bottom-6 text-sky-100 opacity-20 text-9xl font-bold select-none">03</div>
          <div class="w-16 h-16 bg-sky-100 rounded-2xl flex items-center justify-center mb-6 text-brand text-3xl group-hover:bg-brand group-hover:text-white transition-all duration-300 shadow-inner">
            🤝
          </div>
          <h3 class="font-dohyeon text-2xl text-slate-900 mb-4">지치지 않는 체력의 진짜 다정함</h3>
          <p class="text-slate-800 font-bold text-base leading-relaxed mb-4">
            체력이 고갈되면 본심과 달리 배려심도 차갑게 얼어붙습니다. 평소 비축한 단단한 체력이 있기에 고된 업무 상황에서도 끝까지 팀원들에게 다정한 미소와 여유를 잃지 않습니다.
          </p>
          <div id="strength-3" class="hidden text-sm text-brand-dark bg-sky-50/90 p-4 rounded-xl border-2 border-brand/30 transition-all font-bold">
            🏊‍♀️ <strong>협업 메리트:</strong> 바쁜 마감 주간이나 압박이 강한 회의에서도, 여유롭고 차분하게 갈등을 조정해 최상의 시너지를 유지합니다.
          </div>
          <span class="text-sm text-brand block mt-4 font-black group-hover:underline">클릭하여 자세히 보기 &rarr;</span>
        </div>

      </div>

      <!-- 시너지 패널 -->
      <div class="mt-16 bg-slate-900 text-white rounded-3xl p-8 md:p-12 flex flex-col lg:flex-row justify-between items-center gap-8 shadow-xl border-4 border-brand">
        <div class="space-y-4">
          <h4 class="font-dohyeon text-2xl md:text-3xl text-sky-300">🙌 든든한 정연과 최고의 파트너가 될 분들을 찾습니다!</h4>
          <p class="text-slate-300 font-bold text-sm md:text-lg leading-relaxed">
            매일 출퇴근과 지루한 일상에 지쳐 마인드셋 무기가 절실한 직장인 동료들, <br>
            불안한 미래에 멘탈을 든든하게 다스리고 싶은 학생/취업준비생 분들, <br>
            그리고 좋은 체력에서 나오는 고품격 배려심을 지닌 리더십 파트너와의 상생을 환영합니다.
          </p>
        </div>
        <a href="#exercise-recommender" class="shrink-0 font-dohyeon text-lg md:text-xl bg-brand text-white px-8 py-4 rounded-2xl hover:bg-brand-dark transition-all duration-300 shadow-md">
          기분별 맞춤 운동 찾기 &rarr;
        </a>
      </div>

    </div>
  </section>

  <!-- 4. 맞춤 운동 제안 모듈: "그럴 때는 이런 운동 어때요?" (9종 확장 완비) -->
  <section id="exercise-recommender" class="py-24 relative overflow-hidden">
    <div class="max-w-6xl mx-auto px-6 text-center relative z-10">
      
      <!-- 섹션 헤더 -->
      <div class="mb-12">
        <span class="text-5xl inline-block mb-4 animate-bounce">🥽</span>
        <h2 class="font-dohyeon text-4xl md:text-6xl text-slate-900 mb-4">그럴 때는 이런 운동 어때요?</h2>
        <p class="text-slate-800 font-extrabold text-lg md:text-xl max-w-xl mx-auto">
          지금 마음의 무게나 컨디션을 클릭해 보세요! <br>정연이가 직접 겪고 엄선한 맞춤형 긍정 에너지 운동 가이드를 내려 드립니다.
        </p>
      </div>

      <!-- 선택형 인터랙티브 위젯 -->
      <div class="bg-white rounded-3xl p-8 md:p-12 shadow-xl border-4 border-brand-dark text-left">
        <h3 class="font-dohyeon text-2xl md:text-3xl text-brand mb-6 text-center">🎯 지금 나의 마음 신호 상태는?</h3>
        
        <!-- 그리드 확장: 3에서 9종의 운동 추천으로 대폭 확장 -->
        <div class="grid sm:grid-cols-3 gap-4 mb-8">
          <button onclick="recommendExercise('exhausted')" class="p-5 rounded-2xl bg-sky-50 hover:bg-brand hover:text-white transition-all text-slate-950 font-black text-center border-2 border-sky-200 hover:border-brand-dark text-base md:text-lg flex flex-col items-center gap-2">
            <span>😫</span>
            머리가 너무 복잡해서<br>터질 것 같아요
          </button>
          <button onclick="recommendExercise('heavy')" class="p-5 rounded-2xl bg-sky-50 hover:bg-brand hover:text-white transition-all text-slate-950 font-black text-center border-2 border-sky-200 hover:border-brand-dark text-base md:text-lg flex flex-col items-center gap-2">
            <span>🥱</span>
            몸이 찌뿌둥하고<br>강력한 땀을 빼고 싶어요
          </button>
          <button onclick="recommendExercise('lost')" class="p-5 rounded-2xl bg-sky-50 hover:bg-brand hover:text-white transition-all text-slate-950 font-black text-center border-2 border-sky-200 hover:border-brand-dark text-base md:text-lg flex flex-col items-center gap-2">
            <span>😔</span>
            무기력하고 삶의 활력을<br>다시 채우고 싶어요
          </button>
          <button onclick="recommendExercise('tennis')" class="p-5 rounded-2xl bg-sky-50 hover:bg-brand hover:text-white transition-all text-slate-950 font-black text-center border-2 border-sky-200 hover:border-brand-dark text-base md:text-lg flex flex-col items-center gap-2">
            <span>🎾</span>
            강력한 타격감으로<br>스트레스를 날릴래요
          </button>
          <button onclick="recommendExercise('golf')" class="p-5 rounded-2xl bg-sky-50 hover:bg-brand hover:text-white transition-all text-slate-950 font-black text-center border-2 border-sky-200 hover:border-brand-dark text-base md:text-lg flex flex-col items-center gap-2">
            <span>⛳</span>
            조용하고 깊은 몰입과<br>마인드 컨트롤이 필요해요
          </button>
          <button onclick="recommendExercise('ballet')" class="p-5 rounded-2xl bg-sky-50 hover:bg-brand hover:text-white transition-all text-slate-950 font-black text-center border-2 border-sky-200 hover:border-brand-dark text-base md:text-lg flex flex-col items-center gap-2">
            <span>🩰</span>
            흐트러진 몸의 균형과<br>선을 곧게 세우고 싶어요
          </button>
          <button onclick="recommendExercise('pilates')" class="p-5 rounded-2xl bg-sky-50 hover:bg-brand hover:text-white transition-all text-slate-950 font-black text-center border-2 border-sky-200 hover:border-brand-dark text-base md:text-lg flex flex-col items-center gap-2">
            <span>🧘‍♀️</span>
            내면의 속근육과 코어를<br>단단하게 다잡고 싶어요
          </button>
          <button onclick="recommendExercise('climbing')" class="p-5 rounded-2xl bg-sky-50 hover:bg-brand hover:text-white transition-all text-slate-950 font-black text-center border-2 border-sky-200 hover:border-brand-dark text-base md:text-lg flex flex-col items-center gap-2">
            <span>🧗‍♂️</span>
            벽을 마주한 것처럼<br>새로운 도전이 필요해요
          </button>
          <button onclick="recommendExercise('crossfit')" class="p-5 rounded-2xl bg-sky-50 hover:bg-brand hover:text-white transition-all text-slate-950 font-black text-center border-2 border-sky-200 hover:border-brand-dark text-base md:text-lg flex flex-col items-center gap-2">
            <span>🏋️‍♀️</span>
            다 같이 한계에 도전하며<br>엔돌핀을 터뜨릴래요
          </button>
        </div>

        <!-- 추천 결과 박스 (기본적으로 숨김 후 전환) -->
        <div id="recommender-result" class="hidden bg-sky-50/50 p-6 rounded-2xl border-2 border-brand flex-col items-center text-center space-y-4 fade-in-up">
          <div class="text-5xl" id="rec-icon">🏊‍♀️</div>
          <h4 class="font-dohyeon text-2xl md:text-3xl text-slate-900" id="rec-title">추천 운동을 찾고 있습니다...</h4>
          <p class="text-slate-800 font-bold text-base md:text-lg max-w-xl leading-relaxed" id="rec-desc">
            기분을 선택하시면 맞춤형 조언과 운동 처방전이 여기에 나타납니다.
          </p>
          <div class="bg-white px-6 py-3 rounded-full text-brand font-black text-sm border border-brand-light" id="rec-tag">
            #정연의_비밀_처방
          </div>
        </div>

      </div>

    </div>
  </section>

  <!-- 5. 생각 비우기 수영장 (Stress Dissolver) -->
  <section id="mind-pool" class="py-24 relative overflow-hidden">
    <div class="max-w-4xl mx-auto px-6 text-center relative z-10">
      
      <!-- 섹션 헤더 -->
      <div class="mb-12">
        <span class="text-5xl inline-block mb-4 animate-bounce">🏊‍♀️</span>
        <h2 class="font-dohyeon text-4xl md:text-6xl text-brand mb-4">정연이의 마음 비우기 풀(Pool)</h2>
        <p class="text-slate-800 font-extrabold text-lg md:text-xl max-w-xl mx-auto">
          가장 사랑하는 파란 수영장에서 영감을 얻은 마음 청소기입니다. 오늘 머릿속을 괴롭히는 걱정을 차가운 수영장 물속에 통째로 던져 용해시켜 버리세요!
        </p>
      </div>

      <!-- 정화 시뮬레이터 공간 -->
      <div class="max-w-2xl mx-auto bg-gradient-to-b from-sky-400 via-brand to-brand-ocean rounded-3xl p-8 shadow-2xl relative overflow-hidden text-white border-4 border-white">
        <!-- 물속 찰랑거리는 물리 이펙트 -->
        <div class="absolute inset-0 bg-[radial-gradient(ellipse_at_center,_var(--tw-gradient-stops))] from-sky-300/20 via-transparent to-transparent water-ripple pointer-events-none"></div>

        <div id="pool-interactive-container" class="relative z-10 space-y-6">
          <div id="pool-intro">
            <p class="font-dohyeon text-xl md:text-2xl mb-4 text-sky-100">🌊 지금 물에 녹여버리고 싶은 걱정은?</p>
            <div class="flex flex-col sm:flex-row gap-3">
              <input id="stress-input" type="text" placeholder="예: 학업 스트레스, 인간관계 고민, 피곤한 퇴근길 등..." class="flex-1 px-5 py-4 rounded-xl border-none text-slate-900 font-black text-base focus:ring-4 focus:ring-brand-light focus:outline-none">
              <button onclick="dissolveStress()" class="font-dohyeon bg-slate-900 text-sky-300 text-lg px-8 py-4 rounded-xl hover:bg-slate-800 transition-all shrink-0 shadow-lg active:scale-95">
                물속에 던지기 💦
              </button>
            </div>
            <p class="text-xs md:text-sm text-sky-200 mt-3 font-bold opacity-90">⚠️ 수영장에 던져진 스트레스는 흔적도 없이 정화되어 물에 녹아버립니다.</p>
          </div>

          <!-- 용해 애니메이션 영역 (초기 비활성) -->
          <div id="pool-animation" class="hidden flex-col items-center justify-center py-8 space-y-6">
            <div class="relative w-28 h-28 flex items-center justify-center">
              <div class="absolute inset-0 border-4 border-dashed border-sky-200 rounded-full animate-spin"></div>
              <span class="text-5xl text-center" id="pool-emoji">🏊‍♀️</span>
            </div>
            <p id="pool-anim-text" class="font-dohyeon text-2xl tracking-wider animate-pulse">
              물속에서 뽀글뽀글 분해되어 영원히 사라지는 중...
            </p>
          </div>

          <!-- 정화 결과 리액션 영역 (초기 비활성) -->
          <div id="pool-result" class="hidden flex-col items-center justify-center py-6 space-y-5">
            <span class="text-6xl">✨🏊‍♀️✨</span>
            <h3 class="font-dohyeon text-3xl text-sky-200" id="clean-title">걱정이 완전히 녹아 사라졌습니다!</h3>
            <p class="text-base md:text-lg text-white font-bold max-w-md mx-auto leading-relaxed" id="clean-desc">
              "체력이 바닥나서 잠시 걱정이 차올랐던 것뿐이에요! 시원한 물빛 속에 다 털어버렸으니, 이제 수영장 문을 열고 나설 때처럼 가뿐한 긍정 에너지를 가득 채워드릴게요."
            </p>
            <button onclick="resetPool()" class="font-dohyeon border-2 border-white bg-white/10 px-6 py-3 rounded-xl text-base hover:bg-white/20 transition-all mt-4">
              또 다른 스트레스 녹이기
            </button>
          </div>
        </div>

      </div>

    </div>
  </section>

  <!-- 6. 포춘 쿠키 & 비전 섹션 (Call to Action) -->
  <section id="contact" class="py-24 relative overflow-hidden">
    <div class="max-w-4xl mx-auto px-6 text-center relative z-10">
      
      <!-- 포춘 쿠키 장치 (재치있는 문구 상자) -->
      <div class="max-w-2xl mx-auto bg-amber-50 rounded-3xl p-8 mb-12 shadow-xl border-4 border-amber-300 relative">
        <div class="absolute -top-6 left-1/2 -translate-x-1/2 bg-amber-400 text-slate-900 font-dohyeon px-6 py-1 rounded-full text-sm border-2 border-slate-900 shadow-md">
          오늘의 운동 에너자이저
        </div>
        <div class="flex flex-col items-center space-y-4">
          <div class="text-5xl animate-bounce cursor-pointer wiggle-hover" onclick="crackFortuneCookie()">
            🥠
          </div>
          <h3 class="font-dohyeon text-2xl text-slate-800">정연이의 긍정 헬스 포춘 쿠키</h3>
          <!-- 요청 반영: '무작위 운동 조언' 에서 '무작위' 단어 전격 삭제 완료 -->
          <p class="text-slate-700 font-extrabold text-sm md:text-base">
            위의 쿠키를 클릭하면 하루의 피로를 싹 씻어줄 운동 조언과 위트 있는 에너지 명언이 열립니다!
          </p>
          <div id="fortune-display" class="hidden bg-white p-5 rounded-2xl border-2 border-dashed border-amber-400 text-brand-dark font-black text-base md:text-lg w-full max-w-md shadow-inner transition-all transform duration-300">
            "포춘 쿠키를 쪼개어 오늘의 에너지를 획득하세요!"
          </div>
        </div>
      </div>

      <!-- 연락처 및 인사 제안 카드 -->
      <div class="max-w-2xl mx-auto bg-white rounded-3xl p-10 md:p-14 shadow-2xl border-4 border-brand">
        <h2 class="font-dohyeon text-4xl md:text-5xl text-brand mb-6">나 자신과 건강한 친구가 되는 길</h2>
        <p class="text-slate-800 font-bold leading-relaxed mb-8 text-base md:text-lg">
          "몸과 마음의 근력은 단숨에 일궈지지 않지만, 정직하게 나를 돌아보는 한 걸음들이 모여 내 삶의 물길을 바꿉니다. <br>
          명쾌한 영감과 건강한 에너지를 주위에 뿜어내고픈 모든 동료들을 소중히 기다립니다."
        </p>
        
        <!-- 프로필 상세 요약 미니 위젯 -->
        <div class="inline-flex items-center space-x-4 bg-sky-50 p-5 rounded-2xl border-2 border-brand-light text-left mb-8">
          <div class="w-14 h-14 rounded-full bg-brand flex items-center justify-center text-white text-xl font-black shadow-md border-2 border-white">
            정연
          </div>
          <div>
            <h4 class="font-dohyeon text-slate-900 text-lg">김정연 | 브랜더 & 기획자</h4>
            <p class="text-slate-800 font-bold text-xs md:text-sm">꾸준히 수영하고 단련하는 건강한 영감 메신저</p>
          </div>
        </div>

        <!-- 간단 메세지 전송 모듈 -->
        <div class="flex flex-col sm:flex-row gap-3 max-w-md mx-auto">
          <input id="contact-email" type="email" placeholder="당신의 이메일 연락처" class="px-4 py-4 rounded-xl border-4 border-brand-light focus:ring-4 focus:ring-brand focus:outline-none text-base text-slate-900 font-black flex-1">
          <button onclick="sendFakeContact()" class="font-dohyeon bg-brand hover:bg-brand-dark text-white px-8 py-4 rounded-xl text-lg transition-all transform active:scale-95 shadow-lg shadow-sky-300 shrink-0">
            정연이에게 인사 건네기 💌
          </button>
        </div>
        
        <!-- 커스텀 토스트 알림창 대용 메시지 -->
        <div id="contact-success" class="hidden bg-emerald-50 border-2 border-emerald-400 p-3 rounded-xl mt-4">
          <p class="text-emerald-800 font-extrabold text-sm animate-pulse">
            📬 정연 님에게 긍정의 시그널이 도달했습니다! 소중히 검토한 뒤 연락드릴게요! ✨
          </p>
        </div>
      </div>

    </div>
  </section>

  <!-- 7. 푸터 (Footer) -->
  <footer class="bg-slate-950 text-slate-300 py-16 border-t-8 border-brand relative z-10">
    <div class="max-w-6xl mx-auto px-6 flex flex-col md:flex-row justify-between items-center gap-8">
      
      <div class="space-y-3 text-center md:text-left">
        <h3 class="font-dohyeon text-3xl text-white tracking-wider">KIM JEONG YEON</h3>
        <p class="text-sm font-bold text-slate-400">좋은 체력의 단단함에서 흘러나오는 명쾌하고 굳건한 에너지</p>
        <!-- 하단 행운의 마라톤 포춘쿠키 한 문장 상시 가동 -->
        <p class="text-xs text-brand font-black bg-brand/10 inline-block px-3 py-1.5 rounded-lg border border-brand/20">
          🍀 오늘의 한마디: "지구력은 포기하지 않고 숨 쉬는 법을 연습하는 것이다."
        </p>
      </div>

      <div class="flex flex-wrap gap-6 justify-center text-base font-black">
        <a href="#about" class="hover:text-white transition-colors">나의 이야기</a>
        <a href="#strengths" class="hover:text-white transition-colors">체력과 배려</a>
        <a href="#exercise-recommender" class="hover:text-white transition-colors">맞춤 운동 추천</a>
        <a href="#mind-pool" class="hover:text-white transition-colors">마음 정화 풀</a>
        <a href="#contact" class="hover:text-white transition-colors">인사하기</a>
      </div>

    </div>
    
    <div class="max-w-6xl mx-auto px-6 mt-12 pt-8 border-t border-slate-800 flex flex-col sm:flex-row justify-between items-center text-xs text-slate-500 gap-4">
      <p class="font-bold">&copy; 2026 Kim Jeong Yeon. All Rights Reserved. Designed for Authentic Growth.</p>
      <p class="flex items-center gap-1 font-bold">
        <span>Made with</span> 
        <span class="text-red-500">💙</span> 
        <span>and Refreshing Swimming Pool Concept.</span>
      </p>
    </div>
  </footer>

  <!-- JavaScript 상호작용 및 비즈니스 로직 -->
  <script>
    // 1. 소개 탭 상호작용 (Tab Switcher)
    function switchTab(tabId) {
      // 탭 콘텐츠 전부 비활성화
      const contents = document.querySelectorAll('.tab-content');
      contents.forEach(content => {
        content.classList.add('hidden');
        content.classList.remove('block', 'fade-in-up');
      });

      // 탭 버튼 스타일 초기화
      const buttons = document.querySelectorAll('.tab-btn');
      buttons.forEach(btn => {
        btn.classList.remove('bg-brand', 'text-white', 'active', 'shadow-md');
        btn.classList.add('text-slate-800', 'hover:text-brand');
      });

      // 선택한 탭 활성화
      const activeContent = document.getElementById(`content-${tabId}`);
      if (activeContent) {
        activeContent.classList.remove('hidden');
        activeContent.classList.add('block', 'fade-in-up');
      }

      const activeButton = document.getElementById(`tab-${tabId}`);
      if (activeButton) {
        activeButton.classList.add('bg-brand', 'text-white', 'active', 'shadow-md');
        activeButton.classList.remove('text-slate-800', 'hover:text-brand');
      }
    }

    // 2. 강점 카드 상세 토글 (Strength Card Toggle)
    function toggleDetail(detailId) {
      const detailDiv = document.getElementById(detailId);
      if (detailDiv) {
        if (detailDiv.classList.contains('hidden')) {
          detailDiv.classList.remove('hidden');
          detailDiv.classList.add('block', 'fade-in-up');
        } else {
          detailDiv.classList.add('hidden');
          detailDiv.classList.remove('block', 'fade-in-up');
        }
      }
    }

    // 3. 기분 기계 맞춤형 운동 처방전 추천 엔진 (9종 확장)
    function recommendExercise(mood) {
      const resultBox = document.getElementById('recommender-result');
      const recIcon = document.getElementById('rec-icon');
      const recTitle = document.getElementById('rec-title');
      const recDesc = document.getElementById('rec-desc');
      const recTag = document.getElementById('rec-tag');

      resultBox.classList.remove('hidden');
      resultBox.classList.add('flex');

      // 로딩 감지 스크롤바 이동용
      resultBox.scrollIntoView({ behavior: 'smooth', block: 'nearest' });

      if (mood === 'exhausted') {
        recIcon.innerText = "🏊‍♀️";
        recTitle.innerText = "물속에서 깊은 침묵을 만나는 '수영'을 처방합니다!";
        recDesc.innerText = "머리가 터질 것처럼 복잡할 때는 오로지 물리적인 감각에 몰입해 외부 소음을 차단해야 합니다. 시원한 수풀 속으로 뛰어들어 일정한 발차기와 물소리에만 귀를 기울이세요. 물 밖으로 고개를 내밀 때 들이마시는 청량한 공기가 걱정을 전부 날려줄 거예요.";
        recTag.innerText = "#수중_산소호흡 #모든_잡념은_물밑으로";
      } else if (mood === 'heavy') {
        recIcon.innerText = "🧗‍♀️";
        recTitle.innerText = "중력을 거스르며 땀 범벅이 되는 '천국의 계단' 처방!";
        recDesc.innerText = "몸의 독소와 부정적 감정을 몰아내는 최선의 지름길은 고강도 카디오 운동입니다. 묵직한 허벅지의 긴장감과 계단을 밟으며 흐르는 정직한 땀줄기는 복잡하고 잔재주 부리는 생각들을 즉각적으로 단순하게 가공해 줍니다.";
        recTag.innerText = "#천국의계단 #지구력대왕 #단순명쾌피트니스";
      } else if (mood === 'lost') {
        recIcon.innerText = "🏃‍♀️";
        recTitle.innerText = "경쾌하게 대지를 차고 나아가는 '러닝'을 처방합니다!";
        recDesc.innerText = "방구석과 사무실 책상에 갇힌 멘탈을 구출하려면 일단 달려야 합니다. 한 걸음씩 보도블록을 내디딜 때 느껴지는 지면의 반발력과 뺨을 스치는 산뜻한 바람이 고여있던 정연하지 못한 무기력함을 말끔히 쓸어내 줍니다.";
        recTag.innerText = "#러닝메이트 #첫걸음이_중요해 #도파민충전";
      } else if (mood === 'tennis') {
        recIcon.innerText = "🎾";
        recTitle.innerText = "라켓 끝에 전해지는 짜릿한 파괴력, '테니스'를 처방합니다!";
        recDesc.innerText = "가슴속 응어리진 스트레스나 한 주 동안 쌓인 압박감은 노란 공을 강하게 격파하는 타격감으로 해결됩니다. 코트를 바쁘게 질주하고 호쾌한 스윙을 날리다 보면, 어느샌가 고민은 사라지고 개운한 쾌감만 가득 차오릅니다.";
        recTag.innerText = "#랠리_몰입 #라켓스트레스아웃 #유산소끝판왕";
      } else if (mood === 'golf') {
        recIcon.innerText = "⛳";
        recTitle.innerText = "고요한 그린 위에서 나를 정밀하게 직면하는 '골프'를 처방합니다!";
        recDesc.innerText = "어수선한 일상을 멈추고 고독한 평정심과 차분한 지혜를 발휘하고 싶다면 골프가 해답입니다. 한 샷 한 샷에 온전히 나의 밸런스, 그립, 호흡을 동기화하여 완벽하게 제어된 움직임의 예술을 누리세요.";
        recTag.innerText = "#마인드컨트롤 #초정밀_스윙 #그린필드디톡스";
      } else if (mood === 'ballet') {
        recIcon.innerText = "🩰";
        recTitle.innerText = "흐트러진 선을 우아하게 바로 세우는 '발레'를 처방합니다!";
        recDesc.innerText = "컴퓨터 앞에서 경직된 척추와 피로한 근육을 우아하고 곧게 정렬해 줄 발레의 세계를 경험하세요. 호흡을 정갈하게 쉬며 사소한 근육 끝까지 긴장감을 유지하는 동안, 마음마저 기품 있고 굳건하게 바로 서게 될 것입니다.";
        recTag.innerText = "#우아한중심 #자세정렬_마스터 #클래식근력";
      } else if (mood === 'pilates') {
        recIcon.innerText = "🧘‍♀️";
        recTitle.innerText = "나의 중심을 굳건하게 잡는 내면의 힘, '필라테스'를 처방합니다!";
        recDesc.innerText = "흔들리는 주변 환경 속에서 흔들리지 않는 단단한 '코어'를 잡아야 할 때입니다. 깊은 흉식 호흡과 근육 하나하나의 정확한 제어에만 집중하다 보면, 몸의 내공과 함께 어지럽던 정신도 확실한 주체성을 되찾습니다.";
        recTag.innerText = "#속근육마인드 #코어밸런스 #나를_다잡는_시간";
      } else if (mood === 'climbing') {
        recIcon.innerText = "🧗‍♂️";
        recTitle.innerText = "새로운 홀드를 정복하며 한 단계씩 도약하는 '클라이밍'을 처방합니다!";
        recDesc.innerText = "지루하게 반복되는 일상을 비틀고 강력한 성취 욕구를 부활시키고 싶다면 단연 클라이밍입니다. 다음 돌을 붙잡기 위해 영리하게 머리를 굴리고 전신을 팽팽하게 조일 때, 눈앞의 거대한 장애물이 도전에 불과했음을 깨닫습니다.";
        recTag.innerText = "#루트파인딩 #성취감_폭발 #전신인내력";
      } else if (mood === 'crossfit') {
        recIcon.innerText = "🏋️‍♀️";
        recTitle.innerText = "나를 뛰어넘는 뜨거운 동료애와 에너지, '크로스핏'을 처방합니다!";
        recDesc.innerText = "혼자가 아닌 '함께' 한계를 부수고 인생 최고의 폭발적인 아드레날린을 마주하세요. 소리치고, 힘껏 바벨을 들어 올리는 우직한 연대의 에너지 속에서 무기력했던 영혼이 건강하고 명쾌하게 리셋될 것입니다.";
        recTag.innerText = "#WOD돌파 #함께하는시너지 #한계는_없다";
      }
    }

    // 4. 생각 비우기 풀 (Stress Dissolver Controller)
    function dissolveStress() {
      const input = document.getElementById('stress-input');
      const introDiv = document.getElementById('pool-intro');
      const animDiv = document.getElementById('pool-animation');
      const resultDiv = document.getElementById('pool-result');
      const cleanTitle = document.getElementById('clean-title');

      if (!input.value.trim()) {
        alert('물속에 가볍게 털어버릴 수포를 먼저 채워 적어주세요! 🌊');
        return;
      }

      const stressText = input.value;
      introDiv.classList.add('hidden');
      animDiv.classList.remove('hidden');
      animDiv.classList.add('flex');

      // 2초 뒤 물결 정화 완료 시뮬레이션
      setTimeout(() => {
        animDiv.classList.add('hidden');
        animDiv.classList.remove('flex');
        resultDiv.classList.remove('hidden');
        resultDiv.classList.add('flex');
        
        cleanTitle.innerText = `"${stressText}" 걱정은 기분 좋게 완전 정화 완료!`;
      }, 2000);
    }

    function resetPool() {
      const input = document.getElementById('stress-input');
      const introDiv = document.getElementById('pool-intro');
      const resultDiv = document.getElementById('pool-result');

      input.value = '';
      resultDiv.classList.add('hidden');
      resultDiv.classList.remove('flex');
      introDiv.classList.remove('hidden');
    }

    // 5. 긍정 포춘 쿠키 (Fortune Cookie Module)
    const fortunePhrases = [
      "🥠 걱정하지 마세요. 당신이 가진 체력이 생각보다 훨씬 거대합니다! 오늘의 무기력은 땀 한 방울로 말끔히 청소됩니다.",
      "🥠 물 밑으로 깊이 가라앉아 쉬는 법을 아는 사람은, 수면 위로 더 높이 도약할 에너지를 얻습니다.",
      "🥠 운동 효과가 극대화되는 시점은 '더 이상 못 하겠다'가 아닌 '그냥 아무 생각 없이 다음 계단을 밟을 때' 입니다.",
      "🥠 체력이 탄탄해지면, 똑같이 어려운 세상을 대할 때도 한결 부드럽고 유연하게 대처할 수 있는 여유가 피어납니다.",
      "🥠 완벽한 정답보다 단순하고 경쾌하게 던지는 한 걸음이 위기 돌파의 핵심 키워드입니다. 일단 몸을 깨우세요!",
      "🥠 복잡한 수만 가지의 기획서보다, 오늘 퇴근 후 물길을 시원하게 밀어낼 수영 안경 하나의 가치가 큽니다.",
      "🥠 물이 저항으로 느껴진다면, 그 힘에 온전히 나를 맡기세요. 저항은 마침내 나를 앞으로 보낼 추진력이 됩니다."
    ];

    function crackFortuneCookie() {
      const display = document.getElementById('fortune-display');
      display.classList.remove('hidden');
      display.classList.add('block', 'scale-100');
      
      const randomIndex = Math.floor(Math.random() * fortunePhrases.length);
      display.innerText = fortunePhrases[randomIndex];
    }

    // 6. 모의 이메일 연락하기 리액션
    function sendFakeContact() {
      const emailInput = document.getElementById('contact-email');
      const successMsg = document.getElementById('contact-success');

      if (!emailInput.value.trim() || !emailInput.value.includes('@')) {
        alert('김정연 님과 진정으로 소통할 수 있는 올바른 메일 주소를 넣어주세요! 📫');
        return;
      }

      successMsg.classList.remove('hidden');
      emailInput.value = '';

      setTimeout(() => {
        successMsg.classList.add('hidden');
      }, 6000);
    }

    // 7. 네비게이션 스크롤 인터랙션
    window.addEventListener('scroll', () => {
      const nav = document.querySelector('nav');
      if (window.scrollY > 50) {
        nav.classList.add('shadow-xl', 'bg-white', 'py-2');
        nav.classList.remove('py-4');
      } else {
        nav.classList.add('py-4');
        nav.classList.remove('shadow-xl', 'py-2');
      }
    });
  </script>
</body>
</html>