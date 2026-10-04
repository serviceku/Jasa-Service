<!DOCTYPE html>
<html lang="id" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Serviceku - Jasa Service Elektronik Terbaik & Bergaransi</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- FontAwesome Icons -->
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css" rel="stylesheet">
    <!-- Google Fonts: Plus Jakarta Sans -->
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Plus Jakarta Sans', 'sans-serif'],
                    },
                    colors: {
                        brand: {
                            50: '#f0f7ff',
                            100: '#e0effe',
                            200: '#bae0fd',
                            500: '#3b82f6',
                            600: '#2563eb',
                            700: '#1d4ed8',
                            800: '#1e40af',
                            900: '#0f172a',
                            yellow: '#fbbf24',
                            amber: '#f59e0b'
                        }
                    },
                    boxShadow: {
                        'glow': '0 0 25px -5px rgba(37, 99, 235, 0.3)',
                        'card-hover': '0 20px 30px -10px rgba(0, 0, 0, 0.08), 0 8px 10px -6px rgba(0, 0, 0, 0.04)'
                    }
                }
            }
        }
    </script>

    <style>
        .glass-header {
            background: rgba(15, 23, 42, 0.85);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }
        .glass-card {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(226, 232, 240, 0.8);
        }
        .hero-slide {
            opacity: 0;
            transition: opacity 1.2s ease-in-out, transform 1.2s ease-in-out;
            position: absolute;
            inset: 0;
            transform: scale(1.05);
            pointer-events: none;
        }
        .hero-slide.active {
            opacity: 1;
            transform: scale(1);
            pointer-events: auto;
        }
        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-8px); }
        }
        .animate-float {
            animation: float 4s ease-in-out infinite;
        }
        @keyframes pulse-subtle {
            0%, 100% { transform: scale(1); opacity: 1; }
            50% { transform: scale(1.08); opacity: 0.9; }
        }
        .animate-pulse-subtle {
            animation: pulse-subtle 2s infinite ease-in-out;
        }
        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #f1f5f9;
        }
        ::-webkit-scrollbar-thumb {
            background: #cbd5e1;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #94a3b8;
        }
    </style>
</head>
<body class="bg-slate-50 text-slate-800 antialiased flex flex-col min-h-screen font-sans selection:bg-brand-600 selection:text-white">

    <div class="bg-gradient-to-r from-brand-900 via-brand-800 to-slate-900 text-slate-200 text-xs py-2 px-4 border-b border-white/10 hidden sm:block">
        <div class="max-w-7xl mx-auto flex justify-between items-center">
            <div class="flex items-center space-x-6">
                <span><i class="fas fa-map-marker-alt text-brand-yellow mr-1.5"></i> Coverage: Indramayu, Cirebon & Majalengka</span>
                <span><i class="fas fa-clock text-emerald-400 mr-1.5"></i> Buka Setiap Hari: 08.00 - 18.00 WIB</span>
            </div>
            <div class="flex items-center space-x-4">
                <a href="tel:087874417978" class="hover:text-brand-yellow transition-colors flex items-center gap-1">
                    <i class="fas fa-phone-alt"></i> Call Center: 0878-7441-7978
                </a>
            </div>
        </div>
    </div>

    <nav class="sticky top-0 z-50 glass-header transition-all duration-300 shadow-lg" id="navbar">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between h-20 items-center">
                <!-- Logo & Brand -->
                <div class="flex-shrink-0 flex items-center gap-3 cursor-pointer group" onclick="window.scrollTo({top: 0, behavior: 'smooth'})">
                    <div class="relative">
                        <img class="h-11 w-11 object-cover rounded-xl border border-white/20 shadow-md group-hover:scale-105 transition-transform" 
                             src="https://lh3.googleusercontent.com/d/1L2CtZvTu4_T8ji_R1u72kLdQbhdjoFzw" 
                             alt="Serviceku Logo" 
                             onerror="this.src='https://images.unsplash.com/photo-1621905251189-08b45d6a269e?auto=format&fit=crop&w=100&q=80'">
                        <span class="absolute -bottom-1 -right-1 flex h-3.5 w-3.5">
                            <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-emerald-400 opacity-75"></span>
                            <span class="relative inline-flex rounded-full h-3.5 w-3.5 bg-emerald-500 border-2 border-slate-900"></span>
                        </span>
                    </div>
                    <div>
                        <span class="font-black text-xl text-white tracking-wider block leading-none">SERVICE<span class="text-brand-yellow">KU</span></span>
                        <span class="text-[10px] text-slate-300 font-medium tracking-widest uppercase block mt-1">Teknisi Panggilan Terbaik</span>
                    </div>
                </div>

                <!-- Desktop Nav Links -->
                <div class="hidden md:flex items-center space-x-1">
                    <a href="#katalog" class="text-slate-200 hover:text-white hover:bg-white/10 px-3.5 py-2 rounded-xl text-sm font-semibold transition-all flex items-center gap-2">
                        <i class="fas fa-th-large text-brand-yellow text-xs"></i> Katalog Layanan
                    </a>
                    <a href="#area" class="text-slate-200 hover:text-white hover:bg-white/10 px-3.5 py-2 rounded-xl text-sm font-semibold transition-all flex items-center gap-2">
                        <i class="fas fa-map-marked-alt text-brand-yellow text-xs"></i> Area Layanan
                    </a>
                    <a href="#testimoni" class="text-slate-200 hover:text-white hover:bg-white/10 px-3.5 py-2 rounded-xl text-sm font-semibold transition-all flex items-center gap-2">
                        <i class="fas fa-star text-brand-yellow text-xs"></i> Testimoni
                    </a>
                    <a href="#faq" class="text-slate-200 hover:text-white hover:bg-white/10 px-3.5 py-2 rounded-xl text-sm font-semibold transition-all flex items-center gap-2">
                        <i class="fas fa-question-circle text-brand-yellow text-xs"></i> FAQ
                    </a>
                </div>
                
                <!-- Action Buttons -->
                <div class="flex items-center space-x-2 sm:space-x-3">
                    <a href="https://wa.me/6287874417978?text=Halo%20Serviceku,%20saya%20ingin%20konsultasi%20service%20elektronik." 
                       target="_blank" 
                       class="bg-emerald-500 hover:bg-emerald-600 active:scale-95 text-white px-3.5 sm:px-4 py-2.5 rounded-xl text-xs sm:text-sm font-bold shadow-lg shadow-emerald-500/25 transition-all flex items-center gap-2">
                        <i class="fab fa-whatsapp text-lg"></i> 
                        <span class="hidden sm:inline">Order via WA</span>
                    </a>
                    <button id="authNavBtn" onclick="handleAuthClick()" class="bg-brand-600 hover:bg-brand-700 active:scale-95 text-white px-3.5 py-2.5 rounded-xl text-xs sm:text-sm font-bold shadow-lg shadow-brand-500/25 transition-all flex items-center gap-1.5">
                        <i class="fas fa-user-shield"></i> 
                        <span id="authNavText">Admin Login</span>
                    </button>
                    <!-- Mobile Menu Toggle Button -->
                    <button onclick="toggleMobileMenu()" class="md:hidden text-slate-200 hover:text-white p-2 rounded-xl focus:outline-none">
                        <i id="mobileMenuIcon" class="fas fa-bars text-xl"></i>
                    </button>
                </div>
            </div>
        </div>

        <div id="mobileMenu" class="hidden md:hidden bg-slate-900/95 border-b border-white/10 px-4 pt-2 pb-6 space-y-3 backdrop-blur-lg">
            <a href="#katalog" onclick="toggleMobileMenu()" class="block text-slate-200 hover:text-brand-yellow py-2 px-3 rounded-lg text-sm font-medium">
                <i class="fas fa-th-large w-6 text-brand-yellow"></i> Katalog Jasa
            </a>
            <a href="#area" onclick="toggleMobileMenu()" class="block text-slate-200 hover:text-brand-yellow py-2 px-3 rounded-lg text-sm font-medium">
                <i class="fas fa-map-marked-alt w-6 text-brand-yellow"></i> Area Service Panggilan
            </a>
            <a href="#testimoni" onclick="toggleMobileMenu()" class="block text-slate-200 hover:text-brand-yellow py-2 px-3 rounded-lg text-sm font-medium">
                <i class="fas fa-star w-6 text-brand-yellow"></i> Ulasan Pelanggan
            </a>
            <a href="#faq" onclick="toggleMobileMenu()" class="block text-slate-200 hover:text-brand-yellow py-2 px-3 rounded-lg text-sm font-medium">
                <i class="fas fa-question-circle w-6 text-brand-yellow"></i> Pertanyaan Sering Diajukan
            </a>
        </div>
    </nav>

    <header class="relative min-h-[580px] sm:min-h-[620px] flex items-center justify-center overflow-hidden bg-slate-950 text-white pt-10 pb-16">
        <!-- Background Slideshow -->
        <div id="slideshowContainer" class="absolute inset-0 z-0">
            <div class="hero-slide active bg-cover bg-center" style="background-image: linear-gradient(to bottom, rgba(15,23,42,0.75), rgba(15,23,42,0.92)), url('https://images.unsplash.com/photo-1581092160562-40aa08e78837?auto=format&fit=crop&w=1920&q=80');"></div>
            <div class="hero-slide bg-cover bg-center" style="background-image: linear-gradient(to bottom, rgba(15,23,42,0.75), rgba(15,23,42,0.92)), url('https://images.unsplash.com/photo-1584622650111-993a426fbf0a?auto=format&fit=crop&w=1920&q=80');"></div>
            <div class="hero-slide bg-cover bg-center" style="background-image: linear-gradient(to bottom, rgba(15,23,42,0.75), rgba(15,23,42,0.92)), url('https://images.unsplash.com/photo-1599839619722-39751411ea63?auto=format&fit=crop&w=1920&q=80');"></div>
        </div>

        <!-- Overlay Decor Grid -->
        <div class="absolute inset-0 z-10 bg-[radial-gradient(#3b82f6_1px,transparent_1px)] [background-size:24px_24px] opacity-15 pointer-events-none"></div>

        <!-- Hero Content Container -->
        <div class="relative z-20 max-w-5xl mx-auto px-4 sm:px-6 text-center">
            <!-- Trust Badge Pill -->
            <div class="inline-flex items-center gap-2 bg-gradient-to-r from-amber-500/20 via-brand-500/20 to-amber-500/20 border border-amber-400/40 rounded-full px-4 py-1.5 mb-6 backdrop-blur-md shadow-inner animate-float">
                <span class="text-brand-yellow font-extrabold text-xs tracking-wider uppercase flex items-center gap-1.5">
                    <i class="fas fa-shield-halved text-sm"></i> Garansi Resmi 1 Bulan Full Service
                </span>
            </div>

            <!-- Title & Subtitle -->
            <h1 id="mainHeroTitle" class="text-3xl sm:text-5xl lg:text-6xl font-extrabold tracking-tight leading-tight text-white mb-6 drop-shadow-md">
                Jasa Service Elektronik <span class="text-transparent bg-clip-text bg-gradient-to-r from-brand-yellow via-amber-300 to-amber-500">Profesional & Panggilan</span>
            </h1>
            <p id="mainHeroSubtitle" class="text-base sm:text-xl text-slate-300 font-normal max-w-3xl mx-auto mb-10 leading-relaxed">
                Melayani Perbaikan AC, Kulkas, Mesin Cuci, Showcase, Freezer Box & Dispenser. Teknisi jujur, cepat & langsung datang ke rumah Anda di <strong class="text-white font-semibold">Indramayu, Cirebon, & Majalengka</strong>.
            </p>

            <!-- Call to Action Buttons -->
            <div class="flex flex-col sm:flex-row justify-center items-center gap-4 max-w-md mx-auto sm:max-w-none">
                <a href="#katalog" class="w-full sm:w-auto bg-gradient-to-r from-brand-yellow to-amber-500 hover:from-amber-400 hover:to-amber-500 text-slate-950 font-extrabold px-8 py-4 rounded-2xl shadow-xl shadow-amber-500/20 transition-all hover:scale-[1.03] active:scale-95 flex items-center justify-center gap-3 text-base">
                    <i class="fas fa-th-large"></i> Lihat Katalog & Price List
                </a>
                <a href="https://wa.me/6287874417978?text=Halo%20Serviceku,%20saya%20butuh%20teknisi%20datang%20ke%20rumah." 
                   target="_blank" 
                   class="w-full sm:w-auto bg-white/10 hover:bg-white/20 backdrop-blur-md text-white border border-white/20 font-bold px-8 py-4 rounded-2xl shadow-lg transition-all hover:scale-[1.03] active:scale-95 flex items-center justify-center gap-3 text-base">
                    <i class="fab fa-whatsapp text-emerald-400 text-xl"></i> Panggil Teknisi Sekarang
                </a>
                <button id="adminEditBannerBtn" onclick="openBannerModal()" class="hidden w-full sm:w-auto bg-brand-600/80 hover:bg-brand-600 backdrop-blur-md text-white font-semibold px-6 py-4 rounded-2xl transition-all border border-brand-400/30 flex items-center justify-center gap-2 text-sm">
                    <i class="fas fa-edit"></i> Edit Banner Admin
                </button>
            </div>

            <!-- Slideshow Dot Indicators -->
            <div class="flex justify-center items-center space-x-2 mt-12" id="slideshowDots">
                <button onclick="setSlide(0)" class="w-8 h-2 rounded-full bg-brand-yellow transition-all" aria-label="Slide 1"></button>
                <button onclick="setSlide(1)" class="w-2 h-2 rounded-full bg-white/40 hover:bg-white/80 transition-all" aria-label="Slide 2"></button>
                <button onclick="setSlide(2)" class="w-2 h-2 rounded-full bg-white/40 hover:bg-white/80 transition-all" aria-label="Slide 3"></button>
            </div>
        </div>
    </header>

    <section class="bg-gradient-to-r from-slate-900 via-brand-900 to-slate-900 text-white py-8 border-y border-white/10 shadow-xl relative z-30">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-2 md:grid-cols-4 gap-6 text-center">
                <div class="p-4 rounded-2xl bg-white/5 border border-white/10 hover:border-brand-500/40 transition-all hover:-translate-y-1">
                    <div class="w-12 h-12 rounded-2xl bg-brand-600/30 border border-brand-500/30 flex items-center justify-center text-brand-yellow text-xl mx-auto mb-3 shadow-inner">
                        <i class="fas fa-shield-alt"></i>
                    </div>
                    <h4 class="font-bold text-sm sm:text-base text-white">Garansi 30 Hari</h4>
                    <p class="text-xs text-slate-300 mt-1">Jaminan pengerjaan tuntas</p>
                </div>
                <div class="p-4 rounded-2xl bg-white/5 border border-white/10 hover:border-brand-500/40 transition-all hover:-translate-y-1">
                    <div class="w-12 h-12 rounded-2xl bg-brand-600/30 border border-brand-500/30 flex items-center justify-center text-brand-yellow text-xl mx-auto mb-3 shadow-inner">
                        <i class="fas fa-user-check"></i>
                    </div>
                    <h4 class="font-bold text-sm sm:text-base text-white">Teknisi Ahli</h4>
                    <p class="text-xs text-slate-300 mt-1">Jujur, Handal & Amanah</p>
                </div>
                <div class="p-4 rounded-2xl bg-white/5 border border-white/10 hover:border-brand-500/40 transition-all hover:-translate-y-1">
                    <div class="w-12 h-12 rounded-2xl bg-brand-600/30 border border-brand-500/30 flex items-center justify-center text-brand-yellow text-xl mx-auto mb-3 shadow-inner">
                        <i class="fas fa-bolt"></i>
                    </div>
                    <h4 class="font-bold text-sm sm:text-base text-white">Respon Cepat</h4>
                    <p class="text-xs text-slate-300 mt-1">Teknisi siap ke lokasi Anda</p>
                </div>
                <div class="p-4 rounded-2xl bg-white/5 border border-white/10 hover:border-brand-500/40 transition-all hover:-translate-y-1">
                    <div class="w-12 h-12 rounded-2xl bg-brand-600/30 border border-brand-500/30 flex items-center justify-center text-brand-yellow text-xl mx-auto mb-3 shadow-inner">
                        <i class="fas fa-tags"></i>
                    </div>
                    <h4 class="font-bold text-sm sm:text-base text-white">Harga Transparan</h4>
                    <p class="text-xs text-slate-300 mt-1">Tanpa biaya tersembunyi</p>
                </div>
            </div>
        </div>
    </section>

    <main class="flex-grow py-16">
        <section id="katalog" class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <!-- Section Header -->
            <div class="flex flex-col md:flex-row justify-between items-start md:items-end mb-8 gap-4 border-b border-slate-200 pb-6">
                <div>
                    <span class="inline-block bg-brand-100 text-brand-700 font-extrabold text-xs px-3 py-1 rounded-full uppercase tracking-wider mb-2">
                        <i class="fas fa-list-check mr-1"></i> Layanan Terlengkap
                    </span>
                    <h2 class="text-3xl sm:text-4xl font-extrabold text-slate-900 tracking-tight">Katalog & Tarif Layanan Service</h2>
                    <p class="text-slate-600 text-sm mt-1">Pilih jasa yang Anda butuhkan dan hubungi teknisi secara langsung via WhatsApp.</p>
                </div>
                <!-- Admin Add Button -->
                <div id="adminAddContainer" class="hidden flex-shrink-0">
                    <button onclick="openServiceModal()" class="bg-gradient-to-r from-brand-600 to-brand-700 hover:from-brand-700 hover:to-brand-800 text-white px-5 py-3 rounded-2xl font-bold shadow-lg shadow-brand-500/20 transition-all flex items-center gap-2 text-sm">
                        <i class="fas fa-plus-circle text-lg"></i> Tambah Jasa Baru
                    </button>
                </div>
            </div>

            <!-- Search and Category Filter Toolbar -->
            <div class="mb-8 flex flex-col md:flex-row gap-4 justify-between items-center bg-white p-4 rounded-2xl shadow-sm border border-slate-200">
                <!-- Search Input -->
                <div class="relative w-full md:w-80">
                    <i class="fas fa-search absolute left-4 top-1/2 -translate-y-1/2 text-slate-400"></i>
                    <input type="text" id="searchInput" oninput="filterServices()" placeholder="Cari jasa (AC, Kulkas, dll)..." 
                           class="w-full pl-11 pr-4 py-2.5 rounded-xl border border-slate-200 focus:outline-none focus:ring-2 focus:ring-brand-500 text-sm">
                </div>

                <!-- Category Filters -->
                <div class="flex flex-wrap gap-2 w-full md:w-auto overflow-x-auto pb-1 md:pb-0" id="categoryFilters">
                    <button onclick="setCategoryFilter('all')" class="cat-btn active bg-brand-600 text-white text-xs font-bold px-4 py-2 rounded-xl transition-all shadow-sm">
                        Semua Jasa
                    </button>
                    <button onclick="setCategoryFilter('ac')" class="cat-btn bg-slate-100 hover:bg-slate-200 text-slate-700 text-xs font-bold px-4 py-2 rounded-xl transition-all">
                        <i class="fas fa-fan mr-1 text-sky-500"></i> AC
                    </button>
                    <button onclick="setCategoryFilter('kulkas')" class="cat-btn bg-slate-100 hover:bg-slate-200 text-slate-700 text-xs font-bold px-4 py-2 rounded-xl transition-all">
                        <i class="fas fa-box text-indigo-500 mr-1"></i> Kulkas & Showcase
                    </button>
                    <button onclick="setCategoryFilter('mesin_cuci')" class="cat-btn bg-slate-100 hover:bg-slate-200 text-slate-700 text-xs font-bold px-4 py-2 rounded-xl transition-all">
                        <i class="fas fa-soap text-emerald-500 mr-1"></i> Mesin Cuci
                    </button>
                </div>
            </div>

            <!-- Loading Spinner -->
            <div id="catalogLoading" class="text-center py-20 bg-white rounded-3xl border border-slate-100 shadow-sm">
                <div class="inline-block animate-spin rounded-full h-12 w-12 border-4 border-brand-600 border-t-transparent mb-3"></div>
                <p class="text-slate-500 font-semibold text-sm">Memuat katalog jasa Serviceku...</p>
            </div>

            <!-- Services Grid -->
            <div id="servicesGrid" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-6">
                <!-- Dynamically populated from Firestore or Default Catalog -->
            </div>

            <!-- Empty State -->
            <div id="emptyCatalogState" class="hidden text-center py-16 bg-slate-100/60 rounded-3xl border border-dashed border-slate-300">
                <i class="fas fa-search-minus text-4xl text-slate-400 mb-3"></i>
                <h3 class="font-bold text-slate-700 text-lg">Tidak ada layanan ditemukan</h3>
                <p class="text-xs text-slate-500">Coba gunakan kata kunci pencarian lain.</p>
            </div>
        </section>

        <section id="area" class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 mt-20">
            <div class="bg-gradient-to-br from-slate-900 via-brand-900 to-slate-950 rounded-3xl p-8 md:p-12 text-white shadow-2xl relative overflow-hidden border border-white/10">
                <div class="absolute -right-20 -top-20 w-80 h-80 bg-brand-500/20 rounded-full blur-3xl pointer-events-none"></div>
                
                <div class="relative z-10 flex flex-col lg:flex-row items-center justify-between gap-10">
                    <div class="max-w-2xl">
                        <span class="bg-emerald-500/20 text-emerald-300 border border-emerald-500/30 text-xs font-extrabold px-3.5 py-1.5 rounded-full uppercase tracking-wider inline-flex items-center gap-1.5">
                            <i class="fas fa-map-marker-alt"></i> Coverage Layanan Panggilan
                        </span>
                        <h3 class="text-3xl sm:text-4xl font-extrabold mt-4 leading-tight">Teknisi Datang Langsung ke Rumah Anda</h3>
                        <p class="text-slate-300 mt-3 text-sm sm:text-base leading-relaxed">
                            Workshop Utama: <strong class="text-white">Jl. By Pass Binaria - Bondan</strong>. Kami siap datang membawa peralatan lengkap & suku cadang asli untuk melayani kebutuhan perbaikan elektronik Anda di wilayah:
                        </p>
                        
                        <div class="mt-6 flex flex-wrap gap-3">
                            <div class="flex items-center gap-2 bg-white/10 backdrop-blur-md px-4 py-2.5 rounded-2xl text-sm font-bold border border-white/10 shadow-sm">
                                <i class="fas fa-city text-brand-yellow"></i> Kabupaten Indramayu
                            </div>
                            <div class="flex items-center gap-2 bg-white/10 backdrop-blur-md px-4 py-2.5 rounded-2xl text-sm font-bold border border-white/10 shadow-sm">
                                <i class="fas fa-city text-brand-yellow"></i> Kota & Kab. Cirebon
                            </div>
                            <div class="flex items-center gap-2 bg-white/10 backdrop-blur-md px-4 py-2.5 rounded-2xl text-sm font-bold border border-white/10 shadow-sm">
                                <i class="fas fa-city text-brand-yellow"></i> Kabupaten Majalengka
                            </div>
                        </div>
                    </div>

                    <!-- Direct WA Card -->
                    <div class="bg-white/10 backdrop-blur-xl p-8 rounded-3xl border border-white/20 text-center flex-shrink-0 w-full lg:w-80 shadow-2xl">
                        <div class="w-16 h-16 bg-emerald-500 text-white rounded-2xl mx-auto flex items-center justify-center text-3xl mb-4 shadow-lg shadow-emerald-500/30 animate-pulse-subtle">
                            <i class="fab fa-whatsapp"></i>
                        </div>
                        <p class="text-xs uppercase font-extrabold tracking-widest text-brand-yellow">Respons Cepat via WhatsApp</p>
                        <a href="https://wa.me/6287874417978" target="_blank" class="mt-2 block text-2xl font-black text-white hover:text-brand-yellow transition-colors tracking-tight">
                            0878-7441-7978
                        </a>
                        <p class="text-xs text-slate-300 mt-2">Bisa Konsultasi & Kirim Foto Kendaraan/Alat Gratis</p>
                        <a href="https://wa.me/6287874417978?text=Halo%20Serviceku,%20saya%20mau%20konsultasi%20kendala%20elektronik." 
                           target="_blank" 
                           class="mt-5 w-full bg-emerald-500 hover:bg-emerald-600 text-white font-bold py-3 px-4 rounded-xl text-xs transition-all flex items-center justify-center gap-2 shadow-lg">
                            <i class="fab fa-whatsapp text-base"></i> Hubungi WhatsApp
                        </a>
                    </div>
                </div>
            </div>
        </section>

        <section id="testimoni" class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 mt-24">
            <div class="text-center mb-12">
                <span class="bg-brand-100 text-brand-700 font-extrabold text-xs px-3.5 py-1.5 rounded-full uppercase tracking-wider">
                    <i class="fas fa-heart text-red-500 mr-1"></i> Kepuasan Pelanggan
                </span>
                <h2 class="text-3xl sm:text-4xl font-extrabold text-slate-900 mt-2">Apa Kata Pelanggan Kami?</h2>
                <p class="text-slate-600 text-sm mt-1 max-w-xl mx-auto">Pengalaman nyata dari warga Indramayu, Cirebon, & Majalengka yang menggunakan jasa Serviceku.</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                <div class="bg-white p-6 rounded-3xl border border-slate-200 shadow-sm hover:shadow-md transition-all">
                    <div class="flex items-center gap-1 text-amber-400 mb-3">
                        <i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i>
                    </div>
                    <p class="text-slate-700 text-sm italic mb-4">"AC rumah mati mendadak saat cuaca panas. Teknisi Serviceku datang cepat ke Indramayu, pengerjaan rapi dan dingin lagi. Mantap!"</p>
                    <div class="flex items-center gap-3">
                        <div class="w-10 h-10 rounded-full bg-brand-100 text-brand-700 font-bold flex items-center justify-center text-sm">
                            BP
                        </div>
                        <div>
                            <h4 class="font-bold text-sm text-slate-900">Bpk. Paksi</h4>
                            <p class="text-xs text-slate-500">Indramayu</p>
                        </div>
                    </div>
                </div>

                <div class="bg-white p-6 rounded-3xl border border-slate-200 shadow-sm hover:shadow-md transition-all">
                    <div class="flex items-center gap-1 text-amber-400 mb-3">
                        <i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i>
                    </div>
                    <p class="text-slate-700 text-sm italic mb-4">"Service kulkas 2 pintu yang tidak dingin. Teknisi jujur, dijelaskan sparepart mana yang rusak dan biayanya sangat bersahabat."</p>
                    <div class="flex items-center gap-3">
                        <div class="w-10 h-10 rounded-full bg-emerald-100 text-emerald-700 font-bold flex items-center justify-center text-sm">
                            IB
                        </div>
                        <div>
                            <h4 class="font-bold text-sm text-slate-900">Ibu Ratna</h4>
                            <p class="text-xs text-slate-500">Cirebon</p>
                        </div>
                    </div>
                </div>

                <div class="bg-white p-6 rounded-3xl border border-slate-200 shadow-sm hover:shadow-md transition-all">
                    <div class="flex items-center gap-1 text-amber-400 mb-3">
                        <i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i>
                    </div>
                    <p class="text-slate-700 text-sm italic mb-4">"Mesin cuci mati total, langsung diperbaiki di tempat tanpa perlu repot diangkut. Sangat direkomendasikan!"</p>
                    <div class="flex items-center gap-3">
                        <div class="w-10 h-10 rounded-full bg-sky-100 text-sky-700 font-bold flex items-center justify-center text-sm">
                            MS
                        </div>
                        <div>
                            <h4 class="font-bold text-sm text-slate-900">Mas Dedi</h4>
                            <p class="text-xs text-slate-500">Majalengka</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="faq" class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 mt-24">
            <div class="text-center mb-10">
                <span class="bg-brand-100 text-brand-700 font-extrabold text-xs px-3.5 py-1.5 rounded-full uppercase tracking-wider">
                    <i class="fas fa-circle-question mr-1"></i> FAQ
                </span>
                <h2 class="text-3xl font-extrabold text-slate-900 mt-2">Pertanyaan Sering Diajukan</h2>
            </div>

            <div class="space-y-4">
                <details class="group bg-white rounded-2xl border border-slate-200 p-5 [&_summary::-webkit-details-marker]:hidden cursor-pointer shadow-sm">
                    <summary class="flex items-center justify-between font-bold text-slate-900 text-sm sm:text-base">
                        <span>Bagaimana cara memesan jasa service panggilan?</span>
                        <span class="ml-1.5 flex-shrink-0 text-brand-600 transition duration-300 group-open:-rotate-180">
                            <i class="fas fa-chevron-down"></i>
                        </span>
                    </summary>
                    <p class="mt-3 text-xs sm:text-sm text-slate-600 leading-relaxed border-t border-slate-100 pt-3">
                        Cukup klik tombol "Order via WA" atau hubungi kami di 0878-7441-7978. Informasikan kendala elektronik Anda, alamat lengkap, dan teknisi kami akan menjadwalkan kedatangan ke rumah Anda.
                    </p>
                </details>

                <details class="group bg-white rounded-2xl border border-slate-200 p-5 [&_summary::-webkit-details-marker]:hidden cursor-pointer shadow-sm">
                    <summary class="flex items-center justify-between font-bold text-slate-900 text-sm sm:text-base">
                        <span>Apakah hasil pengerjaan mendapatkan garansi?</span>
                        <span class="ml-1.5 flex-shrink-0 text-brand-600 transition duration-300 group-open:-rotate-180">
                            <i class="fas fa-chevron-down"></i>
                        </span>
                    </summary>
                    <p class="mt-3 text-xs sm:text-sm text-slate-600 leading-relaxed border-t border-slate-100 pt-3">
                        Ya, seluruh pekerjaan perbaikan dan pengantian sparepart di Serviceku bergaransi resmi selama 1 Bulan (30 Hari) sejak pengerjaan selesai.
                    </p>
                </details>

                <details class="group bg-white rounded-2xl border border-slate-200 p-5 [&_summary::-webkit-details-marker]:hidden cursor-pointer shadow-sm">
                    <summary class="flex items-center justify-between font-bold text-slate-900 text-sm sm:text-base">
                        <span>Berapa biaya untuk pengecekan / diagnosa?</span>
                        <span class="ml-1.5 flex-shrink-0 text-brand-600 transition duration-300 group-open:-rotate-180">
                            <i class="fas fa-chevron-down"></i>
                        </span>
                    </summary>
                    <p class="mt-3 text-xs sm:text-sm text-slate-600 leading-relaxed border-t border-slate-100 pt-3">
                        Tarif pengecekan terjangkau dan disesuaikan dengan jarak lokasi. Jika pengerjaan perbaikan disetujui, biaya pengecekan sudah termasuk dalam total tarif perbaikan.
                    </p>
                </details>
            </div>
        </section>
    </main>

    <footer class="bg-slate-950 text-white pt-16 pb-12 border-t border-slate-800 relative">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 grid grid-cols-1 md:grid-cols-3 gap-10 mb-12">
            <div>
                <div class="flex items-center gap-3 mb-4">
                    <img class="h-10 w-10 object-cover rounded-xl border border-white/20 bg-white/10 p-1" 
                         src="https://lh3.googleusercontent.com/d/1L2CtZvTu4_T8ji_R1u72kLdQbhdjoFzw" 
                         alt="Serviceku Logo" 
                         onerror="this.src='https://images.unsplash.com/photo-1621905251189-08b45d6a269e?auto=format&fit=crop&w=100&q=80'">
                    <span class="font-extrabold text-xl tracking-wider text-white">SERVICE<span class="text-brand-yellow">KU</span></span>
                </div>
                <p class="text-slate-400 text-sm leading-relaxed mb-4">
                    Jasa service elektronik terpercaya untuk AC, Kulkas, Mesin Cuci, Dispenser, Showcase, dan Freezer Box dengan teknisi handal & bergaransi 30 hari.
                </p>
                <div class="flex space-x-3 text-slate-400">
                    <a href="#" class="w-9 h-9 rounded-xl bg-white/5 hover:bg-brand-600 hover:text-white flex items-center justify-center transition-all"><i class="fab fa-facebook-f"></i></a>
                    <a href="#" class="w-9 h-9 rounded-xl bg-white/5 hover:bg-emerald-600 hover:text-white flex items-center justify-center transition-all"><i class="fab fa-whatsapp"></i></a>
                    <a href="#" class="w-9 h-9 rounded-xl bg-white/5 hover:bg-brand-600 hover:text-white flex items-center justify-center transition-all"><i class="fab fa-instagram"></i></a>
                </div>
            </div>

            <div>
                <h4 class="font-extrabold text-base mb-4 text-brand-yellow uppercase tracking-wider text-xs">Kontak & Workshop</h4>
                <p class="text-slate-300 text-sm mb-3 flex items-start gap-2.5">
                    <i class="fas fa-map-marker-alt text-brand-yellow mt-1"></i>
                    <span>Jl. By Pass Binaria - Bondan (Siap Panggilan Indramayu, Cirebon, Majalengka)</span>
                </p>
                <p class="text-slate-300 text-sm mb-3 flex items-center gap-2.5">
                    <i class="fab fa-whatsapp text-emerald-400 text-base"></i>
                    <a href="https://wa.me/6287874417978" target="_blank" class="hover:text-emerald-400 transition-colors">+62 878-7441-7978</a>
                </p>
                <p class="text-slate-300 text-sm flex items-center gap-2.5">
                    <i class="fas fa-envelope text-sky-400"></i>
                    <span>info@serviceku.id</span>
                </p>
            </div>

            <div>
                <h4 class="font-extrabold text-base mb-4 text-brand-yellow uppercase tracking-wider text-xs">Jam Operasional</h4>
                <div class="bg-white/5 p-4 rounded-2xl border border-white/10">
                    <div class="flex justify-between items-center text-xs text-slate-300 mb-2">
                        <span>Senin - Minggu:</span>
                        <span class="font-bold text-white">08.00 - 18.00 WIB</span>
                    </div>
                    <p class="text-[11px] text-emerald-400 font-semibold flex items-center gap-1 mt-2">
                        <i class="fas fa-check-circle"></i> Layanan Panggilan Darurat Tersedia
                    </p>
                </div>
            </div>
        </div>

        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 pt-6 border-t border-slate-800/80 flex flex-col sm:flex-row justify-between items-center text-xs text-slate-500 gap-4">
            <p>&copy; 2026 Serviceku. Hak Cipta Dilindungi.</p>
            <p>Jasa Service Elektronik Indramayu • Cirebon • Majalengka</p>
        </div>
    </footer>

    <a href="https://wa.me/6287874417978?text=Halo%20Serviceku,%20saya%20ingin%20tanya%20jasa%20service." 
       target="_blank" 
       class="fixed bottom-6 right-6 z-40 bg-emerald-500 hover:bg-emerald-600 text-white p-3.5 rounded-2xl shadow-2xl shadow-emerald-500/50 transition-all hover:scale-110 flex items-center gap-3 group">
        <span class="max-w-0 overflow-hidden whitespace-nowrap group-hover:max-w-xs transition-all duration-300 text-xs font-bold pl-1">
            Chat WhatsApp Teknisi
        </span>
        <div class="relative">
            <i class="fab fa-whatsapp text-2xl"></i>
            <span class="absolute -top-1 -right-1 flex h-3 w-3">
                <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-emerald-300 opacity-75"></span>
                <span class="relative inline-flex rounded-full h-3 w-3 bg-white"></span>
            </span>
        </div>
    </a>

    <div id="loginModal" class="fixed inset-0 z-50 bg-slate-950/70 backdrop-blur-md hidden flex items-center justify-center p-4">
        <div class="bg-white rounded-3xl max-w-md w-full p-8 shadow-2xl relative border border-slate-100">
            <button onclick="closeLoginModal()" class="absolute top-5 right-5 text-slate-400 hover:text-slate-700 text-xl w-8 h-8 flex items-center justify-center rounded-full hover:bg-slate-100 transition-all">
                <i class="fas fa-times"></i>
            </button>
            
            <div class="text-center mb-6">
                <div class="w-16 h-16 bg-brand-100 text-brand-600 rounded-2xl mx-auto flex items-center justify-center text-2xl mb-3 shadow-inner">
                    <i class="fas fa-user-shield"></i>
                </div>
                <h3 class="text-2xl font-black text-slate-900">Admin Login</h3>
                <p class="text-xs text-slate-500 mt-1">Masuk untuk mengelola katalog jasa & banner</p>
            </div>

            <form id="loginForm" onsubmit="handleLogin(event)" class="space-y-4">
                <div>
                    <label class="block text-xs font-bold text-slate-700 uppercase tracking-wider mb-1">Username Admin</label>
                    <input type="text" id="adminUser" required class="w-full px-4 py-3 rounded-xl border border-slate-300 focus:ring-2 focus:ring-brand-500 focus:outline-none text-sm" placeholder="Masukkan username admin">
                </div>
                <div>
                    <label class="block text-xs font-bold text-slate-700 uppercase tracking-wider mb-1">Password</label>
                    <div class="relative">
                        <input type="password" id="adminPass" required class="w-full px-4 py-3 rounded-xl border border-slate-300 focus:ring-2 focus:ring-brand-500 focus:outline-none text-sm pr-12" placeholder="Masukkan password">
                        <button type="button" onclick="togglePasswordVisibility()" class="absolute right-4 top-1/2 -translate-y-1/2 text-slate-400 hover:text-slate-600">
                            <i id="eyeIcon" class="fas fa-eye"></i>
                        </button>
                    </div>
                </div>

                <div id="loginError" class="text-red-500 text-xs font-bold hidden text-center bg-red-50 py-2 px-3 rounded-lg border border-red-200"></div>

                <button type="submit" class="w-full bg-brand-600 hover:bg-brand-700 text-white font-extrabold py-3.5 rounded-xl shadow-lg shadow-brand-500/30 transition-all text-sm">
                    Masuk Dashboard
                </button>
            </form>
        </div>
    </div>

    <div id="serviceModal" class="fixed inset-0 z-50 bg-slate-950/70 backdrop-blur-md hidden flex items-center justify-center p-4">
        <div class="bg-white rounded-3xl max-w-lg w-full p-8 shadow-2xl relative max-h-[90vh] overflow-y-auto border border-slate-100">
            <button onclick="closeServiceModal()" class="absolute top-5 right-5 text-slate-400 hover:text-slate-700 text-xl w-8 h-8 flex items-center justify-center rounded-full hover:bg-slate-100 transition-all">
                <i class="fas fa-times"></i>
            </button>
            
            <h3 id="modalServiceTitle" class="text-2xl font-black text-slate-900 mb-6">Tambah Jasa Baru</h3>
            
            <form id="serviceForm" onsubmit="handleSaveService(event)" class="space-y-4">
                <input type="hidden" id="serviceId">
                <div>
                    <label class="block text-xs font-bold text-slate-700 uppercase tracking-wider mb-1">Nama Jasa / Barang</label>
                    <input type="text" id="serviceName" required class="w-full px-4 py-3 rounded-xl border border-slate-300 focus:ring-2 focus:ring-brand-500 focus:outline-none text-sm" placeholder="Contoh: Cuci AC / Perbaikan Kulkas 2 Pintu">
                </div>
                <div>
                    <label class="block text-xs font-bold text-slate-700 uppercase tracking-wider mb-1">Kategori Jasa</label>
                    <select id="serviceCategory" class="w-full px-4 py-3 rounded-xl border border-slate-300 focus:ring-2 focus:ring-brand-500 focus:outline-none text-sm bg-white">
                        <option value="ac">Service AC</option>
                        <option value="kulkas">Kulkas & Showcase / Freezer</option>
                        <option value="mesin_cuci">Mesin Cuci</option>
                        <option value="lainnya">Lainnya / Dispenser</option>
                    </select>
                </div>
                <div>
                    <label class="block text-xs font-bold text-slate-700 uppercase tracking-wider mb-1">Tarif / Harga (Contoh: 75.000 atau Mulai 100rb)</label>
                    <input type="text" id="servicePrice" required class="w-full px-4 py-3 rounded-xl border border-slate-300 focus:ring-2 focus:ring-brand-500 focus:outline-none text-sm" placeholder="Contoh: 75.000 atau 350.000">
                </div>
                <div>
                    <label class="block text-xs font-bold text-slate-700 uppercase tracking-wider mb-1">URL Foto Jasa</label>
                    <input type="url" id="serviceImage" required class="w-full px-4 py-3 rounded-xl border border-slate-300 focus:ring-2 focus:ring-brand-500 focus:outline-none text-sm" placeholder="https://images.unsplash.com/photo-...">
                    <p class="text-[11px] text-slate-400 mt-1">Masukkan URL gambar langsung dari Unsplash / web publik.</p>
                </div>
                <div>
                    <label class="block text-xs font-bold text-slate-700 uppercase tracking-wider mb-1">Deskripsi Singkat / Catatan Pengerjaan</label>
                    <textarea id="serviceDesc" rows="3" class="w-full px-4 py-3 rounded-xl border border-slate-300 focus:ring-2 focus:ring-brand-500 focus:outline-none text-sm" placeholder="Contoh: Pengecekan menyeluruh, pembersihan unit indoor & outdoor, teknisi ke rumah."></textarea>
                </div>
                <div class="flex gap-3 pt-3">
                    <button type="button" onclick="closeServiceModal()" class="w-1/2 bg-slate-100 hover:bg-slate-200 text-slate-700 font-bold py-3.5 rounded-xl transition-all text-sm">Batal</button>
                    <button type="submit" class="w-1/2 bg-brand-600 hover:bg-brand-700 text-white font-extrabold py-3.5 rounded-xl shadow-lg shadow-brand-500/20 transition-all text-sm">Simpan Jasa</button>
                </div>
            </form>
        </div>
    </div>

    <div id="bannerModal" class="fixed inset-0 z-50 bg-slate-950/70 backdrop-blur-md hidden flex items-center justify-center p-4">
        <div class="bg-white rounded-3xl max-w-md w-full p-8 shadow-2xl relative border border-slate-100">
            <button onclick="closeBannerModal()" class="absolute top-5 right-5 text-slate-400 hover:text-slate-700 text-xl w-8 h-8 flex items-center justify-center rounded-full hover:bg-slate-100 transition-all">
                <i class="fas fa-times"></i>
            </button>
            <h3 class="text-2xl font-black text-slate-900 mb-6">Edit Teks Banner Utama</h3>
            <form onsubmit="handleSaveBanner(event)" class="space-y-4">
                <div>
                    <label class="block text-xs font-bold text-slate-700 uppercase tracking-wider mb-1">Judul Utama</label>
                    <input type="text" id="bannerTitleInput" required class="w-full px-4 py-3 rounded-xl border border-slate-300 focus:ring-2 focus:ring-brand-500 focus:outline-none text-sm">
                </div>
                <div>
                    <label class="block text-xs font-bold text-slate-700 uppercase tracking-wider mb-1">Subjudul / Deskripsi Banner</label>
                    <textarea id="bannerSubtitleInput" rows="3" required class="w-full px-4 py-3 rounded-xl border border-slate-300 focus:ring-2 focus:ring-brand-500 focus:outline-none text-sm"></textarea>
                </div>
                <div class="flex gap-3 pt-2">
                    <button type="button" onclick="closeBannerModal()" class="w-1/2 bg-slate-100 hover:bg-slate-200 text-slate-700 font-bold py-3.5 rounded-xl transition-all text-sm">Batal</button>
                    <button type="submit" class="w-1/2 bg-brand-600 hover:bg-brand-700 text-white font-extrabold py-3.5 rounded-xl shadow-lg shadow-brand-500/20 transition-all text-sm">Simpan Teks</button>
                </div>
            </form>
        </div>
    </div>

    <div id="deleteConfirmModal" class="fixed inset-0 z-50 bg-slate-950/70 backdrop-blur-md hidden flex items-center justify-center p-4">
        <div class="bg-white rounded-3xl max-w-sm w-full p-6 text-center shadow-2xl border border-slate-100">
            <div class="w-14 h-14 bg-red-100 text-red-600 rounded-2xl mx-auto flex items-center justify-center text-2xl mb-4">
                <i class="fas fa-exclamation-triangle"></i>
            </div>
            <h3 class="text-xl font-extrabold text-slate-900 mb-2">Hapus Layanan Ini?</h3>
            <p class="text-xs text-slate-500 mb-6">Tindakan ini tidak dapat dibatalkan. Layanan akan dihapus dari katalog.</p>
            <div class="flex gap-3">
                <button onclick="closeDeleteConfirmModal()" class="w-1/2 bg-slate-100 hover:bg-slate-200 text-slate-700 font-bold py-3 rounded-xl text-xs">Batal</button>
                <button id="confirmDeleteBtn" class="w-1/2 bg-red-600 hover:bg-red-700 text-white font-bold py-3 rounded-xl shadow-lg text-xs">Hapus Sekarang</button>
            </div>
        </div>
    </div>

    <!-- Toast Notification Container -->
    <div id="toastContainer" class="fixed top-24 right-5 z-50 flex flex-col space-y-2 pointer-events-none"></div>

    <script type="module">
        import { initializeApp } from "https://www.gstatic.com/firebasejs/11.6.1/firebase-app.js";
        import { getAuth, signInAnonymously, signInWithCustomToken } from "https://www.gstatic.com/firebasejs/11.6.1/firebase-auth.js";
        import { getFirestore, collection, addDoc, updateDoc, deleteDoc, doc, onSnapshot } from "https://www.gstatic.com/firebasejs/11.6.1/firebase-firestore.js";

        const appId = typeof __app_id !== 'undefined' ? __app_id : 'serviceku-app-2026';
        const firebaseConfig = typeof __firebase_config !== 'undefined' ? JSON.parse(__firebase_config) : {
            apiKey: "demo-key",
            authDomain: "demo.firebaseapp.com",
            projectId: "demo-project",
            storageBucket: "demo.appspot.com",
            messagingSenderId: "123456",
            appId: "123456"
        };

        let app, db, auth;
        let isAdminLoggedIn = localStorage.getItem('serviceku_admin') === 'true';
        let servicesList = [];
        let currentCategory = 'all';
        let deleteTargetId = null;

        const defaultServices = [
            { id: 'def-1', name: 'Cuci AC Standar', price: '75.000', category: 'ac', image: 'https://images.unsplash.com/photo-1621905251189-08b45d6a269e?auto=format&fit=crop&w=600&q=80', desc: 'Pembersihan evaporator, filter, blower indoor & kondensor outdoor.' },
            { id: 'def-2', name: 'Cuci Overhaul Turun Unit AC', price: '350.000', category: 'ac', image: 'https://images.unsplash.com/photo-1581092160562-40aa08e78837?auto=format&fit=crop&w=600&q=80', desc: 'Pembersihan menyeluruh dengan pembongkaran total unit AC.' },
            { id: 'def-3', name: 'Pasang Unit AC Baru/Bekas', price: '350.000', category: 'ac', image: 'https://images.unsplash.com/photo-1584622650111-993a426fbf0a?auto=format&fit=crop&w=600&q=80', desc: 'Jasa instalasi pemasangan AC rapi, vakum, & tes fungsi.' },
            { id: 'def-4', name: 'Bongkar Unit AC', price: '250.000', category: 'ac', image: 'https://images.unsplash.com/photo-1599839619722-39751411ea63?auto=format&fit=crop&w=600&q=80', desc: 'Pembongkaran unit AC aman tanpa kebocoran freon.' },
            { id: 'def-5', name: 'Perbaikan Kebocoran Freon AC', price: '750.000', category: 'ac', image: 'https://images.unsplash.com/photo-1558494949-ef010cbdcc31?auto=format&fit=crop&w=600&q=80', desc: 'Pengelasan bocor, pengisian freon penuh R32/R410/R22.' },
            { id: 'def-6', name: 'Perbaikan Modul Electronic AC', price: '350.000', category: 'ac', image: 'https://images.unsplash.com/photo-1581092335397-9583fe92d232?auto=format&fit=crop&w=600&q=80', desc: 'Perbaikan pcb komputer / sensor AC mati total.' },
            { id: 'def-7', name: 'Penggantian Modul Universal AC', price: '450.000', category: 'ac', image: 'https://images.unsplash.com/photo-1517336714731-489689fd1ca8?auto=format&fit=crop&w=600&q=80', desc: 'Penggantian pcb modul universal kualitas tinggi.' },
            { id: 'def-8', name: 'Service Kulkas & Showcase', price: 'Mulai 100.000', category: 'kulkas', image: 'https://images.unsplash.com/photo-1584622650111-993a426fbf0a?auto=format&fit=crop&w=600&q=80', desc: 'Perbaikan kulkas 1/2 pintu, inverter, & showcase minuman.' },
            { id: 'def-9', name: 'Service Mesin Cuci', price: 'Mulai 120.000', category: 'mesin_cuci', image: 'https://images.unsplash.com/photo-1626806787461-102c1bfaaea1?auto=format&fit=crop&w=600&q=80', desc: 'Perbaikan mesin cuci 1 tabung top loading / front loading & 2 tabung.' }
        ];

        window.addEventListener('DOMContentLoaded', () => {
            initFirebaseAndApp();
            initSlideshow();
            updateAuthUI();
        });

        async function initFirebaseAndApp() {
            try {
                app = initializeApp(firebaseConfig);
                db = getFirestore(app);
                auth = getAuth(app);

                if (typeof __initial_auth_token !== 'undefined' && __initial_auth_token) {
                    await signInWithCustomToken(auth, __initial_auth_token);
                } else {
                    await signInAnonymously(auth);
                }

                const servicesCollection = collection(db, 'artifacts', appId, 'public', 'data', 'services');
                onSnapshot(servicesCollection, (snapshot) => {
                    servicesList = [];
                    snapshot.forEach(docSnap => {
                        servicesList.push({ id: docSnap.id, ...docSnap.data() });
                    });
                    
                    if (servicesList.length === 0) {
                        servicesList = defaultServices;
                    }
                    renderServices();
                    document.getElementById('catalogLoading').style.display = 'none';
                }, (error) => {
                    console.warn("Firestore listener fallback to default:", error);
                    servicesList = defaultServices;
                    renderServices();
                    document.getElementById('catalogLoading').style.display = 'none';
                });

                const bannerTitle = localStorage.getItem('serviceku_banner_title');
                const bannerSub = localStorage.getItem('serviceku_banner_sub');
                if (bannerTitle) document.getElementById('mainHeroTitle').innerHTML = bannerTitle;
                if (bannerSub) document.getElementById('mainHeroSubtitle').innerText = bannerSub;

            } catch (e) {
                console.warn("Firebase initialization warning:", e);
                servicesList = defaultServices;
                renderServices();
                document.getElementById('catalogLoading').style.display = 'none';
            }
        }

        let slideIndex = 0;
        let slideTimer;

        function initSlideshow() {
            const slides = document.querySelectorAll('.hero-slide');
            if (slides.length > 0) {
                slideTimer = setInterval(() => {
                    setSlide((slideIndex + 1) % slides.length);
                }, 5000);
            }
        }

        window.setSlide = function(index) {
            const slides = document.querySelectorAll('.hero-slide');
            const dots = document.querySelectorAll('#slideshowDots button');
            if (slides.length === 0) return;

            slides[slideIndex].classList.remove('active');
            dots[slideIndex].className = "w-2 h-2 rounded-full bg-white/40 hover:bg-white/80 transition-all";

            slideIndex = index;

            slides[slideIndex].classList.add('active');
            dots[slideIndex].className = "w-8 h-2 rounded-full bg-brand-yellow transition-all";
        };

        function formatPriceDisplay(price) {
            if (!price) return 'Konsultasi';
            if (price.toString().toLowerCase().includes('rp') || price.toString().toLowerCase().includes('mulai')) {
                return price;
            }
            if (!isNaN(price) && price.length <= 4) {
                return `Rp ${price}.000`;
            }
            return `Rp ${price}`;
        }

        window.renderServices = function() {
            const grid = document.getElementById('servicesGrid');
            const emptyState = document.getElementById('emptyCatalogState');
            const searchQuery = (document.getElementById('searchInput')?.value || '').toLowerCase().trim();

            grid.innerHTML = '';

            const filtered = servicesList.filter(item => {
                const matchesCat = currentCategory === 'all' || item.category === currentCategory;
                const matchesSearch = item.name.toLowerCase().includes(searchQuery) || 
                                      (item.desc && item.desc.toLowerCase().includes(searchQuery));
                return matchesCat && matchesSearch;
            });

            if (filtered.length === 0) {
                emptyState.classList.remove('hidden');
            } else {
                emptyState.classList.add('hidden');
            }

            filtered.forEach(item => {
                const card = document.createElement('div');
                card.className = "bg-white rounded-3xl overflow-hidden border border-slate-200/80 shadow-sm hover:shadow-card-hover transition-all duration-300 flex flex-col group relative hover:-translate-y-1";
                
                const formattedPrice = formatPriceDisplay(item.price);
                const waMessage = encodeURIComponent(`Halo Serviceku, saya berminat dengan jasa *${item.name}* (Harga: ${formattedPrice}). Boleh minta informasi jadwal teknisi?`);
                const waUrl = `https://wa.me/6287874417978?text=${waMessage}`;

                card.innerHTML = `
                    <div class="relative h-48 overflow-hidden bg-slate-100">
                        <img src="${item.image}" alt="${item.name}" 
                             class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500" 
                             onerror="this.src='https://images.unsplash.com/photo-1621905251189-08b45d6a269e?auto=format&fit=crop&w=600&q=80'">
                        
                        <div class="absolute top-3 right-3 bg-gradient-to-r from-amber-400 to-amber-500 text-slate-950 font-extrabold px-3 py-1.5 rounded-xl text-xs shadow-md border border-white/20">
                            ${formattedPrice}
                        </div>

                        <div class="absolute top-3 left-3 bg-slate-900/80 backdrop-blur-md text-white text-[10px] uppercase tracking-wider font-extrabold px-2.5 py-1 rounded-lg">
                            <i class="fas fa-shield-alt text-brand-yellow mr-1"></i> Garansi 1 Bln
                        </div>
                    </div>

                    <div class="p-5 flex flex-col flex-grow">
                        <h3 class="font-bold text-slate-900 text-base mb-2 group-hover:text-brand-600 transition-colors line-clamp-1">${item.name}</h3>
                        <p class="text-slate-500 text-xs mb-5 line-clamp-2 leading-relaxed flex-grow">${item.desc || 'Jasa perbaikan elektronik profesional & cepat.'}</p>
                        
                        <div class="pt-3 border-t border-slate-100 flex items-center justify-between gap-2">
                            <a href="${waUrl}" target="_blank" 
                               class="flex-grow bg-emerald-500 hover:bg-emerald-600 text-white font-bold py-2.5 px-3 rounded-xl text-xs transition-all shadow-md shadow-emerald-500/20 flex items-center justify-center gap-1.5">
                                <i class="fab fa-whatsapp text-sm"></i> Pesan via WA
                            </a>
                            ${isAdminLoggedIn ? `
                                <button onclick="openEditServiceModal('${item.id}', '${encodeURIComponent(item.name)}', '${encodeURIComponent(item.price)}', '${encodeURIComponent(item.image)}', '${encodeURIComponent(item.desc || '')}', '${item.category || 'ac'}')" 
                                        class="bg-slate-100 hover:bg-slate-200 text-slate-700 p-2.5 rounded-xl text-xs transition-all" title="Edit Jasa">
                                    <i class="fas fa-edit"></i>
                                </button>
                                <button onclick="confirmDeleteService('${item.id}')" 
                                        class="bg-red-50 hover:bg-red-100 text-red-600 p-2.5 rounded-xl text-xs transition-all" title="Hapus Jasa">
                                    <i class="fas fa-trash-alt"></i>
                                </button>
                            ` : ''}
                        </div>
                    </div>
                `;
                grid.appendChild(card);
            });
        };

        window.setCategoryFilter = function(cat) {
            currentCategory = cat;
            const buttons = document.querySelectorAll('#categoryFilters .cat-btn');
            buttons.forEach(btn => {
                btn.className = "cat-btn bg-slate-100 hover:bg-slate-200 text-slate-700 text-xs font-bold px-4 py-2 rounded-xl transition-all";
            });
            event.target.closest('button').className = "cat-btn active bg-brand-600 text-white text-xs font-bold px-4 py-2 rounded-xl transition-all shadow-sm";
            renderServices();
        };

        window.filterServices = function() {
            renderServices();
        };

        window.handleAuthClick = function() {
            if (isAdminLoggedIn) {
                isAdminLoggedIn = false;
                localStorage.setItem('serviceku_admin', 'false');
                updateAuthUI();
                renderServices();
                showToast("Berhasil logout dari mode Admin.");
            } else {
                document.getElementById('loginModal').classList.remove('hidden');
            }
        };

        window.closeLoginModal = function() {
            document.getElementById('loginModal').classList.add('hidden');
            document.getElementById('loginForm').reset();
            document.getElementById('loginError').classList.add('hidden');
        };

        window.togglePasswordVisibility = function() {
            const passInput = document.getElementById('adminPass');
            const eyeIcon = document.getElementById('eyeIcon');
            if (passInput.type === 'password') {
                passInput.type = 'text';
                eyeIcon.className = 'fas fa-eye-slash';
            } else {
                passInput.type = 'password';
                eyeIcon.className = 'fas fa-eye';
            }
        };

        window.handleLogin = function(e) {
            e.preventDefault();
            const user = document.getElementById('adminUser').value.trim();
            const pass = document.getElementById('adminPass').value.trim();

            if (user === 'admin' && pass === 'serviceku123') {
                isAdminLoggedIn = true;
                localStorage.setItem('serviceku_admin', 'true');
                closeLoginModal();
                updateAuthUI();
                renderServices();
                showToast("Login Admin Berhasil!", "success");
            } else {
                const err = document.getElementById('loginError');
                err.innerText = "Username atau password salah! (Default: admin / serviceku123)";
                err.classList.remove('hidden');
            }
        };

        function updateAuthUI() {
            const navText = document.getElementById('authNavText');
            const navBtn = document.getElementById('authNavBtn');
            const addContainer = document.getElementById('adminAddContainer');
            const editBannerBtn = document.getElementById('adminEditBannerBtn');

            if (isAdminLoggedIn) {
                navText.innerText = "Logout Admin";
                navBtn.className = "bg-red-600 hover:bg-red-700 text-white px-3.5 py-2.5 rounded-xl text-xs sm:text-sm font-bold shadow-lg transition-all flex items-center gap-1.5";
                if (addContainer) addContainer.classList.remove('hidden');
                if (editBannerBtn) editBannerBtn.classList.remove('hidden');
            } else {
                navText.innerText = "Admin Login";
                navBtn.className = "bg-brand-600 hover:bg-brand-700 text-white px-3.5 py-2.5 rounded-xl text-xs sm:text-sm font-bold shadow-lg transition-all flex items-center gap-1.5";
                if (addContainer) addContainer.classList.add('hidden');
                if (editBannerBtn) editBannerBtn.classList.add('hidden');
            }
        }

        window.openServiceModal = function() {
            document.getElementById('modalServiceTitle').innerText = "Tambah Jasa Baru";
            document.getElementById('serviceForm').reset();
            document.getElementById('serviceId').value = '';
            document.getElementById('serviceModal').classList.remove('hidden');
        };

        window.openEditServiceModal = function(id, name, price, image, desc, cat) {
            document.getElementById('modalServiceTitle').innerText = "Edit Layanan";
            document.getElementById('serviceId').value = id;
            document.getElementById('serviceName').value = decodeURIComponent(name);
            document.getElementById('servicePrice').value = decodeURIComponent(price);
            document.getElementById('serviceImage').value = decodeURIComponent(image);
            document.getElementById('serviceDesc').value = decodeURIComponent(desc);
            document.getElementById('serviceCategory').value = cat || 'ac';
            document.getElementById('serviceModal').classList.remove('hidden');
        };

        window.closeServiceModal = function() {
            document.getElementById('serviceModal').classList.add('hidden');
        };

        window.handleSaveService = async function(e) {
            e.preventDefault();
            const id = document.getElementById('serviceId').value;
            const name = document.getElementById('serviceName').value;
            const price = document.getElementById('servicePrice').value;
            const image = document.getElementById('serviceImage').value;
            const desc = document.getElementById('serviceDesc').value;
            const category = document.getElementById('serviceCategory').value;

            const serviceData = { name, price, image, desc, category, updatedAt: new Date().toISOString() };

            try {
                if (db && !id.startsWith('def-')) {
                    if (id) {
                        const docRef = doc(db, 'artifacts', appId, 'public', 'data', 'services', id);
                        await updateDoc(docRef, serviceData);
                    } else {
                        const colRef = collection(db, 'artifacts', appId, 'public', 'data', 'services');
                        await addDoc(colRef, serviceData);
                    }
                } else {
                    if (id) {
                        const idx = servicesList.findIndex(s => s.id === id);
                        if (idx !== -1) servicesList[idx] = { id, ...serviceData };
                    } else {
                        servicesList.push({ id: 'local-' + Date.now(), ...serviceData });
                    }
                    renderServices();
                }
                closeServiceModal();
                showToast("Data jasa berhasil disimpan!", "success");
            } catch (err) {
                console.error("Error saving service:", err);
                showToast("Gagal menyimpan jasa", "error");
            }
        };

        window.confirmDeleteService = function(id) {
            deleteTargetId = id;
            document.getElementById('deleteConfirmModal').classList.remove('hidden');
            document.getElementById('confirmDeleteBtn').onclick = () => executeDeleteService(id);
        };

        window.closeDeleteConfirmModal = function() {
            deleteTargetId = null;
            document.getElementById('deleteConfirmModal').classList.add('hidden');
        };

        async function executeDeleteService(id) {
            try {
                if (db && !id.startsWith('def-')) {
                    const docRef = doc(db, 'artifacts', appId, 'public', 'data', 'services', id);
                    await deleteDoc(docRef);
                } else {
                    servicesList = servicesList.filter(s => s.id !== id);
                    renderServices();
                }
                closeDeleteConfirmModal();
                showToast("Layanan berhasil dihapus.", "success");
            } catch (err) {
                console.error("Error deleting service:", err);
                showToast("Gagal menghapus layanan", "error");
            }
        }

        window.openBannerModal = function() {
            document.getElementById('bannerTitleInput').value = document.getElementById('mainHeroTitle').innerText;
            document.getElementById('bannerSubtitleInput').value = document.getElementById('mainHeroSubtitle').innerText;
            document.getElementById('bannerModal').classList.remove('hidden');
        };

        window.closeBannerModal = function() {
            document.getElementById('bannerModal').classList.add('hidden');
        };

        window.handleSaveBanner = function(e) {
            e.preventDefault();
            const newTitle = document.getElementById('bannerTitleInput').value;
            const newSub = document.getElementById('bannerSubtitleInput').value;

            document.getElementById('mainHeroTitle').innerText = newTitle;
            document.getElementById('mainHeroSubtitle').innerText = newSub;

            localStorage.setItem('serviceku_banner_title', newTitle);
            localStorage.setItem('serviceku_banner_sub', newSub);
            closeBannerModal();
            showToast("Teks banner berhasil diperbarui!", "success");
        };

        window.toggleMobileMenu = function() {
            const menu = document.getElementById('mobileMenu');
            const icon = document.getElementById('mobileMenuIcon');
            menu.classList.toggle('hidden');
            if (menu.classList.contains('hidden')) {
                icon.className = 'fas fa-bars text-xl';
            } else {
                icon.className = 'fas fa-times text-xl';
            }
        };

        function showToast(message, type = 'info') {
            const container = document.getElementById('toastContainer');
            const toast = document.createElement('div');
            toast.className = `pointer-events-auto px-4 py-3 rounded-2xl shadow-xl text-white text-xs font-bold flex items-center gap-2 transform transition-all duration-300 translate-x-10 opacity-0 ${
                type === 'success' ? 'bg-emerald-600' : type === 'error' ? 'bg-red-600' : 'bg-slate-800'
            }`;
            
            const iconClass = type === 'success' ? 'fa-check-circle' : type === 'error' ? 'fa-exclamation-circle' : 'fa-info-circle';
            toast.innerHTML = `<i class="fas ${iconClass} text-base"></i> <span>${message}</span>`;
            
            container.appendChild(toast);

            setTimeout(() => {
                toast.classList.remove('translate-x-10', 'opacity-0');
            }, 50);

            setTimeout(() => {
                toast.classList.add('translate-x-10', 'opacity-0');
                setTimeout(() => toast.remove(), 300);
            }, 3000);
        }
    </script>
</body>
</html>
