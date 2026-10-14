# andy
穿搭
<!DOCTYPE html>
<html lang="zh-TW">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>STREET VIBE // 乾淨極簡街頭穿搭誌</title>
  
 <!-- Tailwind CSS CDN -->
  <script src="https://cdn.tailwindcss.com"></script>
  
  <!-- Google Font: Inter & Space Grotesk -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&family=Space+Grotesk:wght@500;700&display=swap" rel="stylesheet">
  
  <!-- FontAwesome Icons -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

  <script>
    tailwind.config = {
      theme: {
        extend: {
          fontFamily: {
            sans: ['Inter', 'sans-serif'],
            display: ['Space Grotesk', 'sans-serif'],
          },
          colors: {
            darkBg: '#09090b',
            cardBg: '#121215',
            panelBg: '#18181c',
            borderBg: '#27272a',
            accentOrange: '#ff5500',
            accentCyan: '#00f0ff',
            accentLime: '#ccff00',
          }
        }
      }
    }
  </script>

  <style>
    body {
      background-color: #09090b;
      color: #f4f4f5;
      font-family: 'Inter', sans-serif;
    }

    .font-display {
      font-family: 'Space Grotesk', sans-serif;
    }

    /* Custom Scrollbar */
    ::-webkit-scrollbar {
      width: 6px;
      height: 6px;
    }
    ::-webkit-scrollbar-track {
      background: #09090b;
    }
    ::-webkit-scrollbar-thumb {
      background: #27272a;
      border-radius: 3px;
    }
    ::-webkit-scrollbar-thumb:hover {
      background: #ff5500;
    }

    .neon-border-orange {
      border-color: #ff5500 !important;
      box-shadow: 0 0 12px rgba(255, 85, 0, 0.25);
    }
    
    .neon-border-cyan {
      border-color: #00f0ff !important;
      box-shadow: 0 0 12px rgba(0, 240, 255, 0.2);
    }

    /* Modal transition backdrop */
    .modal-backdrop {
      background-color: rgba(0, 0, 0, 0.88);
      backdrop-filter: blur(10px);
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(8px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .animate-fade-in {
      animation: fadeIn 0.35s ease-out forwards;
    }
  </style>
</head>
<body class="min-h-screen flex flex-col justify-between selection:bg-accentOrange selection:text-black">

  <!-- Header -->
  <header class="sticky top-0 z-40 bg-[#09090b]/90 backdrop-blur-md border-b border-borderBg">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-20 flex items-center justify-between">
      <div class="flex items-center gap-3">
        <div class="w-10 h-10 bg-accentOrange flex items-center justify-center font-black text-black text-xl font-display transform -rotate-2 shadow-lg shadow-accentOrange/20">
          S
        </div>
        <div>
          <h1 class="font-display font-black text-xl sm:text-2xl tracking-wider text-white uppercase flex items-center gap-2">
            STREET<span class="text-accentOrange">//</span>LAB
          </h1>
          <p class="text-[10px] text-zinc-500 uppercase tracking-widest font-mono">Clean Minimalist Streetwear Guide</p>
        </div>
      </div>

      <!-- Navigation Tabs -->
      <nav class="flex items-center space-x-1 sm:space-x-2 text-xs sm:text-sm font-medium">
        <button onclick="switchTab('generator')" id="nav-generator" class="px-3 sm:px-4 py-2 rounded-lg transition-all duration-200 border border-transparent text-white bg-cardBg hover:border-zinc-700">
          <i class="fa-solid fa-bolt-lightning text-accentOrange mr-1.5"></i>今日穿搭
        </button>
        <button onclick="switchTab('lookbook')" id="nav-lookbook" class="px-3 sm:px-4 py-2 rounded-lg transition-all duration-200 border border-transparent text-zinc-400 hover:text-white hover:bg-cardBg">
          <i class="fa-solid fa-layer-group mr-1.5"></i>穿搭靈感
        </button>
        <button onclick="switchTab('wishlist')" id="nav-wishlist" class="px-3 sm:px-4 py-2 rounded-lg transition-all duration-200 border border-transparent text-zinc-400 hover:text-white hover:bg-cardBg relative">
          <i class="fa-solid fa-bookmark mr-1.5"></i>願望清單
          <span id="wishlist-badge" class="hidden absolute -top-1 -right-1 bg-accentOrange text-black text-[10px] font-bold px-1.5 py-0.5 rounded-full">0</span>
        </button>
      </nav>
    </div>
  </header>

  <main class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-8 flex-grow w-full">

    <!-- ==================== SECTION 1: RECOMMENDATION GENERATOR ==================== -->
    <section id="tab-generator" class="space-y-8">
      <!-- Selector Panel -->
      <div class="bg-cardBg border border-borderBg p-6 sm:p-8 rounded-2xl relative overflow-hidden shadow-xl">
        <div class="absolute -top-12 -right-12 w-80 h-80 bg-accentOrange/10 rounded-full filter blur-3xl pointer-events-none"></div>

        <div class="max-w-2xl mb-8">
          <span class="inline-block px-3 py-1 text-[11px] font-mono bg-accentOrange/10 text-accentOrange border border-accentOrange/30 rounded-md mb-3 font-semibold">OOTD GENERATOR v2.0</span>
          <h2 class="text-2xl sm:text-4xl font-extrabold text-white tracking-tight font-display">高質感極簡街頭搭配推演</h2>
          <p class="text-zinc-400 text-xs sm:text-sm mt-2 leading-relaxed">選擇當下的氣候條件與想要的 Vibes，由系統幫你演繹出高階乾淨的街頭 Outfit 及色彩建議。</p>
        </div>

        <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
          <!-- Weather Options -->
          <div>
            <label class="block text-xs font-mono uppercase tracking-wider text-zinc-400 mb-3 flex items-center gap-2">
              <i class="fa-solid fa-temperature-half text-accentCyan"></i> 1. 選擇天氣 / Weather
            </label>
            <div class="grid grid-cols-2 gap-3" id="weather-buttons">
              <button onclick="selectWeather('炎熱 (Hot)')" class="weather-btn p-3.5 bg-darkBg border border-borderBg hover:border-accentCyan rounded-xl text-left transition flex items-center justify-between text-xs sm:text-sm font-medium" data-value="炎熱 (Hot)">
                <span>炎熱 (Hot) ☀️</span>
                <i class="fa-solid fa-circle-check text-accentCyan opacity-0 check-icon text-base"></i>
              </button>
              <button onclick="selectWeather('涼爽 (Mild)')" class="weather-btn p-3.5 bg-darkBg border border-borderBg hover:border-accentCyan rounded-xl text-left transition flex items-center justify-between text-xs sm:text-sm font-medium" data-value="涼爽 (Mild)">
                <span>涼爽 (Mild) 🌤️</span>
                <i class="fa-solid fa-circle-check text-accentCyan opacity-0 check-icon text-base"></i>
              </button>
              <button onclick="selectWeather('寒冷 (Cold)')" class="weather-btn p-3.5 bg-darkBg border border-borderBg hover:border-accentCyan rounded-xl text-left transition flex items-center justify-between text-xs sm:text-sm font-medium" data-value="寒冷 (Cold)">
                <span>寒冷 (Cold) ❄️</span>
                <i class="fa-solid fa-circle-check text-accentCyan opacity-0 check-icon text-base"></i>
              </button>
              <button onclick="selectWeather('下雨 (Rainy)')" class="weather-btn p-3.5 bg-darkBg border border-borderBg hover:border-accentCyan rounded-xl text-left transition flex items-center justify-between text-xs sm:text-sm font-medium" data-value="下雨 (Rainy)">
                <span>下雨 (Rainy) 🌧️</span>
                <i class="fa-solid fa-circle-check text-accentCyan opacity-0 check-icon text-base"></i>
              </button>
            </div>
          </div>

          <!-- Mood / Style Options -->
          <div>
            <label class="block text-xs font-mono uppercase tracking-wider text-zinc-400 mb-3 flex items-center gap-2">
              <i class="fa-solid fa-wand-magic-sparkles text-accentOrange"></i> 2. 選擇風格氛圍 / Style Vibe
            </label>
            <div class="grid grid-cols-2 sm:grid-cols-3 gap-2.5" id="mood-buttons">
              <button onclick="selectMood('帥氣街頭 (Swag Street)')" class="mood-btn p-3 bg-darkBg border border-borderBg hover:border-accentOrange rounded-xl text-left transition flex flex-col justify-between text-xs font-medium h-20" data-value="帥氣街頭 (Swag Street)">
                <div class="flex justify-between w-full">
                  <span class="text-zinc-400 font-mono text-[10px]">01</span>
                  <i class="fa-solid fa-circle-check text-accentOrange opacity-0 check-icon"></i>
                </div>
                <span class="font-bold text-white">帥氣街頭 😎</span>
              </button>

              <button onclick="selectMood('隨性 Chill (Effortless Chill)')" class="mood-btn p-3 bg-darkBg border border-borderBg hover:border-accentOrange rounded-xl text-left transition flex flex-col justify-between text-xs font-medium h-20" data-value="隨性 Chill (Effortless Chill)">
                <div class="flex justify-between w-full">
                  <span class="text-zinc-400 font-mono text-[10px]">02</span>
                  <i class="fa-solid fa-circle-check text-accentOrange opacity-0 check-icon"></i>
                </div>
                <span class="font-bold text-white">隨性 Chill ☕</span>
              </button>

              <button onclick="selectMood('工裝俐落 (Tech/Utility Workwear)')" class="mood-btn p-3 bg-darkBg border border-borderBg hover:border-accentOrange rounded-xl text-left transition flex flex-col justify-between text-xs font-medium h-20" data-value="工裝俐落 (Tech/Utility Workwear)">
                <div class="flex justify-between w-full">
                  <span class="text-zinc-400 font-mono text-[10px]">03</span>
                  <i class="fa-solid fa-circle-check text-accentOrange opacity-0 check-icon"></i>
                </div>
                <span class="font-bold text-white">工裝俐落 🛠️</span>
              </button>

              <button onclick="selectMood('復古街頭 (Vintage/Retro Street)')" class="mood-btn p-3 bg-darkBg border border-borderBg hover:border-accentOrange rounded-xl text-left transition flex flex-col justify-between text-xs font-medium h-20" data-value="復古街頭 (Vintage/Retro Street)">
                <div class="flex justify-between w-full">
                  <span class="text-zinc-400 font-mono text-[10px]">04</span>
                  <i class="fa-solid fa-circle-check text-accentOrange opacity-0 check-icon"></i>
                </div>
                <span class="font-bold text-white">復古街頭 📼</span>
              </button>

              <button onclick="selectMood('極簡高街 (High-Street Minimal)')" class="mood-btn p-3 bg-darkBg border border-borderBg hover:border-accentOrange rounded-xl text-left transition flex flex-col justify-between text-xs font-medium h-20" data-value="極簡高街 (High-Street Minimal)">
                <div class="flex justify-between w-full">
                  <span class="text-zinc-400 font-mono text-[10px]">05</span>
                  <i class="fa-solid fa-circle-check text-accentOrange opacity-0 check-icon"></i>
                </div>
                <span class="font-bold text-white">極簡高街 ✨</span>
              </button>

              <button onclick="selectMood('鬆弛感/Athleisure (Sporty Casual)')" class="mood-btn p-3 bg-darkBg border border-borderBg hover:border-accentOrange rounded-xl text-left transition flex flex-col justify-between text-xs font-medium h-20" data-value="鬆弛感/Athleisure (Sporty Casual)">
                <div class="flex justify-between w-full">
                  <span class="text-zinc-400 font-mono text-[10px]">06</span>
                  <i class="fa-solid fa-circle-check text-accentOrange opacity-0 check-icon"></i>
                </div>
                <span class="font-bold text-white">鬆弛感 🏃‍♂️</span>
              </button>
            </div>
          </div>
        </div>

        <!-- Action Button -->
        <div class="mt-8 flex justify-end border-t border-borderBg/60 pt-6">
          <button onclick="generateRecommendation()" class="w-full sm:w-auto px-8 py-4 bg-accentOrange hover:bg-orange-600 text-black font-extrabold text-sm uppercase tracking-wider rounded-xl transition-all flex items-center justify-center gap-2 shadow-xl shadow-accentOrange/20 active:scale-98">
            <i class="fa-solid fa-arrows-rotate text-base"></i> 生成今日穿搭建議
          </button>
        </div>
      </div>

      <!-- Recommendation Display Container -->
      <div id="recommendation-result" class="hidden">
        <!-- Rendered dynamically -->
      </div>
    </section>

    <!-- ==================== SECTION 2: LOOKBOOK GALLERY ==================== -->
    <section id="tab-lookbook" class="hidden space-y-6">
      <div class="flex flex-col lg:flex-row lg:items-center justify-between gap-4 border-b border-borderBg pb-6">
        <div>
          <h2 class="text-2xl sm:text-3xl font-black text-white uppercase tracking-wider font-display">LOOKBOOK // 靈感圖鑑</h2>
          <p class="text-xs sm:text-sm text-zinc-400 mt-1">探索多元極簡街頭範例，支援重點標籤檢索</p>
        </div>

        <!-- Filter Tags Bar -->
        <div class="flex flex-wrap gap-2" id="lookbook-filter-tags">
          <button onclick="filterLookbook('ALL')" class="tag-filter-btn active px-3 py-1.5 rounded-lg text-xs font-mono transition bg-white text-black font-bold" data-tag="ALL">
            #全部 (All)
          </button>
          <button onclick="filterLookbook('#Oversized')" class="tag-filter-btn px-3 py-1.5 rounded-lg text-xs font-mono transition bg-cardBg border border-borderBg text-zinc-300 hover:border-zinc-500" data-tag="#Oversized">
            #Oversized
          </button>
          <button onclick="filterLookbook('#工裝')" class="tag-filter-btn px-3 py-1.5 rounded-lg text-xs font-mono transition bg-cardBg border border-borderBg text-zinc-300 hover:border-zinc-500" data-tag="#工裝">
            #工裝
          </button>
          <button onclick="filterLookbook('#層次穿搭')" class="tag-filter-btn px-3 py-1.5 rounded-lg text-xs font-mono transition bg-cardBg border border-borderBg text-zinc-300 hover:border-zinc-500" data-tag="#層次穿搭">
            #層次穿搭
          </button>
          <button onclick="filterLookbook('#復古')" class="tag-filter-btn px-3 py-1.5 rounded-lg text-xs font-mono transition bg-cardBg border border-borderBg text-zinc-300 hover:border-zinc-500" data-tag="#復古">
            #復古
          </button>
          <button onclick="filterLookbook('#高街極簡')" class="tag-filter-btn px-3 py-1.5 rounded-lg text-xs font-mono transition bg-cardBg border border-borderBg text-zinc-300 hover:border-zinc-500" data-tag="#高街極簡">
            #高街極簡
          </button>
          <button onclick="filterLookbook('#機能')" class="tag-filter-btn px-3 py-1.5 rounded-lg text-xs font-mono transition bg-cardBg border border-borderBg text-zinc-300 hover:border-zinc-500" data-tag="#機能">
            #機能
          </button>
          <button onclick="filterLookbook('#球鞋重點')" class="tag-filter-btn px-3 py-1.5 rounded-lg text-xs font-mono transition bg-cardBg border border-borderBg text-zinc-300 hover:border-zinc-500" data-tag="#球鞋重點">
            #球鞋重點
          </button>
        </div>
      </div>

      <!-- Outfits Grid -->
      <div id="lookbook-grid" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
        <!-- Outfits injected dynamically -->
      </div>
    </section>

    <!-- ==================== SECTION 3: WISHLIST & SHOPPING TRACKER ==================== -->
    <section id="tab-wishlist" class="hidden space-y-6">
      <div class="flex flex-col sm:flex-row sm:items-center justify-between gap-4 border-b border-borderBg pb-6">
        <div>
          <h2 class="text-2xl sm:text-3xl font-black text-white uppercase tracking-wider font-display">WISHLIST // 單品夢幻清單</h2>
          <p class="text-xs sm:text-sm text-zinc-400 mt-1">追蹤心儀街頭單品與採購進度（資料自動保存在瀏覽器本地）</p>
        </div>

        <button onclick="toggleWishlistModal(true)" class="px-4 py-2.5 bg-accentCyan hover:bg-cyan-400 text-black font-extrabold text-xs uppercase tracking-wider rounded-lg transition flex items-center gap-2 self-start sm:self-auto shadow-lg shadow-accentCyan/10">
          <i class="fa-solid fa-plus text-sm"></i> 新增單品
        </button>
      </div>

      <!-- Wishlist Grid -->
      <div id="wishlist-grid" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
        <!-- Injected via JS -->
      </div>

      <!-- Empty State -->
      <div id="wishlist-empty" class="hidden text-center py-20 bg-cardBg border border-dashed border-borderBg rounded-2xl">
        <div class="w-16 h-16 bg-darkBg border border-borderBg rounded-full flex items-center justify-center mx-auto mb-4 text-zinc-500">
          <i class="fa-solid fa-bag-shopping text-2xl"></i>
        </div>
        <h3 class="text-lg font-bold text-zinc-300">願望清單目前無任何資料</h3>
        <p class="text-xs text-zinc-500 mt-1 max-w-sm mx-auto">點擊右上角「新增單品」，或是從今日推薦中直接快取收藏！</p>
      </div>
    </section>

  </main>

  <!-- MODAL: Outfit Details -->
  <div id="modal-outfit" class="fixed inset-0 z-50 hidden modal-backdrop flex items-center justify-center p-4 sm:p-6">
    <div class="bg-cardBg border border-borderBg rounded-2xl max-w-2xl w-full max-h-[90vh] overflow-y-auto relative shadow-2xl">
      <button onclick="closeOutfitModal()" class="absolute top-4 right-4 z-20 w-9 h-9 bg-black/80 border border-borderBg text-zinc-400 hover:text-white rounded-full flex items-center justify-center transition">
        <i class="fa-solid fa-xmark"></i>
      </button>

      <div id="modal-outfit-content">
        <!-- Dynamically filled -->
      </div>
    </div>
  </div>

  <!-- MODAL: Add Wishlist Item -->
  <div id="modal-wishlist" class="fixed inset-0 z-50 hidden modal-backdrop flex items-center justify-center p-4">
    <div class="bg-cardBg border border-borderBg rounded-2xl max-w-md w-full p-6 relative shadow-2xl">
      <div class="flex items-center justify-between pb-4 border-b border-borderBg mb-5">
        <h3 class="text-lg font-bold text-white uppercase tracking-wider flex items-center gap-2 font-display">
          <i class="fa-solid fa-circle-plus text-accentCyan"></i> 新增夢幻單品
        </h3>
        <button onclick="toggleWishlistModal(false)" class="text-zinc-400 hover:text-white text-lg">
          <i class="fa-solid fa-xmark"></i>
        </button>
      </div>

      <form id="wishlist-form" onsubmit="saveWishlistItem(event)" class="space-y-4">
        <div>
          <label class="block text-xs font-mono uppercase text-zinc-400 mb-1">單品名稱 *</label>
          <input type="text" id="ws-name" required placeholder="例: Acne Studios 寬版重磅 Hoodie" class="w-full bg-darkBg border border-borderBg focus:border-accentCyan text-white px-3.5 py-2.5 rounded-lg text-sm outline-none transition">
        </div>

        <div class="grid grid-cols-2 gap-3">
          <div>
            <label class="block text-xs font-mono uppercase text-zinc-400 mb-1">品牌 / Brand</label>
            <input type="text" id="ws-brand" placeholder="例: Stussy" class="w-full bg-darkBg border border-borderBg focus:border-accentCyan text-white px-3.5 py-2.5 rounded-lg text-sm outline-none transition">
          </div>
          <div>
            <label class="block text-xs font-mono uppercase text-zinc-400 mb-1">類別 / Category</label>
            <select id="ws-category" class="w-full bg-darkBg border border-borderBg focus:border-accentCyan text-white px-3 py-2.5 rounded-lg text-sm outline-none transition">
              <option value="上衣 Top">上衣 Top</option>
              <option value="褲款 Bottom">褲款 Bottom</option>
              <option value="外套 Jacket">外套 Jacket</option>
              <option value="鞋款 Sneaker">鞋款 Sneaker</option>
              <option value="配件 Accessory">配件 Accessory</option>
            </select>
          </div>
        </div>

        <div class="grid grid-cols-2 gap-3">
          <div>
            <label class="block text-xs font-mono uppercase text-zinc-400 mb-1">預估價格 (NT$)</label>
            <input type="number" id="ws-price" placeholder="例: 4500" class="w-full bg-darkBg border border-borderBg focus:border-accentCyan text-white px-3.5 py-2.5 rounded-lg text-sm outline-none transition">
          </div>
          <div>
            <label class="block text-xs font-mono uppercase text-zinc-400 mb-1">圖片網址 (URL)</label>
            <input type="url" id="ws-image" placeholder="https://..." class="w-full bg-darkBg border border-borderBg focus:border-accentCyan text-white px-3.5 py-2.5 rounded-lg text-sm outline-none transition">
          </div>
        </div>

        <div>
          <label class="block text-xs font-mono uppercase text-zinc-400 mb-1">備註 / 搭配筆記</label>
          <textarea id="ws-note" rows="2" placeholder="例: 版型偏大，建議拿 S 號，適合配寬版灰色棉褲..." class="w-full bg-darkBg border border-borderBg focus:border-accentCyan text-white px-3.5 py-2.5 rounded-lg text-sm outline-none transition"></textarea>
        </div>

        <div class="pt-2 flex justify-end gap-3">
          <button type="button" onclick="toggleWishlistModal(false)" class="px-4 py-2.5 bg-darkBg border border-borderBg text-zinc-300 text-xs font-bold rounded-lg hover:bg-zinc-800 transition">
            取消
          </button>
          <button type="submit" class="px-5 py-2.5 bg-accentCyan hover:bg-cyan-400 text-black text-xs font-extrabold uppercase tracking-wider rounded-lg transition">
            儲存單品
          </button>
        </div>
      </form>
    </div>
  </div>

  <!-- Footer -->
  <footer class="border-t border-borderBg bg-darkBg py-8 mt-16">
    <div class="max-w-7xl mx-auto px-4 text-center text-xs text-zinc-500 font-mono">
      <p>STREET VIBE // CLEAN MINIMALIST STREETWEAR OOTD CATALOG</p>
      <p class="mt-1 text-[10px] text-zinc-600">DESIGNED FOR URBAN STREETWEAR ENTHUSIASTS</p>
    </div>
  </footer>

  <script>
    /* ==================== EXPANDED OUTFIT DATABASE ==================== */
    const OUTFITS_DATA = [
      {
        id: 'outfit-1',
        title: '極簡黑魂工裝與機能疊穿 Look',
        weather: '涼爽 (Mild)',
        mood: '工裝俐落 (Tech/Utility Workwear)',
        tags: ['#Oversized', '#工裝', '#機能', '#層次穿搭'],
        image: 'https://images.unsplash.com/photo-1509631179647-0177331693ae?auto=format&fit=crop&w=900&q=80',
        palette: ['#09090b', '#27272a', '#71717a', '#00f0ff'],
        colorDesc: '全黑基底 (Mono Black) 輔以銀灰配件與極小面積亮點，營造俐落工業冷酷感。',
        items: [
          '重磅高領黑色 Oversized 工裝襯衫',
          '多口袋防刮降落傘寬版降落褲',
          'Salomon XT-6 越野跑鞋 (純黑版本)',
          '戰術扣環防潑水單肩小包'
        ],
        desc: '以不同材質的黑色系（霧面棉質、高密度尼龍、金屬扣環）堆疊出同色系的階梯感，乾淨俐落又具備強烈的都會機能街頭感。'
      },
      {
        id: 'outfit-2',
        title: '美式 90s 水洗單寧與重磅素 T',
        weather: '涼爽 (Mild)',
        mood: '復古街頭 (Vintage/Retro Street)',
        tags: ['#復古', '#Oversized', '#層次穿搭'],
        image: 'https://images.unsplash.com/photo-1529139574466-a303027c1d8b?auto=format&fit=crop&w=900&q=80',
        palette: ['#1e293b', '#64748b', '#f8fafc', '#b91c1c'],
        colorDesc: '復古水洗藍 (Washed Denim) 與純白撞色，充滿純粹的 90 年代隨性街頭味。',
        items: [
          '古著水洗落肩丹寧夾克外套',
          '280g 重磅純白落肩 T-Shirt (露內搭底邊)',
          '水洗碳灰微寬版微喇叭牛仔褲',
          'Nike Dunk Low 復古紅白球鞋'
        ],
        desc: '水洗落肩版型能完美修飾身形輪廓，運用下擺下露出的白色 T-shirt 做出俐落分界，是永遠不退流行且具高級質感的經典街頭 Look。'
      },
      {
        id: 'outfit-3',
        title: '高街極簡黑白高磅數 Hoodie 套裝',
        weather: '寒冷 (Cold)',
        mood: '帥氣街頭 (Swag Street)',
        tags: ['#Oversized', '#高街極簡', '#球鞋重點'],
        image: 'https://images.unsplash.com/photo-1552374196-1ab2a1c593e8?auto=format&fit=crop&w=900&q=80',
        palette: ['#000000', '#ffffff', '#ff5500'],
        colorDesc: '高對比黑白極簡對比，加上球鞋橘紅色焦點點綴。',
        items: [
          '450g 挺括硬挺無接縫連帽衛衣 (Hoodie)',
          '極簡黑直筒落地微寬縮口褲',
          'Air Jordan 1 High 經典配色球鞋',
          '粗體古巴鏈條銀飾 (Cuban Chain)'
        ],
        desc: '選擇磅數高且布料挺括的黑 Hoodie，拋棄複雜印花，純粹靠流暢俐落的版型與質感球鞋展現高街 swag 氣場。'
      },
      {
        id: 'outfit-4',
        title: '極簡都會機能防風雨風衣組',
        weather: '下雨 (Rainy)',
        mood: '工裝俐落 (Tech/Utility Workwear)',
        tags: ['#機能', '#高街極簡', '#工裝'],
        image: 'https://images.unsplash.com/photo-1515886657613-9f3515b0c78f?auto=format&fit=crop&w=900&q=80',
        palette: ['#18181b', '#3f3f46', '#0284c7'],
        colorDesc: '深灰雨雲色調 (Storm Grey) 搭配防水材質所展現的自然光澤。',
        items: [
          'GORE-TEX 防水立領拼接拉鍊夾克',
          '抗撕裂防水微寬直筒西裝長褲',
          'Hoka One One 防水中筒越野靴',
          '極簡無縫防水漁夫帽'
        ],
        desc: '雨天專屬的俐落防線！完全不顯狼狽，乾淨流線的切割剪裁搭配無縫線口袋，兼具全天候機能與高品質都會美學。'
      },
      {
        id: 'outfit-5',
        title: '鬆弛感 City Boy 夏日五分褲穿搭',
        weather: '炎熱 (Hot)',
        mood: '隨性 Chill (Effortless Chill)',
        tags: ['#Oversized', '#高街極簡', '#球鞋重點'],
        image: 'https://images.unsplash.com/photo-1503342217505-b0a15ec3261c?auto=format&fit=crop&w=900&q=80',
        palette: ['#f5f5f4', '#1e293b', '#94a3b8'],
        colorDesc: '燕麥色 (Oatmeal) 與海軍藍 (Navy Blue) 的清涼質感交織。',
        items: [
          '燕麥白寬版 10oz 磅數微高領短 T',
          '膝下深藍打褶寬版五分褲',
          'New Balance 1906R 復古銀灰跑鞋',
          '白色中筒運動印花襪'
        ],
        desc: '夏季街頭最需追求「鬆弛感」。寬大的五分褲與挺身 short-sleeve 帶來極佳的空氣感與通風度，清爽度滿分。'
      },
      {
        id: 'outfit-6',
        title: '美式學院復古棒球夾克組合',
        weather: '寒冷 (Cold)',
        mood: '復古街頭 (Vintage/Retro Street)',
        tags: ['#復古', '#層次穿搭', '#球鞋重點'],
        image: 'https://images.unsplash.com/photo-1516257984-b1b4d707412e?auto=format&fit=crop&w=900&q=80',
        palette: ['#451a03', '#fef3c7', '#172554'],
        colorDesc: '復古皮革棕與奶白色拼接，散發濃郁 80 年代常春藤街頭質感。',
        items: [
          '皮革拼接毛料美式棒球外套 (Varsity Jacket)',
          '灰色內刷毛連帽拉鍊衫',
          '直筒寬版水洗藍原色牛仔褲',
          'Adidas Samba 麂皮德訓鞋'
        ],
        desc: '運用棒球外套的拼接皮革細節拉出主角光環，內搭灰色 Hoodie 做出厚實有型的保暖層次感。'
      },
      {
        id: 'outfit-7',
        title: '高街極簡暗黑懸垂感穿搭',
        weather: '涼爽 (Mild)',
        mood: '極簡高街 (High-Street Minimal)',
        tags: ['#高街極簡', '#Oversized'],
        image: 'https://images.unsplash.com/photo-1508214751196-bcfd4ca60f91?auto=format&fit=crop&w=900&q=80',
        palette: ['#000000', '#262626', '#e5e5e5'],
        colorDesc: '純粹的極致黑與懸垂布料的光影交錯。',
        items: [
          '微光澤感落肩寬袖西裝外套',
          '不規則裁切長版黑 T (內搭露層次)',
          '垂墜感高腰寬版落地微喇叭拖地褲',
          '方頭皮革厚底德比鞋/靴款'
        ],
        desc: '拋棄街頭常見的複雜 Logo，將重點完全放在剪裁、布料垂墜度與比例延伸上，呈現低調卻氣場強大的現代高街廓形。'
      },
      {
        id: 'outfit-8',
        title: '輕便 Athleisure 街頭運動鬆弛感',
        weather: '炎熱 (Hot)',
        mood: '鬆弛感/Athleisure (Sporty Casual)',
        tags: ['#球鞋重點', '#Oversized', '#層次穿搭'],
        image: 'https://images.unsplash.com/photo-1483721310020-03333e577078?auto=format&fit=crop&w=900&q=80',
        palette: ['#052e16', '#e2e8f0', '#00f0ff'],
        colorDesc: '復古墨綠 (Forest Green) 與運動灰的日常調和。',
        items: [
          '美式復古字體印花 OVERSZE 圓領 T-shirt',
          '灰階高磅數運動尼龍抽繩短褲',
          'Asics GEL-Kayano 14 復古金屬感跑鞋',
          '黑刺繡棒球帽 (Dad Cap)'
        ],
        desc: '隨興卻絕非隨便！巧妙運用復古運動印花與銀色金屬跑鞋作為亮點，打造休閒、舒適又滿載街頭細節的 Athleisure 氛圍。'
      },
      {
        id: 'outfit-9',
        title: '夏日雨季街頭涼爽輕機能Look',
        weather: '下雨 (Rainy)',
        mood: '隨性 Chill (Effortless Chill)',
        tags: ['#機能', '#工裝'],
        image: 'https://images.unsplash.com/photo-1520975661595-6453be3f7070?auto=format&fit=crop&w=900&q=80',
        palette: ['#1c1917', '#78716c', '#ccff00'],
        colorDesc: '大地泥灰 (Earth Stone) 結合螢光綠小扣件的戶外質感。',
        items: [
          '防潑水超薄網眼透氣薄外套',
          '吸濕排汗灰色打底背心',
          '速乾快乾防撕裂鬆緊短褲',
          'Keen / Suicoke 機能戶外涼鞋搭配黑襪'
        ],
        desc: '因應夏天突然其來的驟雨，輕盈速乾布料搭配戶外機能涼鞋，既能保持腳步乾爽，又能展現不凡的露營戶外街頭 Vibe。'
      }
    ];

    /* State Management */
    let selectedWeather = null;
    let selectedMood = null;
    let activeTag = 'ALL';
    let wishlistItems = JSON.parse(localStorage.getItem('streetvibe_wishlist') || '[]');

    /* Initialization */
    window.onload = function() {
      renderLookbook();
      renderWishlist();
    };

    function switchTab(tabName) {
      ['generator', 'lookbook', 'wishlist'].forEach(t => {
        const section = document.getElementById(`tab-${t}`);
        const navBtn = document.getElementById(`nav-${t}`);
        if (t === tabName) {
          section.classList.remove('hidden');
          navBtn.classList.remove('text-zinc-400');
          navBtn.classList.add('text-white', 'bg-cardBg', 'border-zinc-700');
        } else {
          section.classList.add('hidden');
          navBtn.classList.add('text-zinc-400');
          navBtn.classList.remove('text-white', 'bg-cardBg', 'border-zinc-700');
        }
      });
    }

    /* Generator Logic */
    function selectWeather(val) {
      selectedWeather = val;
      document.querySelectorAll('#weather-buttons .weather-btn').forEach(btn => {
        const isMatch = btn.getAttribute('data-value') === val;
        btn.classList.toggle('neon-border-cyan', isMatch);
        btn.classList.toggle('border-borderBg', !isMatch);
        btn.querySelector('.check-icon').classList.toggle('opacity-0', !isMatch);
      });
    }

    function selectMood(val) {
      selectedMood = val;
      document.querySelectorAll('#mood-buttons .mood-btn').forEach(btn => {
        const isMatch = btn.getAttribute('data-value') === val;
        btn.classList.toggle('neon-border-orange', isMatch);
        btn.classList.toggle('border-borderBg', !isMatch);
        btn.querySelector('.check-icon').classList.toggle('opacity-0', !isMatch);
      });
    }

    function generateRecommendation() {
      const resultContainer = document.getElementById('recommendation-result');

      // Filter outfits according to choices
      let matches = OUTFITS_DATA.filter(item => {
        const matchW = !selectedWeather || item.weather === selectedWeather;
        const matchM = !selectedMood || item.mood === selectedMood;
        return matchW && matchM;
      });

      let isFallback = false;
      if (matches.length === 0) {
        matches = OUTFITS_DATA;
        isFallback = true;
      }

      // Pick random matched item
      const picked = matches[Math.floor(Math.random() * matches.length)];

      resultContainer.innerHTML = `
        <div class="bg-cardBg border border-accentOrange/50 rounded-2xl overflow-hidden shadow-2xl transition-all animate-fade-in mt-6">
          ${isFallback ? `
            <div class="bg-accentOrange/10 border-b border-accentOrange/20 px-4 py-2 text-xs text-accentOrange font-mono flex items-center gap-2">
              <i class="fa-solid fa-circle-info"></i> 未找到完全精準條件的組合，為你精選此款備受好評的街頭極簡組合：
            </div>
          ` : ''}
          <div class="grid grid-cols-1 lg:grid-cols-12">
            <div class="lg:col-span-5 relative h-80 lg:h-auto overflow-hidden bg-black">
              <img src="${picked.image}" alt="${picked.title}" class="w-full h-full object-cover">
              <div class="absolute top-4 left-4 flex flex-wrap gap-2">
                <span class="px-2.5 py-1 bg-black/85 text-accentCyan text-xs font-mono rounded-md border border-accentCyan/30">${picked.weather}</span>
                <span class="px-2.5 py-1 bg-black/85 text-accentOrange text-xs font-mono rounded-md border border-accentOrange/30">${picked.mood}</span>
              </div>
            </div>

            <div class="lg:col-span-7 p-6 sm:p-8 flex flex-col justify-between">
              <div>
                <div class="flex flex-wrap gap-1.5 mb-3">
                  ${picked.tags.map(t => `<span class="text-[11px] font-mono text-zinc-400 bg-darkBg px-2.5 py-1 rounded-md border border-borderBg">${t}</span>`).join('')}
                </div>
                <h3 class="text-2xl sm:text-3xl font-extrabold text-white tracking-wide font-display mb-3">${picked.title}</h3>
                <p class="text-xs sm:text-sm text-zinc-300 leading-relaxed mb-6">${picked.desc}</p>

                <!-- Color Palette Advice -->
                <div class="bg-darkBg p-3.5 rounded-xl border border-borderBg mb-6">
                  <span class="text-[10px] font-mono uppercase tracking-wider text-zinc-400 block mb-2 flex items-center gap-1.5">
                    <i class="fa-solid fa-palette text-accentCyan"></i> 色彩搭配調性建議 / Color Palette
                  </span>
                  <div class="flex items-center gap-3">
                    <div class="flex items-center gap-1">
                      ${picked.palette.map(c => `<span class="w-5 h-5 rounded-full border border-zinc-700 shadow-inner" style="background-color: ${c}"></span>`).join('')}
                    </div>
                    <p class="text-xs text-zinc-400">${picked.colorDesc}</p>
                  </div>
                </div>

                <!-- Item Breakdown -->
                <div class="border-t border-borderBg pt-5 mb-6">
                  <h4 class="text-xs font-mono uppercase text-zinc-400 tracking-wider mb-3 flex items-center gap-2">
                    <i class="fa-solid fa-shirt text-accentOrange"></i> 單品組合拆解 / Outfit Breakdown
                  </h4>
                  <div class="grid grid-cols-1 sm:grid-cols-2 gap-2 text-xs text-zinc-200">
                    ${picked.items.map(it => `
                      <div class="flex items-center justify-between bg-darkBg p-2.5 rounded-lg border border-borderBg">
                        <span class="flex items-center gap-2">
                          <i class="fa-solid fa-angle-right text-accentOrange text-xs"></i> ${it}
                        </span>
                        <button onclick="quickAddWishlist('${it}')" class="text-[10px] font-mono text-accentCyan hover:underline">
                          + 收藏
                        </button>
                      </div>
                    `).join('')}
                  </div>
                </div>
              </div>

              <div class="flex items-center justify-between pt-2 border-t border-borderBg/40">
                <button onclick="generateRecommendation()" class="text-xs font-mono text-zinc-400 hover:text-white flex items-center gap-1.5 transition">
                  <i class="fa-solid fa-shuffle"></i> 重新抽換組合
                </button>
                <button onclick="openOutfitModal('${picked.id}')" class="px-4 py-2 bg-darkBg hover:bg-zinc-800 border border-borderBg text-white text-xs font-bold rounded-lg transition">
                  檢視詳細資料
                </button>
              </div>
            </div>
          </div>
        </div>
      `;

      resultContainer.classList.remove('hidden');
      resultContainer.scrollIntoView({ behavior: 'smooth', block: 'nearest' });
    }

    /* Lookbook Gallery Logic */
    function filterLookbook(tag) {
      activeTag = tag;
      document.querySelectorAll('#lookbook-filter-tags .tag-filter-btn').forEach(btn => {
        const isMatch = btn.getAttribute('data-tag') === tag;
        if (isMatch) {
          btn.className = 'tag-filter-btn active px-3 py-1.5 rounded-lg text-xs font-mono transition bg-white text-black font-bold';
        } else {
          btn.className = 'tag-filter-btn px-3 py-1.5 rounded-lg text-xs font-mono transition bg-cardBg border border-borderBg text-zinc-300 hover:border-zinc-500';
        }
      });
      renderLookbook();
    }

    function renderLookbook() {
      const grid = document.getElementById('lookbook-grid');
      const filtered = activeTag === 'ALL' 
        ? OUTFITS_DATA 
        : OUTFITS_DATA.filter(item => item.tags.includes(activeTag));

      grid.innerHTML = filtered.map(item => `
        <div class="bg-cardBg border border-borderBg rounded-2xl overflow-hidden hover:border-zinc-500 transition-all duration-300 group flex flex-col justify-between">
          <div>
            <div class="relative h-80 overflow-hidden bg-black">
              <img src="${item.image}" alt="${item.title}" class="w-full h-full object-cover group-hover:scale-105 transition duration-500">
              <div class="absolute top-3 left-3 flex flex-wrap gap-1">
                <span class="px-2 py-0.5 bg-black/80 text-accentCyan text-[10px] font-mono rounded border border-accentCyan/30">${item.weather}</span>
                <span class="px-2 py-0.5 bg-black/80 text-accentOrange text-[10px] font-mono rounded border border-accentOrange/30">${item.mood.split(' ')[0]}</span>
              </div>
            </div>

            <div class="p-5">
              <div class="flex flex-wrap gap-1 mb-2">
                ${item.tags.map(t => `<span class="text-[10px] font-mono text-zinc-400 bg-darkBg px-2 py-0.5 rounded border border-borderBg">${t}</span>`).join('')}
              </div>
              <h3 class="text-base font-bold text-white group-hover:text-accentOrange transition mb-2 font-display">${item.title}</h3>
              <p class="text-xs text-zinc-400 line-clamp-2 leading-relaxed">${item.desc}</p>
            </div>
          </div>

          <div class="px-5 pb-5 pt-0">
            <button onclick="openOutfitModal('${item.id}')" class="w-full py-2.5 bg-darkBg border border-borderBg hover:border-accentOrange text-zinc-300 hover:text-white text-xs font-mono rounded-lg transition flex items-center justify-center gap-2">
              <i class="fa-regular fa-eye"></i> 查看風格靈感細節
            </button>
          </div>
        </div>
      `).join('');
    }

    function openOutfitModal(id) {
      const item = OUTFITS_DATA.find(o => o.id === id);
      if (!item) return;

      const modalContent = document.getElementById('modal-outfit-content');
      modalContent.innerHTML = `
        <div class="relative h-80 sm:h-96 w-full bg-black">
          <img src="${item.image}" alt="${item.title}" class="w-full h-full object-cover">
          <div class="absolute bottom-0 inset-x-0 bg-gradient-to-t from-cardBg to-transparent h-24"></div>
        </div>
        <div class="p-6 sm:p-8 space-y-6">
          <div>
            <div class="flex items-center gap-2 mb-2">
              <span class="px-2.5 py-0.5 bg-accentCyan/10 text-accentCyan border border-accentCyan/30 text-xs font-mono rounded-md">${item.weather}</span>
              <span class="px-2.5 py-0.5 bg-accentOrange/10 text-accentOrange border border-accentOrange/30 text-xs font-mono rounded-md">${item.mood}</span>
            </div>
            <h3 class="text-2xl font-extrabold text-white font-display">${item.title}</h3>
            <p class="text-xs sm:text-sm text-zinc-300 mt-2 leading-relaxed">${item.desc}</p>
          </div>

          <!-- Color palette details -->
          <div class="bg-darkBg p-3.5 rounded-xl border border-borderBg">
            <span class="text-[10px] font-mono uppercase tracking-wider text-zinc-400 block mb-2 flex items-center gap-1.5">
              <i class="fa-solid fa-palette text-accentCyan"></i> 調性配色 / Color Concept
            </span>
            <div class="flex items-center gap-3">
              <div class="flex items-center gap-1">
                ${item.palette.map(c => `<span class="w-5 h-5 rounded-full border border-zinc-700" style="background-color: ${c}"></span>`).join('')}
              </div>
              <p class="text-xs text-zinc-400">${item.colorDesc}</p>
            </div>
          </div>

          <!-- Items list -->
          <div class="border-t border-borderBg pt-5">
            <h4 class="text-xs font-mono uppercase text-zinc-400 tracking-wider mb-3 flex items-center gap-2">
              <i class="fa-solid fa-list-check text-accentOrange"></i> 穿搭單品與著用解析 / Breakdown
            </h4>
            <div class="space-y-2">
              ${item.items.map(it => `
                <div class="flex items-center justify-between p-3 bg-darkBg border border-borderBg rounded-xl text-xs text-zinc-200">
                  <span class="flex items-center gap-2">
                    <i class="fa-solid fa-tag text-accentOrange"></i> ${it}
                  </span>
                  <button onclick="quickAddWishlist('${it}')" class="text-[11px] text-accentCyan hover:underline font-mono">
                    + 加入願望清單
                  </button>
                </div>
              `).join('')}
            </div>
          </div>
        </div>
      `;

      document.getElementById('modal-outfit').classList.remove('hidden');
    }

    function closeOutfitModal() {
      document.getElementById('modal-outfit').classList.add('hidden');
    }

    /* Wishlist Operations */
    function toggleWishlistModal(show) {
      document.getElementById('modal-wishlist').classList.toggle('hidden', !show);
    }

    function saveWishlistItem(e) {
      e.preventDefault();
      const name = document.getElementById('ws-name').value;
      const brand = document.getElementById('ws-brand').value || '獨立街頭品牌';
      const category = document.getElementById('ws-category').value;
      const price = document.getElementById('ws-price').value;
      const image = document.getElementById('ws-image').value || 'https://images.unsplash.com/photo-1523381210434-271e8be1f52b?auto=format&fit=crop&w=600&q=80';
      const note = document.getElementById('ws-note').value;

      const newItem = {
        id: 'ws-' + Date.now(),
        name,
        brand,
        category,
        price: price ? parseInt(price) : null,
        image,
        note,
        purchased: false,
        createdAt: new Date().toLocaleDateString()
      };

      wishlistItems.unshift(newItem);
      persistWishlist();
      renderWishlist();

      document.getElementById('wishlist-form').reset();
      toggleWishlistModal(false);
    }

    function quickAddWishlist(itemName) {
      const newItem = {
        id: 'ws-' + Date.now(),
        name: itemName,
        brand: '街頭精選單品',
        category: '配件 Accessory',
        price: null,
        image: 'https://images.unsplash.com/photo-1523381210434-271e8be1f52b?auto=format&fit=crop&w=600&q=80',
        note: '來自今日推薦的搭配拆解清單',
        purchased: false,
        createdAt: new Date().toLocaleDateString()
      };

      wishlistItems.unshift(newItem);
      persistWishlist();
      renderWishlist();
      closeOutfitModal();
      switchTab('wishlist');
    }

    function togglePurchaseStatus(id) {
      wishlistItems = wishlistItems.map(item => {
        if (item.id === id) {
          return { ...item, purchased: !item.purchased };
        }
        return item;
      });
      persistWishlist();
      renderWishlist();
    }

    function deleteWishlistItem(id) {
      wishlistItems = wishlistItems.filter(item => item.id !== id);
      persistWishlist();
      renderWishlist();
    }

    function persistWishlist() {
      localStorage.setItem('streetvibe_wishlist', JSON.stringify(wishlistItems));
    }

    function renderWishlist() {
      const grid = document.getElementById('wishlist-grid');
      const emptyState = document.getElementById('wishlist-empty');
      const badge = document.getElementById('wishlist-badge');

      if (wishlistItems.length > 0) {
        badge.innerText = wishlistItems.length;
        badge.classList.remove('hidden');
      } else {
        badge.classList.add('hidden');
      }

      if (wishlistItems.length === 0) {
        grid.innerHTML = '';
        emptyState.classList.remove('hidden');
        return;
      }

      emptyState.classList.add('hidden');
      grid.innerHTML = wishlistItems.map(item => `
        <div class="bg-cardBg border ${item.purchased ? 'border-borderBg opacity-60' : 'border-borderBg'} rounded-2xl overflow-hidden flex flex-col justify-between relative group">
          <div>
            <div class="h-48 overflow-hidden bg-darkBg relative">
              <img src="${item.image}" alt="${item.name}" class="w-full h-full object-cover">
              <span class="absolute top-2 left-2 px-2 py-0.5 bg-black/80 text-zinc-300 font-mono text-[10px] rounded border border-borderBg">${item.category || '單品'}</span>
              ${item.purchased ? `
                <div class="absolute inset-0 bg-black/75 flex items-center justify-center">
                  <span class="px-3 py-1 bg-accentCyan text-black font-extrabold text-xs uppercase tracking-wider rounded-md font-mono">已購入 BOUGHT</span>
                </div>
              ` : ''}
              <button onclick="deleteWishlistItem('${item.id}')" class="absolute top-2 right-2 w-7 h-7 bg-black/80 text-zinc-400 hover:text-red-400 rounded-full flex items-center justify-center text-xs transition">
                <i class="fa-solid fa-trash"></i>
              </button>
            </div>

            <div class="p-5">
              <div class="flex items-center justify-between text-xs text-zinc-500 font-mono mb-1">
                <span>${item.brand}</span>
                <span>${item.createdAt}</span>
              </div>
              <h4 class="font-bold text-white text-base font-display ${item.purchased ? 'line-through text-zinc-400' : ''}">${item.name}</h4>
              
              <div class="mt-2 text-sm font-extrabold text-accentOrange">
                ${item.price ? `NT$ ${item.price.toLocaleString()}` : '未標註價格'}
              </div>

              ${item.note ? `
                <p class="text-xs text-zinc-400 mt-3 bg-darkBg p-2.5 rounded-lg border border-borderBg/50 leading-relaxed">${item.note}</p>
              ` : ''}
            </div>
          </div>

          <div class="p-5 pt-0">
            <button onclick="togglePurchaseStatus('${item.id}')" class="w-full py-2.5 ${item.purchased ? 'bg-darkBg border border-borderBg text-zinc-400' : 'bg-accentCyan/10 border border-accentCyan/30 text-accentCyan hover:bg-accentCyan/20'} text-xs font-mono rounded-lg transition font-bold">
              ${item.purchased ? '標示為未購買' : '標示為已購入'}
            </button>
          </div>
        </div>
      `).join('');
    }
  </script>
</body>
</html>
