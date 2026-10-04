<!DOCTYPE html>
<html lang="id" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Serviceku - Jasa Service Elektronik Terbaik</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    },
                    colors: {
                        brand: {
                            50: '#eff6ff',
                            100: '#dbeafe',
                            500: '#3b82f6',
                            600: '#2563eb',
                            700: '#1d4ed8',
                            900: '#1e3a8a',
                            yellow: '#facc15'
                        }
                    }
                }
            }
        }
    </script>
    <style>
        .glass {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border-bottom: 1px solid rgba(229, 231, 235, 0.8);
        }
        .hero-slide {
            opacity: 0;
            transition: opacity 1s ease-in-out;
            position: absolute;
            inset: 0;
            display: none;
        }
        .hero-slide.active {
            opacity: 1;
            display: block;
        }
    </style>
</head>
<body class="bg-gray-50 text-gray-800 antialiased flex flex-col min-h-screen">

    <nav class="fixed w-full z-50 glass transition-all duration-300 shadow-sm" id="navbar">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between h-20 items-center">
                <!-- Logo & Brand -->
                <div class="flex-shrink-0 flex items-center cursor-pointer" onclick="window.scrollTo(0,0)">
                    <img class="h-12 w-auto object-contain rounded-lg shadow-sm" src="https://lh3.googleusercontent.com/d/1L2CtZvTu4_T8ji_R1u72kLdQbhdjoFzw" alt="Serviceku Logo" onerror="this.src='https://drive.google.com/uc?export=view&id=1L2CtZvTu4_T8ji_R1u72kLdQbhdjoFzw'">
                    <span class="ml-3 font-extrabold text-xl text-brand-900 tracking-tight">SERVICEKU</span>
                </div>
                
                <!-- Navigation Actions -->
                <div class="flex items-center space-x-3">
                    <a href="#katalog" class="text-gray-700 hover:text-brand-600 px-3 py-2 rounded-lg text-sm font-medium transition-colors hidden sm:block">
                        <i class="fas fa-tools mr-1"></i> Katalog Layanan
                    </a>
                    <a href="https://wa.me/6287874417978" target="_blank" class="bg-emerald-500 hover:bg-emerald-600 text-white px-4 py-2 rounded-xl text-sm font-semibold shadow-md shadow-emerald-500/20 transition-all flex items-center gap-2">
                        <i class="fab fa-whatsapp text-lg"></i> <span class="hidden md:inline">0878-7441-7978</span>
                    </a>
                    <button id="authNavBtn" onclick="handleAuthClick()" class="bg-brand-600 hover:bg-brand-700 text-white px-4 py-2 rounded-xl text-sm font-semibold shadow-md shadow-brand-500/20 transition-all flex items-center gap-1.5">
                        <i class="fas fa-user-shield"></i> <span id="authNavText">Admin Login</span>
                    </button>
                </div>
            </div>
        </div>
    </nav>

    <header class="relative h-[65vh] min-h-[450px] flex items-center justify-center overflow-hidden pt-20 bg-gray-900">
        <!-- Slideshow Backgrounds -->
        <div id="slideshowContainer" class="absolute inset-0 z-0">
            <div class="hero-slide active inset-0 bg-cover bg-center" style="background-image: linear-gradient(to bottom, rgba(15,23,42,0.7), rgba(15,23,42,0.9)), url('https://images.unsplash.com/photo-1581092160562-40aa08e78837?auto=format&fit=crop&w=1920&q=80');"></div>
            <div class="hero-slide inset-0 bg-cover bg-center" style="background-image: linear-gradient(to bottom, rgba(15,23,42,0.7), rgba(15,23,42,0.9)), url('https://images.unsplash.com/photo-1584622650111-993a426fbf0a?auto=format&fit=crop&w=1920&q=80');"></div>
            <div class="hero-slide inset-0 bg-cover bg-center" style="background-image: linear-gradient(to bottom, rgba(15,23,42,0.7), rgba(15,23,42,0.9)), url('https://images.unsplash.com/photo-1599839619722-39751411ea63?auto=format&fit=crop&w=1920&q=80');"></div>
        </div>

        <!-- Banner Content -->
        <div class="relative z-20 text-center px-4 max-w-4xl mx-auto mt-6">
            <span class="bg-brand-yellow text-gray-900 font-bold px-3 py-1 rounded-full text-xs uppercase tracking-wider mb-4 inline-block shadow-sm">
                <i class="fas fa-star mr-1"></i> Bergaransi 1 Bulan
            </span>
            <h1 id="mainHeroTitle" class="text-3xl sm:text-5xl md:text-6xl font-extrabold text-white tracking-tight mb-4 drop-shadow-md">
                Jasa Service Elektronik Profesional & Panggilan
            </h1>
            <p id="mainHeroSubtitle" class="text-base sm:text-lg text-gray-200 mb-8 font-light max-w-2xl mx-auto drop-shadow">
                Melayani AC, Kulkas, Mesin Cuci, Showcase, Freezer Box & Dispenser langsung ke rumah Anda di Indramayu, Cirebon, & Majalengka.
            </p>
            <div class="flex flex-wrap justify-center gap-3 sm:gap-4">
                <a href="#katalog" class="bg-brand-yellow hover:bg-yellow-400 text-gray-900 font-bold px-8 py-3.5 rounded-xl shadow-lg transition-all hover:scale-105 flex items-center gap-2">
                    <i class="fas fa-th-large"></i> Lihat Katalog Jasa
                </a>
                <button id="adminEditBannerBtn" onclick="openBannerModal()" class="hidden bg-white/20 hover:bg-white/30 backdrop-blur-md text-white font-semibold px-6 py-3.5 rounded-xl transition-all border border-white/30 flex items-center gap-2">
                    <i class="fas fa-edit"></i> Edit Teks Banner
                </button>
            </div>
        </div>
    </header>

    <section class="bg-brand-900 text-white py-6 border-b border-brand-700">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 grid grid-cols-2 md:grid-cols-4 gap-6 text-center">
            <div class="flex flex-col items-center">
                <div class="w-12 h-12 rounded-full bg-brand-600/50 flex items-center justify-center text-brand-yellow text-xl mb-2"><i class="fas fa-shield-alt"></i></div>
                <h4 class="font-bold text-sm">Pekerjaan Bergaransi</h4>
                <p class="text-xs text-gray-300">Garansi service 1 bulan</p>
            </div>
            <div class="flex flex-col items-center">
                <div class="w-12 h-12 rounded-full bg-brand-600/50 flex items-center justify-center text-brand-yellow text-xl mb-2"><i class="fas fa-user-tie"></i></div>
                <h4 class="font-bold text-sm">Teknisi Berpengalaman</h4>
                <p class="text-xs text-gray-300">Handal, Jujur & Amanah</p>
            </div>
            <div class="flex flex-col items-center">
                <div class="w-12 h-12 rounded-full bg-brand-600/50 flex items-center justify-center text-brand-yellow text-xl mb-2"><i class="fas fa-bolt"></i></div>
                <h4 class="font-bold text-sm">Respon Cepat</h4>
                <p class="text-xs text-gray-300">Teknisi siap datang ke lokasi</p>
            </div>
            <div class="flex flex-col items-center">
                <div class="w-12 h-12 rounded-full bg-brand-600/50 flex items-center justify-center text-brand-yellow text-xl mb-2"><i class="fas fa-map-marked-alt"></i></div>
                <h4 class="font-bold text-sm">Wilayah Layanan</h4>
                <p class="text-xs text-gray-300">Indramayu, Cirebon, Majalengka</p>
            </div>
        </div>
    </section>

    <main class="flex-grow py-16">
        <section id="katalog" class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex flex-col md:flex-row justify-between items-start md:items-end mb-10 gap-4">
                <div>
                    <span class="text-brand-600 font-semibold text-sm uppercase tracking-wider">Daftar Harga & Jasa</span>
                    <h2 class="text-3xl font-extrabold text-gray-900 mt-1">Katalog & Tarif Layanan Elektronik</h2>
                    <p class="text-gray-600 text-sm mt-1">Klik pada layanan untuk langsung terhubung ke WhatsApp teknisi kami.</p>
                </div>
                <!-- Admin Add Button Container -->
                <div id="adminAddContainer" class="hidden">
                    <button onclick="openServiceModal()" class="bg-brand-600 hover:bg-brand-700 text-white px-5 py-3 rounded-xl font-semibold shadow-md shadow-brand-500/20 transition-all flex items-center gap-2">
                        <i class="fas fa-plus-circle"></i> Tambah Jasa Baru
                    </button>
                </div>
            </div>

            <!-- Loading Spinner -->
            <div id="catalogLoading" class="text-center py-20">
                <div class="inline-block animate-spin rounded-full h-12 w-12 border-4 border-brand-600 border-t-transparent"></div>
                <p class="text-gray-500 mt-3 font-medium">Memuat katalog jasa...</p>
            </div>

            <!-- Services Grid -->
            <div id="servicesGrid" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
                <!-- Dynamically populated from Firestore or Default Catalog -->
            </div>
        </section>

        <section class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 mt-20">
            <div class="bg-gradient-to-r from-brand-900 to-brand-700 rounded-3xl p-8 md:p-12 text-white shadow-xl flex flex-col md:flex-row items-center justify-between gap-8">
                <div class="max-w-xl">
                    <span class="bg-white/20 text-white text-xs font-bold px-3 py-1 rounded-full uppercase">Area Panggilan</span>
                    <h3 class="text-2xl md:text-3xl font-extrabold mt-3">Melayani Service Panggilan ke Rumah Anda</h3>
                    <p class="text-gray-200 mt-2 text-sm leading-relaxed">
                        Jl. By Pass Binaria - Bondan. Teknisi kami siap melayani perbaikan langsung di tempat untuk wilayah Indramayu, Cirebon, dan Majalengka serta sekitarnya.
                    </p>
                    <div class="mt-6 flex flex-wrap gap-4">
                        <div class="flex items-center gap-2 bg-white/10 px-4 py-2 rounded-xl text-sm font-semibold">
                            <i class="fas fa-map-marker-alt text-brand-yellow"></i> Indramayu
                        </div>
                        <div class="flex items-center gap-2 bg-white/10 px-4 py-2 rounded-xl text-sm font-semibold">
                            <i class="fas fa-map-marker-alt text-brand-yellow"></i> Cirebon
                        </div>
                        <div class="flex items-center gap-2 bg-white/10 px-4 py-2 rounded-xl text-sm font-semibold">
                            <i class="fas fa-map-marker-alt text-brand-yellow"></i> Majalengka
                        </div>
                    </div>
                </div>
                <div class="bg-white/10 backdrop-blur-md p-6 rounded-2xl border border-white/20 text-center flex-shrink-0 w-full md:w-auto">
                    <p class="text-xs uppercase font-bold tracking-wider text-brand-yellow">Hubungi Cepat via WhatsApp</p>
                    <a href="https://wa.me/6287874417978" target="_blank" class="mt-3 block text-2xl md:text-3xl font-extrabold text-white hover:text-brand-yellow transition-colors">
                        <i class="fab fa-whatsapp mr-2"></i> 0878-7441-7978
                    </a>
                    <p class="text-xs text-gray-300 mt-1">Respon cepat jam kerja</p>
                </div>
            </div>
        </section>
    </main>

    <footer class="bg-gray-900 text-white pt-12 pb-8 border-t border-gray-800">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 grid grid-cols-1 md:grid-cols-3 gap-8 mb-8">
            <div>
                <div class="flex items-center space-x-3 mb-4">
                    <img class="h-10 w-auto object-contain rounded p-0.5 bg-white/10" src="https://lh3.googleusercontent.com/d/1L2CtZvTu4_T8ji_R1u72kLdQbhdjoFzw" alt="Serviceku Logo" onerror="this.src='https://drive.google.com/uc?export=view&id=1L2CtZvTu4_T8ji_R1u72kLdQbhdjoFzw'">
                    <span class="font-bold text-lg tracking-wide">SERVICEKU</span>
                </div>
                <p class="text-gray-400 text-sm leading-relaxed">
                    Jasa service elektronik terpercaya untuk AC, Kulkas, Mesin Cuci, Dispenser, Showcase, dan Freezer Box dengan teknisi handal dan bergaransi.
                </p>
            </div>
            <div>
                <h4 class="font-bold text-base mb-4 text-brand-yellow">Kontak & Alamat</h4>
                <p class="text-gray-400 text-sm mb-2"><i class="fas fa-map-marker-alt mr-2 text-brand-500"></i> Jl. By Pass Binaria - Bondan</p>
                <p class="text-gray-400 text-sm mb-2"><i class="fab fa-whatsapp mr-2 text-emerald-500"></i> +62 878-7441-7978</p>
                <p class="text-gray-400 text-sm"><i class="fas fa-envelope mr-2 text-brand-500"></i> info@serviceku.id</p>
            </div>
            <div>
                <h4 class="font-bold text-base mb-4 text-brand-yellow">Jam Operasional</h4>
                <p class="text-gray-400 text-sm mb-2">Senin - Minggu: 08.00 - 18.00 WIB</p>
                <p class="text-gray-400 text-sm">Layanan darurat panggilan tersedia.</p>
            </div>
        </div>
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 pt-6 border-t border-gray-800 text-center text-xs text-gray-500">
            &copy; 2026 Serviceku. Hak Cipta Dilindungi.
        </div>
    </footer>

    <div id="loginModal" class="fixed inset-0 z-50 bg-black/60 backdrop-blur-sm hidden flex items-center justify-center p-4">
        <div class="bg-white rounded-3xl max-w-md w-full p-8 shadow-2xl relative">
            <button onclick="closeLoginModal()" class="absolute top-5 right-5 text-gray-400 hover:text-gray-600 text-xl"><i class="fas fa-times"></i></button>
            <div class="text-center mb-6">
                <div class="w-14 h-14 bg-brand-100 text-brand-600 rounded-2xl mx-auto flex items-center justify-center text-2xl mb-3 shadow-inner">
                    <i class="fas fa-user-shield"></i>
                </div>
                <h3 class="text-2xl font-bold text-gray-900">Admin Login</h3>
                <p class="text-sm text-gray-500 mt-1">Masuk untuk mengelola katalog & banner jasa</p>
            </div>
            <form id="loginForm" onsubmit="handleLogin(event)" class="space-y-4">
                <div>
                    <label class="block text-xs font-bold text-gray-700 uppercase mb-1">Username Admin</label>
                    <input type="text" id="adminUser" required class="w-full px-4 py-3 rounded-xl border border-gray-300 focus:ring-2 focus:ring-brand-500 focus:outline-none text-sm" placeholder="Masukkan username">
                </div>
                <div>
                    <label class="block text-xs font-bold text-gray-700 uppercase mb-1">Password</label>
                    <div class="relative">
                        <input type="password" id="adminPass" required class="w-full px-4 py-3 rounded-xl border border-gray-300 focus:ring-2 focus:ring-brand-500 focus:outline-none text-sm pr-12" placeholder="Masukkan password">
                        <button type="button" onclick="togglePasswordVisibility()" class="absolute right-4 top-1/2 -translate-y-1/2 text-gray-400 hover:text-gray-600">
                            <i id="eyeIcon" class="fas fa-eye"></i>
                        </button>
                    </div>
                </div>
                <div id="loginError" class="text-red-500 text-xs font-semibold hidden text-center"></div>
                <button type="submit" class="w-full bg-brand-600 hover:bg-brand-700 text-white font-bold py-3.5 rounded-xl shadow-lg shadow-brand-500/30 transition-all text-sm">
                    Masuk Dashboard
                </button>
            </form>
        </div>
    </div>

    <div id="serviceModal" class="fixed inset-0 z-50 bg-black/60 backdrop-blur-sm hidden flex items-center justify-center p-4">
        <div class="bg-white rounded-3xl max-w-lg w-full p-8 shadow-2xl relative max-h-[90vh] overflow-y-auto">
            <button onclick="closeServiceModal()" class="absolute top-5 right-5 text-gray-400 hover:text-gray-600 text-xl"><i class="fas fa-times"></i></button>
            <h3 id="modalServiceTitle" class="text-2xl font-bold text-gray-900 mb-6">Tambah Jasa Baru</h3>
            <form id="serviceForm" onsubmit="handleSaveService(event)" class="space-y-4">
                <input type="hidden" id="serviceId">
                <div>
                    <label class="block text-xs font-bold text-gray-700 uppercase mb-1">Nama Jasa / Barang</label>
                    <input type="text" id="serviceName" required class="w-full px-4 py-3 rounded-xl border border-gray-300 focus:ring-2 focus:ring-brand-500 focus:outline-none text-sm" placeholder="Contoh: Cuci AC / Perbaikan Kulkas">
                </div>
                <div>
                    <label class="block text-xs font-bold text-gray-700 uppercase mb-1">Tarif / Harga (Rupiah atau Keterangan)</label>
                    <input type="text" id="servicePrice" required class="w-full px-4 py-3 rounded-xl border border-gray-300 focus:ring-2 focus:ring-brand-500 focus:outline-none text-sm" placeholder="Contoh: 75.000 atau 750 (tergantung kapasitas)">
                </div>
                <div>
                    <label class="block text-xs font-bold text-gray-700 uppercase mb-1">URL Foto Jasa (Gambar Langsung)</label>
                    <input type="url" id="serviceImage" required class="w-full px-4 py-3 rounded-xl border border-gray-300 focus:ring-2 focus:ring-brand-500 focus:outline-none text-sm" placeholder="https://images.unsplash.com/photo-...">
                    <p class="text-xs text-gray-400 mt-1">Masukkan link gambar publik (Unsplash, Google Drive direct link, dll).</p>
                </div>
                <div>
                    <label class="block text-xs font-bold text-gray-700 uppercase mb-1">Deskripsi Singkat / Catatan</label>
                    <textarea id="serviceDesc" rows="3" class="w-full px-4 py-3 rounded-xl border border-gray-300 focus:ring-2 focus:ring-brand-500 focus:outline-none text-sm" placeholder="Contoh: Pengecekan menyeluruh, teknisi datang langsung ke rumah."></textarea>
                </div>
                <div class="flex gap-3 pt-2">
                    <button type="button" onclick="closeServiceModal()" class="w-1/2 bg-gray-100 hover:bg-gray-200 text-gray-700 font-bold py-3 rounded-xl transition-all text-sm">Batal</button>
                    <button type="submit" class="w-1/2 bg-brand-600 hover:bg-brand-700 text-white font-bold py-3 rounded-xl shadow-lg shadow-brand-500/20 transition-all text-sm">Simpan Jasa</button>
                </div>
            </form>
        </div>
    </div>

    <div id="bannerModal" class="fixed inset-0 z-50 bg-black/60 backdrop-blur-sm hidden flex items-center justify-center p-4">
        <div class="bg-white rounded-3xl max-w-md w-full p-8 shadow-2xl relative">
            <button onclick="closeBannerModal()" class="absolute top-5 right-5 text-gray-400 hover:text-gray-600 text-xl"><i class="fas fa-times"></i></button>
            <h3 class="text-2xl font-bold text-gray-900 mb-6">Edit Teks Banner</h3>
            <form onsubmit="handleSaveBanner(event)" class="space-y-4">
                <div>
                    <label class="block text-xs font-bold text-gray-700 uppercase mb-1">Judul Banner Utama</label>
                    <input type="text" id="bannerTitleInput" required class="w-full px-4 py-3 rounded-xl border border-gray-300 focus:ring-2 focus:ring-brand-500 focus:outline-none text-sm">
                </div>
                <div>
                    <label class="block text-xs font-bold text-gray-700 uppercase mb-1">Subjudul / Deskripsi Banner</label>
                    <textarea id="bannerSubtitleInput" rows="3" required class="w-full px-4 py-3 rounded-xl border border-gray-300 focus:ring-2 focus:ring-brand-500 focus:outline-none text-sm"></textarea>
                </div>
                <div class="flex gap-3 pt-2">
                    <button type="button" onclick="closeBannerModal()" class="w-1/2 bg-gray-100 hover:bg-gray-200 text-gray-700 font-bold py-3 rounded-xl transition-all text-sm">Batal</button>
                    <button type="submit" class="w-1/2 bg-brand-600 hover:bg-brand-700 text-white font-bold py-3 rounded-xl shadow-lg shadow-brand-500/20 transition-all text-sm">Simpan Banner</button>
                </div>
            </form>
        </div>
    </div>

    <script type="module">
        import { initializeApp } from "https://www.gstatic.com/firebasejs/11.6.1/firebase-app.js";
        import { getAuth, signInAnonymously, signInWithCustomToken, onAuthStateChanged } from "https://www.gstatic.com/firebasejs/11.6.1/firebase-auth.js";
        import { getFirestore, collection, addDoc, updateDoc, deleteDoc, doc, onSnapshot } from "https://www.gstatic.com/firebasejs/11.6.1/firebase-firestore.js";

        // Global variables & Firebase Setup
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
        let currentUser = null;
        let isAdminLoggedIn = localStorage.getItem('serviceku_admin') === 'true';
        let servicesList = [];

        // Default initial services based on the uploaded flyer catalog
        const defaultServices = [
            { id: 'def-1', name: 'Cuci AC', price: '75', image: 'https://images.unsplash.com/photo-1621905251189-08b45d6a269e?auto=format&fit=crop&w=600&q=80', desc: 'Pembersihan unit AC indoor & outdoor agar dingin maksimal.' },
            { id: 'def-2', name: 'Cuci Overhaul Turun Unit', price: '350', image: 'https://images.unsplash.com/photo-1581092160562-40aa08e78837?auto=format&fit=crop&w=600&q=80', desc: 'Cuci besar pembongkaran total unit AC.' },
            { id: 'def-3', name: 'Pasang AC', price: '350', image: 'https://images.unsplash.com/photo-1584622650111-993a426fbf0a?auto=format&fit=crop&w=600&q=80', desc: 'Jasa instalasi pemasangan AC baru / bekas.' },
            { id: 'def-4', name: 'Bongkar AC', price: '250', image: 'https://images.unsplash.com/photo-1599839619722-39751411ea63?auto=format&fit=crop&w=600&q=80', desc: 'Jasa pembongkaran unit AC rapi dan aman.' },
            { id: 'def-5', name: 'Perbaikan Kebocoran Freon AC', price: '750', image: 'https://images.unsplash.com/photo-1558494949-ef010cbdcc31?auto=format&fit=crop&w=600&q=80', desc: 'Tergantung kapasitas dan tingkat kesulitan.' },
            { id: 'def-6', name: 'Perbaikan Modul AC', price: '350', image: 'https://images.unsplash.com/photo-1581092335397-9583fe92d232?auto=format&fit=crop&w=600&q=80', desc: 'Perbaikan kerusakan elektronik modul AC.' },
            { id: 'def-7', name: 'Penggantian Modul Universal', price: '450', image: 'https://images.unsplash.com/photo-1517336714731-489689fd1ca8?auto=format&fit=crop&w=600&q=80', desc: 'Penggantian modul universal bergaransi.' },
            { id: 'def-8', name: 'Kulkas & Dispenser', price: 'Mulai 100', image: 'https://images.unsplash.com/photo-1584622650111-993a426fbf0a?auto=format&fit=crop&w=600&q=80', desc: 'Service kulkas 1 pintu, side by side, & dispenser air.' },
            { id: 'def-9', name: 'Mesin Cuci & Showcase', price: 'Mulai 120', image: 'https://images.unsplash.com/photo-1626806787461-102c1bfaaea1?auto=format&fit=crop&w=600&q=80', desc: 'Perbaikan mesin cuci front/top loading & showcase pendingin.' }
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
                        renderServices(defaultServices);
                    } else {
                        renderServices(servicesList);
                    }
                    document.getElementById('catalogLoading').style.display = 'none';
                }, (error) => {
                    console.error("Firestore error:", error);
                    renderServices(defaultServices);
                    document.getElementById('catalogLoading').style.display = 'none';
                });

                const bannerTitle = localStorage.getItem('serviceku_banner_title');
                const bannerSub = localStorage.getItem('serviceku_banner_sub');
                if (bannerTitle) document.getElementById('mainHeroTitle').innerText = bannerTitle;
                if (bannerSub) document.getElementById('mainHeroSubtitle').innerText = bannerSub;

            } catch (e) {
                console.warn("Using offline mode fallback:", e);
                renderServices(defaultServices);
                document.getElementById('catalogLoading').style.display = 'none';
            }
        }

        // Slideshow functionality
        function initSlideshow() {
            const slides = document.querySelectorAll('.hero-slide');
            let currentSlide = 0;
            if (slides.length > 0) {
                setInterval(() => {
                    slides[currentSlide].classList.remove('active');
                    currentSlide = (currentSlide + 1) % slides.length;
                    slides[currentSlide].classList.add('active');
                }, 4500);
            }
        }

        function renderServices(items) {
            const grid = document.getElementById('servicesGrid');
            grid.innerHTML = '';

            items.forEach(item => {
                const card = document.createElement('div');
                card.className = "bg-white rounded-3xl overflow-hidden shadow-md hover:shadow-xl transition-all duration-300 border border-gray-100 flex flex-col group";
                
                const waMessage = encodeURIComponent(`Halo Serviceku, saya ingin memesan jasa: *${item.name}* (Tarif: ${item.price}). Mohon info jadwal teknisi.`);
                const waUrl = `https://wa.me/6287874417978?text=${waMessage}`;

                card.innerHTML = `
                    <div class="relative h-48 overflow-hidden bg-gray-100">
                        <img src="${item.image}" alt="${item.name}" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500" onerror="this.src='https://placehold.co/600x400/2563eb/white?text=SERVICEKU'">
                        <div class="absolute top-3 right-3 bg-brand-yellow text-gray-900 font-bold px-3 py-1 rounded-full text-xs shadow-md">
                            Rp ${item.price}
                        </div>
                    </div>
                    <div class="p-6 flex flex-col flex-grow">
                        <h3 class="font-bold text-lg text-gray-900 mb-2">${item.name}</h3>
                        <p class="text-gray-600 text-xs mb-4 line-clamp-2 leading-relaxed">${item.desc || 'Jasa perbaikan elektronik handal dan profesional.'}</p>
                        
                        <div class="mt-auto pt-4 border-t border-gray-100 flex items-center justify-between gap-2">
                            <a href="${waUrl}" target="_blank" class="flex-grow bg-emerald-500 hover:bg-emerald-600 text-white font-bold py-2.5 px-4 rounded-xl text-xs transition-all shadow-sm flex items-center justify-center gap-1.5">
                                <i class="fab fa-whatsapp text-sm"></i> Chat WA
                            </a>
                            ${isAdminLoggedIn ? `
                                <button onclick="openEditServiceModal('${item.id}', '${encodeURIComponent(item.name)}', '${encodeURIComponent(item.price)}', '${encodeURIComponent(item.image)}', '${encodeURIComponent(item.desc || '')}')" class="bg-gray-100 hover:bg-gray-200 text-gray-700 p-2.5 rounded-xl text-xs transition-all" title="Edit Jasa">
                                    <i class="fas fa-edit"></i>
                                </button>
                                <button onclick="deleteService('${item.id}')" class="bg-red-50 hover:bg-red-100 text-red-600 p-2.5 rounded-xl text-xs transition-all" title="Hapus Jasa">
                                    <i class="fas fa-trash"></i>
                                </button>
                            ` : ''}
                        </div>
                    </div>
                `;
                grid.appendChild(card);
            });
        }

        window.handleAuthClick = function() {
            if (isAdminLoggedIn) {
                isAdminLoggedIn = false;
                localStorage.setItem('serviceku_admin', 'false');
                updateAuthUI();
                renderServices(servicesList.length > 0 ? servicesList : defaultServices);
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
            const user = document.getElementById('adminUser').value;
            const pass = document.getElementById('adminPass').value;

            if (user === 'admin' && pass === 'serviceku123') {
                isAdminLoggedIn = true;
                localStorage.setItem('serviceku_admin', 'true');
                closeLoginModal();
                updateAuthUI();
                renderServices(servicesList.length > 0 ? servicesList : defaultServices);
            } else {
                const err = document.getElementById('loginError');
                err.innerText = "Username atau password salah! (Gunakan admin / serviceku123)";
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
                navBtn.className = "bg-red-600 hover:bg-red-700 text-white px-4 py-2 rounded-xl text-sm font-semibold shadow-md transition-all flex items-center gap-1.5";
                if (addContainer) addContainer.classList.remove('hidden');
                if (editBannerBtn) editBannerBtn.classList.remove('hidden');
            } else {
                navText.innerText = "Admin Login";
                navBtn.className = "bg-brand-600 hover:bg-brand-700 text-white px-4 py-2 rounded-xl text-sm font-semibold shadow-md transition-all flex items-center gap-1.5";
                if (addContainer) addContainer.classList.add('hidden');
                if (editBannerBtn) editBannerBtn.classList.add('hidden');
            }
        }

        // Service Modal CRUD
        window.openServiceModal = function() {
            document.getElementById('modalServiceTitle').innerText = "Tambah Jasa Baru";
            document.getElementById('serviceForm').reset();
            document.getElementById('serviceId').value = '';
            document.getElementById('serviceModal').classList.remove('hidden');
        };

        window.openEditServiceModal = function(id, name, price, image, desc) {
            document.getElementById('modalServiceTitle').innerText = "Edit Jasa / Layanan";
            document.getElementById('serviceId').value = id;
            document.getElementById('serviceName').value = decodeURIComponent(name);
            document.getElementById('servicePrice').value = decodeURIComponent(price);
            document.getElementById('serviceImage').value = decodeURIComponent(image);
            document.getElementById('serviceDesc').value = decodeURIComponent(desc);
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

            const serviceData = { name, price, image, desc, updatedAt: new Date().toISOString() };

            try {
                if (db) {
                    if (id && !id.startsWith('def-')) {
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
                    renderServices(servicesList);
                }
                closeServiceModal();
            } catch (err) {
                console.error("Error saving service:", err);
            }
        };

        window.deleteService = async function(id) {
            try {
                if (db && !id.startsWith('def-')) {
                    const docRef = doc(db, 'artifacts', appId, 'public', 'data', 'services', id);
                    await deleteDoc(docRef);
                } else {
                    servicesList = servicesList.filter(s => s.id !== id);
                    renderServices(servicesList);
                }
            } catch (err) {
                console.error("Error deleting service:", err);
            }
        };

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
        };
    </script>
</body>
</html>
