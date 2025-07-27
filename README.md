<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Wilson's Lane Cafe</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: '#FF6B98',
                        secondary: '#FFD1DC',
                        accent: '#FF91A4',
                        dark: '#4A3637',
                        light: '#FFF0F3',
                    },
                    fontFamily: {
                        sans: ['Poppins', 'sans-serif'],
                        serif: ['Playfair Display', 'serif'],
                    }
                }
            }
        }
    </script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;500;600;700&family=Poppins:wght@300;400;500;600&display=swap');
        
        body {
            font-family: 'Poppins', sans-serif;
            scroll-behavior: smooth;
        }
        
        .hero-pattern {
            background-color: #FFF0F3;
            background-image: url("data:image/svg+xml,%3Csvg width='60' height='60' viewBox='0 0 60 60' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='none' fill-rule='evenodd'%3E%3Cg fill='%23ff6b98' fill-opacity='0.1'%3E%3Cpath d='M36 34v-4h-2v4h-4v2h4v4h2v-4h4v-2h-4zm0-30V0h-2v4h-4v2h4v4h2V6h4V4h-4zM6 34v-4H4v4H0v2h4v4h2v-4h4v-2H6zM6 4V0H4v4H0v2h4v4h2V6h4V4H6z'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E");
        }
        
        .menu-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 15px -3px rgba(255, 107, 152, 0.3);
        }
        
        .gallery-img {
            transition: all 0.3s ease;
        }
        
        .gallery-img:hover {
            transform: scale(1.05);
        }
        
        .testimonial-card {
            transition: all 0.3s ease;
        }
        
        .testimonial-card:hover {
            transform: translateY(-5px);
        }
        
        .nav-link {
            position: relative;
        }
        
        .nav-link::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -2px;
            left: 0;
            background-color: #FF6B98;
            transition: width 0.3s ease;
        }
        
        .nav-link:hover::after {
            width: 100%;
        }
    </style>
</head>
<body class="bg-light text-dark">
    <!-- Navigation -->
    <nav class="bg-white shadow-md fixed w-full z-50">
        <div class="container mx-auto px-4 py-3 flex justify-between items-center">
            <a href="#" class="text-2xl font-serif font-bold text-primary">The Wilson's Lane</a>
            
            <!-- Mobile menu button -->
            <div class="md:hidden">
                <button id="mobile-menu-button" class="text-dark focus:outline-none">
                    <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
                    </svg>
                </button>
            </div>
            
            <!-- Desktop Navigation -->
            <div class="hidden md:flex space-x-8">
                <a href="#home" class="nav-link font-medium">Beranda</a>
                <a href="#about" class="nav-link font-medium">Tentang Kami</a>
                <a href="#menu" class="nav-link font-medium">Menu</a>
                <a href="#services" class="nav-link font-medium">Layanan</a>
                <a href="#gallery" class="nav-link font-medium">Galeri</a>
                <a href="#testimonials" class="nav-link font-medium">Testimoni</a>
                <a href="#contact" class="nav-link font-medium">Kontak</a>
            </div>
        </div>
        
        <!-- Mobile Navigation -->
        <div id="mobile-menu" class="hidden md:hidden bg-white pb-4 px-4">
            <a href="#home" class="block py-2 text-center">Beranda</a>
            <a href="#about" class="block py-2 text-center">Tentang Kami</a>
            <a href="#menu" class="block py-2 text-center">Menu</a>
            <a href="#services" class="block py-2 text-center">Layanan</a>
            <a href="#gallery" class="block py-2 text-center">Galeri</a>
            <a href="#testimonials" class="block py-2 text-center">Testimoni</a>
            <a href="#contact" class="block py-2 text-center">Kontak</a>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="hero-pattern pt-24 md:pt-32 pb-16 md:pb-24">
        <div class="container mx-auto px-4">
            <div class="flex flex-col md:flex-row items-center">
                <div class="md:w-1/2 mb-8 md:mb-0">
                    <h1 class="text-4xl md:text-5xl lg:text-6xl font-serif font-bold text-primary mb-4">The Wilson's Lane</h1>
                    <p class="text-lg md:text-xl mb-6">Nikmati pengalaman kuliner yang menyenangkan dengan suasana yang nyaman dan menu yang lezat.</p>
                    <div class="flex flex-col sm:flex-row gap-4">
                        <a href="#menu" class="bg-primary hover:bg-accent text-white font-medium py-3 px-6 rounded-full transition duration-300 text-center">Lihat Menu</a>
                        <a href="#contact" class="border-2 border-primary hover:bg-secondary text-primary font-medium py-3 px-6 rounded-full transition duration-300 text-center">Hubungi Kami</a>
                    </div>
                </div>
                <div class="md:w-1/2">
                    <div class="relative">
                        <div class="absolute -top-4 -left-4 w-24 h-24 bg-secondary rounded-full -z-10"></div>
                        <div class="absolute -bottom-4 -right-4 w-32 h-32 bg-accent rounded-full -z-10"></div>
                        <svg class="w-full h-auto" viewBox="0 0 500 400" xmlns="http://www.w3.org/2000/svg">
                            <rect x="50" y="50" width="400" height="300" rx="20" fill="#FFF" stroke="#FF6B98" stroke-width="5"/>
                            <circle cx="250" cy="200" r="80" fill="#FFD1DC"/>
                            <path d="M200,200 Q250,150 300,200 T400,200" stroke="#FF6B98" stroke-width="8" fill="none"/>
                            <text x="180" y="210" font-family="'Playfair Display', serif" font-size="24" fill="#4A3637" font-weight="bold">Wilson's Lane</text>
                            <path d="M150,250 Q250,300 350,250" stroke="#FF91A4" stroke-width="6" fill="none"/>
                            <circle cx="150" cy="150" r="20" fill="#FF91A4"/>
                            <circle cx="350" cy="150" r="20" fill="#FF91A4"/>
                            <rect x="200" y="250" width="100" height="30" rx="15" fill="#FF6B98"/>
                            <text x="215" y="270" font-family="'Poppins', sans-serif" font-size="14" fill="#FFF">CAFE</text>
                        </svg>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-16 bg-white">
        <div class="container mx-auto px-4">
            <div class="text-center mb-12">
                <h2 class="text-3xl md:text-4xl font-serif font-bold text-primary mb-2">Tentang Wilson's Lane</h2>
                <div class="w-24 h-1 bg-accent mx-auto"></div>
            </div>
            
            <div class="flex flex-col md:flex-row items-center gap-8">
                <div class="md:w-1/2">
                    <div class="relative">
                        <div class="absolute -top-4 -left-4 w-full h-full bg-secondary rounded-lg -z-10 transform rotate-3"></div>
                        <div class="bg-white p-6 rounded-lg shadow-lg">
                            <svg class="w-full h-auto" viewBox="0 0 400 300" xmlns="http://www.w3.org/2000/svg">
                                <rect width="400" height="300" fill="#FFF0F3" rx="10"/>
                                <circle cx="200" cy="100" r="50" fill="#FFD1DC"/>
                                <rect x="150" y="150" width="100" height="100" rx="10" fill="#FF91A4"/>
                                <circle cx="200" cy="200" r="30" fill="#FF6B98"/>
                                <path d="M170,200 Q200,170 230,200" stroke="#FFF" stroke-width="4" fill="none"/>
                                <circle cx="185" cy="190" r="5" fill="#FFF"/>
                                <circle cx="215" cy="190" r="5" fill="#FFF"/>
                                <path d="M100,250 Q200,280 300,250" stroke="#FF6B98" stroke-width="6" fill="none"/>
                                <text x="130" y="80" font-family="'Playfair Display', serif" font-size="24" fill="#4A3637" font-weight="bold">The Wilson's Lane</text>
                            </svg>
                        </div>
                    </div>
                </div>
                
                <div class="md:w-1/2">
                    <h3 class="text-2xl font-serif font-semibold text-dark mb-4">Selamat Datang di The Wilson's Lane</h3>
                    <p class="mb-4">The Wilson's Lane adalah kafe yang menggabungkan kenyamanan, cita rasa, dan keindahan dalam satu tempat. Didirikan dengan semangat untuk menciptakan ruang yang nyaman bagi semua orang, kafe kami menawarkan pengalaman kuliner yang tak terlupakan.</p>
                    <p class="mb-4">Kami menggunakan bahan-bahan berkualitas tinggi dan segar untuk setiap hidangan kami. Menu kami menggabungkan cita rasa lokal dan internasional, dengan sentuhan kreatif yang unik.</p>
                    <p class="mb-6">Suasana kafe kami dirancang untuk memberikan kenyamanan maksimal, baik untuk pertemuan santai, kerja remote, atau sekadar menikmati waktu sendiri dengan secangkir kopi.</p>
                    <div class="flex flex-wrap gap-4">
                        <div class="flex items-center">
                            <div class="w-12 h-12 bg-secondary rounded-full flex items-center justify-center mr-3">
                                <i class="fas fa-coffee text-primary text-xl"></i>
                            </div>
                            <span>Kopi Berkualitas</span>
                        </div>
                        <div class="flex items-center">
                            <div class="w-12 h-12 bg-secondary rounded-full flex items-center justify-center mr-3">
                                <i class="fas fa-utensils text-primary text-xl"></i>
                            </div>
                            <span>Menu Lezat</span>
                        </div>
                        <div class="flex items-center">
                            <div class="w-12 h-12 bg-secondary rounded-full flex items-center justify-center mr-3">
                                <i class="fas fa-wifi text-primary text-xl"></i>
                            </div>
                            <span>WiFi Gratis</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Menu Section -->
    <section id="menu" class="py-16 bg-light">
        <div class="container mx-auto px-4">
            <div class="text-center mb-12">
                <h2 class="text-3xl md:text-4xl font-serif font-bold text-primary mb-2">Menu Favorit Kami</h2>
                <div class="w-24 h-1 bg-accent mx-auto"></div>
                <p class="mt-4 text-lg">Nikmati hidangan spesial kami yang dibuat dengan cinta dan bahan berkualitas</p>
            </div>
            
            <!-- Signature Menu -->
            <div class="mb-12">
                <h3 class="text-2xl font-serif font-semibold text-center mb-8">Signature Menu</h3>
                <div class="bg-white rounded-xl shadow-lg overflow-hidden transition-all duration-300 hover:shadow-xl max-w-4xl mx-auto">
                    <div class="flex flex-col md:flex-row">
                        <div class="md:w-1/2 p-6">
                            <div class="bg-secondary rounded-lg p-4 h-full flex items-center justify-center">
                                <svg viewBox="0 0 300 200" xmlns="http://www.w3.org/2000/svg" class="w-full h-auto">
                                    <rect width="300" height="200" fill="#FFD1DC" rx="10"/>
                                    <ellipse cx="150" cy="100" rx="100" ry="60" fill="#FF91A4"/>
                                    <path d="M80,120 Q150,160 220,120" stroke="#FFF" stroke-width="8" fill="none"/>
                                    <path d="M100,90 L200,90" stroke="#FFF" stroke-width="6" fill="none"/>
                                    <path d="M110,70 L190,70" stroke="#FFF" stroke-width="4" fill="none"/>
                                    <circle cx="150" cy="50" r="20" fill="#FF6B98"/>
                                    <text x="110" y="180" font-family="'Playfair Display', serif" font-size="16" fill="#4A3637" font-weight="bold">Arsik Salmon</text>
                                </svg>
                            </div>
                        </div>
                        <div class="md:w-1/2 p-6">
                            <div class="flex justify-between items-start mb-2">
                                <h4 class="text-xl font-serif font-bold text-primary">Arsik Salmon</h4>
                                <span class="bg-primary text-white px-3 py-1 rounded-full text-sm">Signature</span>
                            </div>
                            <p class="text-sm text-gray-500 mb-4">Hidangan spesial dengan sentuhan tradisional</p>
                            <p class="mb-4">Salmon segar yang dimasak dengan bumbu arsik khas Batak, disajikan dengan nasi putih hangat dan lalapan segar. Perpaduan cita rasa lokal dan bahan premium.</p>
                            <div class="flex justify-between items-center">
                                <span class="text-xl font-bold text-dark">Rp 85.000</span>
                                <button class="bg-primary hover:bg-accent text-white px-4 py-2 rounded-full transition duration-300">Pesan Sekarang</button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- Other Menu -->
            <h3 class="text-2xl font-serif font-semibold text-center mb-8">Menu Lainnya</h3>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
                <!-- Menu Item 1 -->
                <div class="menu-item bg-white rounded-xl shadow-md overflow-hidden transition-all duration-300">
                    <div class="h-48 bg-secondary flex items-center justify-center">
                        <svg viewBox="0 0 200 150" xmlns="http://www.w3.org/2000/svg" class="w-full h-auto">
                            <rect width="200" height="150" fill="#FFD1DC" rx="5"/>
                            <circle cx="100" cy="75" r="50" fill="#FF91A4"/>
                            <rect x="70" y="60" width="60" height="40" rx="5" fill="#FFF"/>
                            <path d="M75,80 Q100,100 125,80" stroke="#FF6B98" stroke-width="3" fill="none"/>
                            <path d="M80,70 L120,70" stroke="#FF6B98" stroke-width="2" fill="none"/>
                            <path d="M85,65 L115,65" stroke="#FF6B98" stroke-width="2" fill="none"/>
                            <text x="60" y="130" font-family="'Poppins', sans-serif" font-size="12" fill="#4A3637" font-weight="bold">Nasi Goreng Jambal</text>
                        </svg>
                    </div>
                    <div class="p-4">
                        <h4 class="text-lg font-serif font-bold text-primary mb-1">Nasi Goreng Jambal</h4>
                        <p class="text-sm text-gray-600 mb-3">Nasi goreng dengan ikan jambal roti khas Batak yang gurih dan lezat</p>
                        <div class="flex justify-between items-center">
                            <span class="font-bold text-dark">Rp 45.000</span>
                            <button class="bg-primary hover:bg-accent text-white px-3 py-1 rounded-full text-sm transition duration-300">Pesan</button>
                        </div>
                    </div>
                </div>
                
                <!-- Menu Item 2 -->
                <div class="menu-item bg-white rounded-xl shadow-md overflow-hidden transition-all duration-300">
                    <div class="h-48 bg-secondary flex items-center justify-center">
                        <svg viewBox="0 0 200 150" xmlns="http://www.w3.org/2000/svg" class="w-full h-auto">
                            <rect width="200" height="150" fill="#FFD1DC" rx="5"/>
                            <circle cx="100" cy="75" r="50" fill="#FF91A4"/>
                            <rect x="70" y="50" width="60" height="50" rx="5" fill="#FFF"/>
                            <circle cx="100" cy="75" r="15" fill="#FF6B98"/>
                            <path d="M80,90 L120,90" stroke="#FF6B98" stroke-width="3" fill="none"/>
                            <path d="M85,60 L115,60" stroke="#FF6B98" stroke-width="2" fill="none"/>
                            <text x="75" y="130" font-family="'Poppins', sans-serif" font-size="12" fill="#4A3637" font-weight="bold">Egy Rice</text>
                        </svg>
                    </div>
                    <div class="p-4">
                        <h4 class="text-lg font-serif font-bold text-primary mb-1">Egy Rice</h4>
                        <p class="text-sm text-gray-600 mb-3">Nasi dengan telur mata sapi, ayam, dan saus spesial Wilson's Lane</p>
                        <div class="flex justify-between items-center">
                            <span class="font-bold text-dark">Rp 38.000</span>
                            <button class="bg-primary hover:bg-accent text-white px-3 py-1 rounded-full text-sm transition duration-300">Pesan</button>
                        </div>
                    </div>
                </div>
                
                <!-- Menu Item 3 -->
                <div class="menu-item bg-white rounded-xl shadow-md overflow-hidden transition-all duration-300">
                    <div class="h-48 bg-secondary flex items-center justify-center">
                        <svg viewBox="0 0 200 150" xmlns="http://www.w3.org/2000/svg" class="w-full h-auto">
                            <rect width="200" height="150" fill="#FFD1DC" rx="5"/>
                            <circle cx="100" cy="75" r="50" fill="#FF91A4"/>
                            <path d="M70,90 Q100,110 130,90" stroke="#FFF" stroke-width="4" fill="none"/>
                            <circle cx="85" cy="70" r="10" fill="#FFF"/>
                            <circle cx="115" cy="70" r="10" fill="#FFF"/>
                            <path d="M75,50 Q100,30 125,50" stroke="#FF6B98" stroke-width="3" fill="none"/>
                            <text x="50" y="130" font-family="'Poppins', sans-serif" font-size="12" fill="#4A3637" font-weight="bold">Chicken Butter Milk</text>
                        </svg>
                    </div>
                    <div class="p-4">
                        <h4 class="text-lg font-serif font-bold text-primary mb-1">Chicken Butter Milk</h4>
                        <p class="text-sm text-gray-600 mb-3">Ayam goreng dengan saus butter milk yang creamy dan lezat</p>
                        <div class="flex justify-between items-center">
                            <span class="font-bold text-dark">Rp 52.000</span>
                            <button class="bg-primary hover:bg-accent text-white px-3 py-1 rounded-full text-sm transition duration-300">Pesan</button>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="text-center mt-10">
                <a href="#" class="inline-block border-2 border-primary hover:bg-primary hover:text-white text-primary font-medium py-2 px-6 rounded-full transition duration-300">Lihat Menu Lengkap</a>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section id="services" class="py-16 bg-white">
        <div class="container mx-auto px-4">
            <div class="text-center mb-12">
                <h2 class="text-3xl md:text-4xl font-serif font-bold text-primary mb-2">Layanan Kami</h2>
                <div class="w-24 h-1 bg-accent mx-auto"></div>
                <p class="mt-4 text-lg">Kami menyediakan berbagai layanan untuk memenuhi kebutuhan Anda</p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- Service 1 -->
                <div class="bg-light rounded-xl shadow-md p-6 transition-all duration-300 hover:shadow-lg hover:transform hover:-translate-y-2">
                    <div class="w-16 h-16 bg-secondary rounded-full flex items-center justify-center mx-auto mb-4">
                        <i class="fas fa-coffee text-primary text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-serif font-bold text-primary text-center mb-3">Kopi & Minuman</h3>
                    <p class="text-center">Kopi pilihan single origin dan minuman spesial buatan barista.</p>
                </div>
                
                <!-- Service 2 -->
                <div class="bg-light rounded-xl shadow-md p-6 transition-all duration-300 hover:shadow-lg hover:transform hover:-translate-y-2">
                    <div class="w-16 h-16 bg-secondary rounded-full flex items-center justify-center mx-auto mb-4">
                        <i class="fas fa-leaf text-primary text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-serif font-bold text-primary text-center mb-3">Makanan Sehat</h3>
                    <p class="text-center">Menu sehat, vegetarian, vegan dan pilihan sarapan lengkap.</p>
                </div>
                
                <!-- Service 3 -->
                <div class="bg-light rounded-xl shadow-md p-6 transition-all duration-300 hover:shadow-lg hover:transform hover:-translate-y-2">
                    <div class="w-16 h-16 bg-secondary rounded-full flex items-center justify-center mx-auto mb-4">
                        <i class="fas fa-music text-primary text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-serif font-bold text-primary text-center mb-3">Acara & Workshop</h3>
                    <p class="text-center">Live music, komunitas, dan event kreatif mingguan.</p>
                </div>
            </div>
            
            <div class="mt-12 bg-secondary rounded-xl p-6 md:p-8">
                <div class="flex flex-col md:flex-row items-center">
                    <div class="md:w-2/3 mb-6 md:mb-0 md:pr-6">
                        <h3 class="text-2xl font-serif font-bold text-primary mb-3">Ingin Mengadakan Acara di Wilson's Lane?</h3>
                        <p class="mb-4">Kami menyediakan ruang yang nyaman untuk berbagai acara seperti ulang tahun, gathering, atau workshop. Hubungi kami untuk informasi lebih lanjut.</p>
                        <a href="#contact" class="inline-block bg-primary hover:bg-accent text-white font-medium py-2 px-6 rounded-full transition duration-300">Hubungi Kami</a>
                    </div>
                    <div class="md:w-1/3">
                        <svg viewBox="0 0 200 150" xmlns="http://www.w3.org/2000/svg" class="w-full h-auto">
                            <rect width="200" height="150" fill="#FFF0F3" rx="10"/>
                            <rect x="30" y="40" width="140" height="80" rx="5" fill="#FF91A4"/>
                            <circle cx="60" cy="70" r="15" fill="#FFF"/>
                            <circle cx="100" cy="70" r="15" fill="#FFF"/>
                            <circle cx="140" cy="70" r="15" fill="#FFF"/>
                            <path d="M40,100 L160,100" stroke="#FFF" stroke-width="3" stroke-dasharray="5,5" fill="none"/>
                            <path d="M50,120 L150,120" stroke="#FF6B98" stroke-width="2" fill="none"/>
                            <text x="70" y="30" font-family="'Poppins', sans-serif" font-size="12" fill="#4A3637" font-weight="bold">Events</text>
                        </svg>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Gallery Section -->
    <section id="gallery" class="py-16 bg-light">
        <div class="container mx-auto px-4">
            <div class="text-center mb-12">
                <h2 class="text-3xl md:text-4xl font-serif font-bold text-primary mb-2">Galeri</h2>
                <div class="w-24 h-1 bg-accent mx-auto"></div>
                <p class="mt-4 text-lg">Suasana dan momen di The Wilson's Lane</p>
            </div>
            
            <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4">
                <!-- Gallery Item 1 -->
                <div class="gallery-img overflow-hidden rounded-lg shadow-md">
                    <div class="bg-secondary aspect-square">
                        <svg viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg" class="w-full h-full">
                            <rect width="200" height="200" fill="#FFD1DC"/>
                            <circle cx="100" cy="100" r="70" fill="#FF91A4"/>
                            <rect x="50" y="70" width="100" height="60" rx="5" fill="#FFF"/>
                            <circle cx="80" cy="100" r="10" fill="#FF6B98"/>
                            <circle cx="120" cy="100" r="10" fill="#FF6B98"/>
                            <path d="M70,130 Q100,150 130,130" stroke="#FF6B98" stroke-width="3" fill="none"/>
                            <text x="70" y="50" font-family="'Playfair Display', serif" font-size="12" fill="#FFF" font-weight="bold">Cafe Interior</text>
                        </svg>
                    </div>
                </div>
                
                <!-- Gallery Item 2 -->
                <div class="gallery-img overflow-hidden rounded-lg shadow-md">
                    <div class="bg-accent aspect-square">
                        <svg viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg" class="w-full h-full">
                            <rect width="200" height="200" fill="#FF91A4"/>
                            <circle cx="100" cy="80" r="50" fill="#FFD1DC"/>
                            <rect x="60" y="100" width="80" height="60" rx="5" fill="#FFF"/>
                            <circle cx="100" cy="130" r="15" fill="#FF6B98"/>
                            <path d="M70,160 L130,160" stroke="#FFF" stroke-width="3" fill="none"/>
                            <text x="65" y="50" font-family="'Playfair Display', serif" font-size="12" fill="#FFF" font-weight="bold">Coffee Art</text>
                        </svg>
                    </div>
                </div>
                
                <!-- Gallery Item 3 -->
                <div class="gallery-img overflow-hidden rounded-lg shadow-md">
                    <div class="bg-primary aspect-square">
                        <svg viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg" class="w-full h-full">
                            <rect width="200" height="200" fill="#FF6B98"/>
                            <circle cx="100" cy="100" r="60" fill="#FFD1DC"/>
                            <rect x="70" y="80" width="60" height="40" rx="5" fill="#FFF"/>
                            <path d="M80,100 L120,100" stroke="#FF91A4" stroke-width="3" fill="none"/>
                            <path d="M80,110 L120,110" stroke="#FF91A4" stroke-width="3" fill="none"/>
                            <text x="60" y="60" font-family="'Playfair Display', serif" font-size="12" fill="#FFF" font-weight="bold">Signature Menu</text>
                        </svg>
                    </div>
                </div>
                
                <!-- Gallery Item 4 -->
                <div class="gallery-img overflow-hidden rounded-lg shadow-md">
                    <div class="bg-secondary aspect-square">
                        <svg viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg" class="w-full h-full">
                            <rect width="200" height="200" fill="#FFD1DC"/>
                            <rect x="40" y="60" width="120" height="80" rx="10" fill="#FF91A4"/>
                            <circle cx="70" cy="100" r="15" fill="#FFF"/>
                            <circle cx="130" cy="100" r="15" fill="#FFF"/>
                            <path d="M60,130 Q100,150 140,130" stroke="#FFF" stroke-width="3" fill="none"/>
                            <text x="60" y="50" font-family="'Playfair Display', serif" font-size="12" fill="#4A3637" font-weight="bold">Outdoor Area</text>
                        </svg>
                    </div>
                </div>
                
                <!-- Gallery Item 5 -->
                <div class="gallery-img overflow-hidden rounded-lg shadow-md">
                    <div class="bg-accent aspect-square">
                        <svg viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg" class="w-full h-full">
                            <rect width="200" height="200" fill="#FF91A4"/>
                            <circle cx="100" cy="100" r="60" fill="#FFD1DC"/>
                            <rect x="80" y="70" width="40" height="60" rx="5" fill="#FFF"/>
                            <circle cx="100" cy="90" r="10" fill="#FF6B98"/>
                            <path d="M85,110 L115,110" stroke="#FF6B98" stroke-width="2" fill="none"/>
                            <path d="M90,120 L110,120" stroke="#FF6B98" stroke-width="2" fill="none"/>
                            <text x="70" y="50" font-family="'Playfair Display', serif" font-size="12" fill="#FFF" font-weight="bold">Live Music</text>
                        </svg>
                    </div>
                </div>
                
                <!-- Gallery Item 6 -->
                <div class="gallery-img overflow-hidden rounded-lg shadow-md">
                    <div class="bg-primary aspect-square">
                        <svg viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg" class="w-full h-full">
                            <rect width="200" height="200" fill="#FF6B98"/>
                            <circle cx="100" cy="100" r="70" fill="#FFD1DC"/>
                            <rect x="70" y="70" width="60" height="60" rx="30" fill="#FFF"/>
                            <circle cx="100" cy="100" r="20" fill="#FF91A4"/>
                            <path d="M60,140 Q100,160 140,140" stroke="#FFF" stroke-width="3" fill="none"/>
                            <text x="65" y="50" font-family="'Playfair Display', serif" font-size="12" fill="#FFF" font-weight="bold">Desserts</text>
                        </svg>
                    </div>
                </div>
                
                <!-- Gallery Item 7 -->
                <div class="gallery-img overflow-hidden rounded-lg shadow-md">
                    <div class="bg-secondary aspect-square">
                        <svg viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg" class="w-full h-full">
                            <rect width="200" height="200" fill="#FFD1DC"/>
                            <rect x="50" y="50" width="100" height="100" rx="10" fill="#FF91A4"/>
                            <circle cx="100" cy="80" r="20" fill="#FFF"/>
                            <rect x="80" y="110" width="40" height="20" rx="5" fill="#FFF"/>
                            <path d="M70,150 L130,150" stroke="#FFF" stroke-width="3" fill="none"/>
                            <text x="55" y="40" font-family="'Playfair Display', serif" font-size="12" fill="#4A3637" font-weight="bold">Workshop Event</text>
                        </svg>
                    </div>
                </div>
                
                <!-- Gallery Item 8 -->
                <div class="gallery-img overflow-hidden rounded-lg shadow-md">
                    <div class="bg-accent aspect-square">
                        <svg viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg" class="w-full h-full">
                            <rect width="200" height="200" fill="#FF91A4"/>
                            <circle cx="100" cy="100" r="60" fill="#FFD1DC"/>
                            <rect x="70" y="80" width="60" height="40" rx="5" fill="#FFF"/>
                            <circle cx="85" cy="100" r="8" fill="#FF6B98"/>
                            <circle cx="115" cy="100" r="8" fill="#FF6B98"/>
                            <path d="M85,130 Q100,140 115,130" stroke="#FFF" stroke-width="2" fill="none"/>
                            <text x="60" y="60" font-family="'Playfair Display', serif" font-size="12" fill="#FFF" font-weight="bold">Cozy Corner</text>
                        </svg>
                    </div>
                </div>
            </div>
            
            <div class="text-center mt-10">
                <a href="#" class="inline-block border-2 border-primary hover:bg-primary hover:text-white text-primary font-medium py-2 px-6 rounded-full transition duration-300">Lihat Lebih Banyak</a>
            </div>
        </div>
    </section>

    <!-- Testimonials Section -->
    <section id="testimonials" class="py-16 bg-white">
        <div class="container mx-auto px-4">
            <div class="text-center mb-12">
                <h2 class="text-3xl md:text-4xl font-serif font-bold text-primary mb-2">Testimoni</h2>
                <div class="w-24 h-1 bg-accent mx-auto"></div>
                <p class="mt-4 text-lg">Apa kata mereka tentang The Wilson's Lane</p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                <!-- Testimonial 1 -->
                <div class="testimonial-card bg-light rounded-xl shadow-md p-6">
                    <div class="flex items-start mb-4">
                        <div class="w-12 h-12 bg-secondary rounded-full flex items-center justify-center mr-4">
                            <span class="text-primary font-bold text-xl">R</span>
                        </div>
                        <div>
                            <h4 class="font-bold text-primary">Rina</h4>
                            <p class="text-sm text-gray-500">Jakarta</p>
                        </div>
                    </div>
                    <div class="mb-4">
                        <div class="flex text-yellow-400 mb-2">
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                        </div>
                        <p class="italic">"Tempatnya nyaman banget, kopinya enak, staff-nya ramah. Highly recommended!"</p>
                    </div>
                </div>
                
                <!-- Testimonial 2 -->
                <div class="testimonial-card bg-light rounded-xl shadow-md p-6">
                    <div class="flex items-start mb-4">
                        <div class="w-12 h-12 bg-secondary rounded-full flex items-center justify-center mr-4">
                            <span class="text-primary font-bold text-xl">B</span>
                        </div>
                        <div>
                            <h4 class="font-bold text-primary">Budi</h4>
                            <p class="text-sm text-gray-500">Bekasi</p>
                        </div>
                    </div>
                    <div class="mb-4">
                        <div class="flex text-yellow-400 mb-2">
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star-half-alt"></i>
                        </div>
                        <p class="italic">"Saya suka suasana tamannya. Cocok buat kerja remote atau santai sore."</p>
                    </div>
                </div>
            </div>
            
            <div class="mt-12 bg-secondary rounded-xl p-6 md:p-8 text-center">
                <h3 class="text-2xl font-serif font-bold text-primary mb-4">Bagikan Pengalaman Anda</h3>
                <p class="mb-6">Kami sangat menghargai masukan dari Anda untuk terus meningkatkan layanan kami</p>
                <a href="#" class="inline-block bg-primary hover:bg-accent text-white font-medium py-2 px-6 rounded-full transition duration-300">Tulis Review</a>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-16 bg-light">
        <div class="container mx-auto px-4">
            <div class="text-center mb-12">
                <h2 class="text-3xl md:text-4xl font-serif font-bold text-primary mb-2">Hubungi Kami</h2>
                <div class="w-24 h-1 bg-accent mx-auto"></div>
                <p class="mt-4 text-lg">Kami siap melayani Anda</p>
            </div>
            
            <div class="flex flex-col md:flex-row gap-8">
                <div class="md:w-1/2">
                    <div class="bg-white rounded-xl shadow-md p-6">
                        <h3 class="text-xl font-serif font-bold text-primary mb-4">Informasi Kontak</h3>
                        
                        <div class="flex items-start mb-4">
                            <div class="w-10 h-10 bg-secondary rounded-full flex items-center justify-center mr-4">
                                <i class="fas fa-map-marker-alt text-primary"></i>
                            </div>
                            <div>
                                <h4 class="font-bold">Alamat</h4>
                                <p>Jl. Tegal No.4, Menteng, Jakarta Pusat</p>
                            </div>
                        </div>
                        
                        <div class="flex items-start mb-4">
                            <div class="w-10 h-10 bg-secondary rounded-full flex items-center justify-center mr-4">
                                <i class="fas fa-envelope text-primary"></i>
                            </div>
                            <div>
                                <h4 class="font-bold">Email</h4>
                                <p>info@wilsonslane.com</p>
                            </div>
                        </div>
                        
                        <div class="flex items-start mb-4">
                            <div class="w-10 h-10 bg-secondary rounded-full flex items-center justify-center mr-4">
                                <i class="fab fa-whatsapp text-primary"></i>
                            </div>
                            <div>
                                <h4 class="font-bold">WhatsApp</h4>
                                <p>0812-3456-7890</p>
                            </div>
                        </div>
                        
                        <div class="flex items-start">
                            <div class="w-10 h-10 bg-secondary rounded-full flex items-center justify-center mr-4">
                                <i class="fas fa-clock text-primary"></i>
                            </div>
                            <div>
                                <h4 class="font-bold">Jam Buka</h4>
                                <p>Senin - Jumat: 08.00 - 22.00</p>
                                <p>Sabtu - Minggu: 09.00 - 23.00</p>
                            </div>
                        </div>
                        
                        <div class="mt-6">
                            <h4 class="font-bold mb-2">Ikuti Kami</h4>
                            <div class="flex space-x-4">
                                <a href="#" class="w-10 h-10 bg-secondary rounded-full flex items-center justify-center hover:bg-primary hover:text-white transition duration-300">
                                    <i class="fab fa-instagram"></i>
                                </a>
                                <a href="#" class="w-10 h-10 bg-secondary rounded-full flex items-center justify-center hover:bg-primary hover:text-white transition duration-300">
                                    <i class="fab fa-facebook-f"></i>
                                </a>
                                <a href="#" class="w-10 h-10 bg-secondary rounded-full flex items-center justify-center hover:bg-primary hover:text-white transition duration-300">
                                    <i class="fab fa-twitter"></i>
                                </a>
                                <a href="#" class="w-10 h-10 bg-secondary rounded-full flex items-center justify-center hover:bg-primary hover:text-white transition duration-300">
                                    <i class="fab fa-tiktok"></i>
                                </a>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="md:w-1/2">
                    <div class="bg-white rounded-xl shadow-md p-6">
                        <h3 class="text-xl font-serif font-bold text-primary mb-4">Kirim Pesan</h3>
                        
                        <form id="contactForm" class="space-y-4">
                            <div>
                                <label for="name" class="block text-sm font-medium text-gray-700 mb-1">Nama</label>
                                <input type="text" id="name" name="name" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-primary">
                            </div>
                            
                            <div>
                                <label for="email" class="block text-sm font-medium text-gray-700 mb-1">Email</label>
                                <input type="email" id="email" name="email" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-primary">
                            </div>
                            
                            <div>
                                <label for="subject" class="block text-sm font-medium text-gray-700 mb-1">Subjek</label>
                                <input type="text" id="subject" name="subject" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-primary">
                            </div>
                            
                            <div>
                                <label for="message" class="block text-sm font-medium text-gray-700 mb-1">Pesan</label>
                                <textarea id="message" name="message" rows="4" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-primary"></textarea>
                            </div>
                            
                            <div>
                                <button type="submit" class="w-full bg-primary hover:bg-accent text-white font-medium py-2 px-6 rounded-lg transition duration-300">Kirim Pesan</button>
                            </div>
                        </form>
                    </div>
                </div>
            </div>
            
            <div class="mt-12 bg-white rounded-xl shadow-md p-6">
                <h3 class="text-xl font-serif font-bold text-primary mb-4 text-center">Lokasi Kami</h3>
                <div class="bg-secondary h-64 rounded-lg flex items-center justify-center">
                    <svg viewBox="0 0 400 200" xmlns="http://www.w3.org/2000/svg" class="w-full h-auto">
                        <rect width="400" height="200" fill="#FFD1DC" rx="5"/>
                        <rect x="50" y="40" width="300" height="120" rx="5" fill="#FFF"/>
                        <circle cx="200" cy="100" r="20" fill="#FF6B98"/>
                        <path d="M200,80 L200,120" stroke="#FFF" stroke-width="2" fill="none"/>
                        <path d="M180,100 L220,100" stroke="#FFF" stroke-width="2" fill="none"/>
                        <path d="M80,60 L320,60" stroke="#FF91A4" stroke-width="1" fill="none"/>
                        <path d="M80,80 L320,80" stroke="#FF91A4" stroke-width="1" fill="none"/>
                        <path d="M80,100 L180,100" stroke="#FF91A4" stroke-width="1" fill="none"/>
                        <path d="M220,100 L320,100" stroke="#FF91A4" stroke-width="1" fill="none"/>
                        <path d="M80,120 L320,120" stroke="#FF91A4" stroke-width="1" fill="none"/>
                        <path d="M80,140 L320,140" stroke="#FF91A4" stroke-width="1" fill="none"/>
                        <text x="130" y="180" font-family="'Poppins', sans-serif" font-size="12" fill="#4A3637" font-weight="bold">Jl. Tegal No.4, Menteng, Jakarta Pusat</text>
                    </svg>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-dark text-white py-8">
        <div class="container mx-auto px-4">
            <div class="flex flex-col md:flex-row justify-between">
                <div class="mb-6 md:mb-0">
                    <h3 class="text-2xl font-serif font-bold text-primary mb-4">The Wilson's Lane</h3>
                    <p class="max-w-xs">Tempat yang nyaman untuk menikmati kopi dan makanan lezat dengan suasana yang menyenangkan.</p>
                </div>
                
                <div class="mb-6 md:mb-0">
                    <h4 class="text-lg font-bold mb-4">Link Cepat</h4>
                    <ul class="space-y-2">
                        <li><a href="#home" class="hover:text-primary transition duration-300">Beranda</a></li>
                        <li><a href="#about" class="hover:text-primary transition duration-300">Tentang Kami</a></li>
                        <li><a href="#menu" class="hover:text-primary transition duration-300">Menu</a></li>
                        <li><a href="#gallery" class="hover:text-primary transition duration-300">Galeri</a></li>
                        <li><a href="#contact" class="hover:text-primary transition duration-300">Kontak</a></li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="text-lg font-bold mb-4">Hubungi Kami</h4>
                    <ul class="space-y-2">
                        <li class="flex items-center">
                            <i class="fas fa-map-marker-alt text-primary mr-2"></i>
                            <span>Jl. Tegal No.4, Menteng, Jakarta Pusat</span>
                        </li>
                        <li class="flex items-center">
                            <i class="fas fa-envelope text-primary mr-2"></i>
                            <span>info@wilsonslane.com</span>
                        </li>
                        <li class="flex items-center">
                            <i class="fab fa-whatsapp text-primary mr-2"></i>
                            <span>0812-3456-7890</span>
                        </li>
                    </ul>
                </div>
            </div>
            
            <div class="border-t border-gray-700 mt-8 pt-6 flex flex-col md:flex-row justify-between items-center">
                <p>&copy; 2023 The Wilson's Lane. All rights reserved.</p>
                <div class="flex space-x-4 mt-4 md:mt-0">
                    <a href="#" class="hover:text-primary transition duration-300"><i class="fab fa-instagram"></i></a>
                    <a href="#" class="hover:text-primary transition duration-300"><i class="fab fa-facebook-f"></i></a>
                    <a href="#" class="hover:text-primary transition duration-300"><i class="fab fa-twitter"></i></a>
                    <a href="#" class="hover:text-primary transition duration-300"><i class="fab fa-tiktok"></i></a>
                </div>
            </div>
        </div>
    </footer>

    <script>
        // Mobile menu toggle
        const mobileMenuButton = document.getElementById('mobile-menu-button');
        const mobileMenu = document.getElementById('mobile-menu');
        
        mobileMenuButton.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });
        
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                // Close mobile menu if open
                mobileMenu.classList.add('hidden');
                
                const targetId = this.getAttribute('href');
                const targetElement = document.querySelector(targetId);
                
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                }
            });
        });
        
        // Contact form submission
        const contactForm = document.getElementById('contactForm');
        
        contactForm.addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Get form values
            const name = document.getElementById('name').value;
            const email = document.getElementById('email').value;
            const subject = document.getElementById('subject').value;
            const message = document.getElementById('message').value;
            
            // Simple validation
            if (!name || !email || !message) {
                alert('Mohon lengkapi semua field yang diperlukan');
                return;
            }
            
            // Show success message (in a real app, you would send this data to a server)
            alert('Terima kasih! Pesan Anda telah terkirim. Kami akan segera menghubungi Anda.');
            
            // Reset form
            contactForm.reset();
        });
    </script>
<script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'965d1849e256f8c6',t:'MTc1MzYyOTM1NC4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
