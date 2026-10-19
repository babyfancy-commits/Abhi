```html
<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aaron Fancy Store | High Fashion Meets Himalayan Heritage</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts: Playfair Display & Plus Jakarta Sans -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400..900;1,400..900&family=Plus+Jakarta+Sans:wght@300;400;500;600;700&display=swap" rel="stylesheet">

    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        nepal: {
                            crimson: '#800020',
                            crimsonDark: '#580016',
                            gold: '#D4AF37',
                            goldLight: '#F3E5AB',
                            goldDark: '#B38B27',
                            terracotta: '#C85A32',
                            charcoal: '#1C1A27',
                            cardBg: '#252233',
                            ivory: '#FFFDF8',
                            muted: '#A29EAF'
                        }
                    },
                    fontFamily: {
                        serif: ['Playfair Display', 'serif'],
                        sans: ['Plus Jakarta Sans', 'sans-serif']
                    }
                }
            }
        }
    </script>

    <style>
        /* Custom scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #1C1A27;
        }
        ::-webkit-scrollbar-thumb {
            background: #800020;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #D4AF37;
        }

        /* Dhaka Pattern Styling Accent */
        .dhaka-pattern-border {
            background: repeating-linear-gradient(
                45deg,
                #800020,
                #800020 10px,
                #D4AF37 10px,
                #D4AF37 15px,
                #C85A32 15px,
                #C85A32 25px,
                #1C1A27 25px,
                #1C1A27 30px
            );
        }

        .gold-gradient-text {
            background: linear-gradient(135deg, #FFFDF8 0%, #D4AF37 50%, #B38B27 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .glass-nav {
            background: rgba(28, 26, 39, 0.92);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
        }

        .dhaka-bg-subtle {
            background-color: #1C1A27;
            background-image: radial-gradient(#D4AF37 0.75px, transparent 0.75px), radial-gradient(#800020 0.75px, #1C1A27 0.75px);
            background-size: 30px 30px;
            background-position: 0 0, 15px 15px;
            background-opacity: 0.15;
        }
    </style>
</head>
<body class="bg-nepal-charcoal text-nepal-ivory font-sans antialiased selection:bg-nepal-gold selection:text-nepal-charcoal min-h-screen flex flex-col justify-between overflow-x-hidden">

    <!-- Toast Notification Container -->
    <div id="toast-container" class="fixed bottom-6 right-6 z-50 flex flex-col gap-3 pointer-events-none"></div>

    <!-- Dhaka Accent Top Border Ribbon -->
    <div class="h-1.5 w-full dhaka-pattern-border"></div>

    <!-- Announcement Bar -->
    <div class="bg-nepal-crimson border-b border-nepal-gold/30 text-[11px] sm:text-xs py-2 px-4 text-center text-nepal-gold font-medium uppercase tracking-widest flex items-center justify-center gap-2">
        <span class="animate-spin text-nepal-gold">✦</span>
        <span>Complimentary Express Shipping on Orders Over NRs. 50,000 ($400 USD)</span>
        <span class="animate-spin text-nepal-gold">✦</span>
    </div>

    <!-- Navigation Bar -->
    <header class="sticky top-0 z-40 glass-nav border-b border-white/10 transition-all duration-300">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-20">

                <!-- Mobile Menu Button -->
                <button id="mobile-menu-btn" class="lg:hidden text-nepal-ivory hover:text-nepal-gold p-2">
                    <i class="fa-solid fa-bars text-xl"></i>
                </button>

                <!-- Brand Logo with Mandala SVG Emblem -->
                <a href="#" class="flex items-center space-x-3 group">
                    <div class="w-10 h-10 rounded-full border border-nepal-gold/50 flex items-center justify-center bg-nepal-crimson/30 group-hover:border-nepal-gold transition-colors">
                        <!-- Mandala Geometric Icon -->
                        <svg class="w-6 h-6 text-nepal-gold group-hover:rotate-45 transition-transform duration-700" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
                            <circle cx="12" cy="12" r="9" stroke="currentColor"/>
                            <path d="M12 3v18M3 12h18M5.636 5.636l12.728 12.728M5.636 18.364L18.364 5.636"/>
                            <circle cx="12" cy="12" r="3" fill="currentColor"/>
                        </svg>
                    </div>
                    <div class="flex flex-col">
                        <span class="font-serif text-xl sm:text-2xl font-bold tracking-widest gold-gradient-text uppercase">Aaron</span>
                        <span class="text-[8px] tracking-[0.35em] text-nepal-gold/80 uppercase -mt-1 font-semibold">Fancy Store</span>
                    </div>
                </a>

                <!-- Desktop Menu -->
                <nav class="hidden lg:flex items-center space-x-8 text-xs uppercase tracking-[0.2em] font-medium">
                    <a href="#hero" class="hover:text-nepal-gold transition-colors">Home</a>
                    <a href="#catalog" class="hover:text-nepal-gold transition-colors">Collections</a>
                    <a href="#heritage" class="hover:text-nepal-gold transition-colors">Himalayan Craft</a>
                    <a href="#custom-tailoring" class="hover:text-nepal-gold transition-colors">Royal Bespoke</a>
                    <a href="#testimonials" class="hover:text-nepal-gold transition-colors">Patrons</a>
                </nav>

                <!-- Header Action Buttons -->
                <div class="flex items-center space-x-4">
                    <button id="search-toggle-btn" class="text-nepal-ivory hover:text-nepal-gold p-2 transition-colors" title="Search">
                        <i class="fa-solid fa-magnifying-glass text-lg"></i>
                    </button>
                    <button id="wishlist-btn" class="relative text-nepal-ivory hover:text-nepal-gold p-2 transition-colors" title="Wishlist">
                        <i class="fa-solid fa-heart text-lg"></i>
                        <span id="wishlist-badge" class="absolute top-1 -right-1 bg-nepal-terracotta text-white text-[9px] font-bold w-4 h-4 rounded-full flex items-center justify-center opacity-0 scale-50 transition-all">0</span>
                    </button>
                    <button id="cart-toggle-btn" class="relative text-nepal-ivory hover:text-nepal-gold p-2 transition-colors" title="Shopping Bag">
                        <i class="fa-solid fa-bag-shopping text-xl"></i>
                        <span id="cart-badge" class="absolute top-1 -right-1 bg-nepal-gold text-nepal-charcoal text-[10px] font-bold w-4 h-4 rounded-full flex items-center justify-center opacity-0 scale-50 transition-all">0</span>
                    </button>
                </div>
            </div>
        </div>

        <!-- Mobile Drawer Navigation -->
        <div id="mobile-menu" class="hidden lg:hidden bg-nepal-charcoal border-b border-nepal-gold/30 px-6 py-6">
            <div class="flex flex-col space-y-4 text-xs uppercase tracking-widest font-medium">
                <a href="#hero" class="mobile-link py-2 border-b border-white/5 hover:text-nepal-gold">Home</a>
                <a href="#catalog" class="mobile-link py-2 border-b border-white/5 hover:text-nepal-gold">Collections</a>
                <a href="#heritage" class="mobile-link py-2 border-b border-white/5 hover:text-nepal-gold">Himalayan Craft</a>
                <a href="#custom-tailoring" class="mobile-link py-2 border-b border-white/5 hover:text-nepal-gold">Royal Bespoke</a>
                <a href="#testimonials" class="mobile-link py-2 hover:text-nepal-gold">Patrons</a>
            </div>
        </div>

        <!-- Search Overlay -->
        <div id="search-bar" class="hidden bg-nepal-charcoal border-b border-nepal-gold/30 px-4 py-4">
            <div class="max-w-2xl mx-auto relative">
                <input type="text" id="search-input" placeholder="Search Dhaka blazers, Pashmina shawls, Velvet gowns..." class="w-full bg-nepal-cardBg border border-nepal-gold/30 py-3 pl-4 pr-10 text-sm text-nepal-ivory focus:outline-none focus:border-nepal-gold">
                <button id="search-close-btn" class="absolute right-3 top-1/2 -translate-y-1/2 text-nepal-muted hover:text-nepal-gold">
                    <i class="fa-solid fa-xmark text-lg"></i>
                </button>
            </div>
        </div>
    </header>

    <main>
        <!-- Hero Section -->
        <section id="hero" class="relative min-h-[85vh] flex items-center justify-center overflow-hidden dhaka-bg-subtle">
            <!-- Background Backdrop Image with Deep Crimson Gradient Overlay -->
            <div class="absolute inset-0 z-0">
                <img src="https://images.unsplash.com/photo-1544441893-675973e31985?q=80&w=2000&auto=format&fit=crop" alt="High Fashion Nepali Model" class="w-full h-full object-cover object-top opacity-35 scale-105">
                <div class="absolute inset-0 bg-gradient-to-t from-nepal-charcoal via-nepal-charcoal/70 to-transparent"></div>
            </div>

            <div class="relative z-10 max-w-5xl mx-auto px-4 text-center py-20">
                <!-- Royal Gold Crest Badge -->
                <div class="inline-flex items-center gap-2 border border-nepal-gold/40 bg-nepal-crimson/40 backdrop-blur-md px-4 py-1.5 rounded-full mb-6">
                    <span class="text-xs text-nepal-gold font-semibold uppercase tracking-[0.3em]">High Fashion Meets Himalayan Heritage</span>
                </div>

                <h1 class="font-serif text-4xl sm:text-6xl md:text-7xl font-normal leading-tight text-white mb-6">
                    Regal Palpali Dhaka &<br>
                    <span class="italic gold-gradient-text font-light">Pure Himalayan Cashmere</span>
                </h1>

                <p class="text-sm sm:text-base text-nepal-ivory/80 max-w-2xl mx-auto font-light mb-10 leading-relaxed">
                    At Aaron Fancy Store, we fuse royal Nepalese textiles with modern runway silhouettes. Experience handwoven Palpali Dhaka, regal velvet Daura-Suruwal blazers, and pure Mustang cashmere.
                </p>

                <div class="flex flex-col sm:flex-row items-center justify-center gap-4">
                    <a href="#catalog" class="w-full sm:w-auto px-8 py-4 bg-nepal-crimson border border-nepal-gold text-nepal-gold text-xs uppercase tracking-[0.2em] font-semibold hover:bg-nepal-gold hover:text-nepal-charcoal transition-all shadow-xl">
                        Explore Heritage Collection
                    </a>
                    <button onclick="openCustomTailoringModal()" class="w-full sm:w-auto px-8 py-4 border border-white/20 hover:border-nepal-gold text-nepal-ivory hover:text-nepal-gold text-xs uppercase tracking-[0.2em] font-semibold transition-all">
                        Request Royal Bespoke
                    </button>
                </div>
            </div>
        </section>

        <!-- Craftsmanship & Material Highlights -->
        <section id="heritage" class="py-16 bg-nepal-cardBg border-y border-nepal-gold/20 relative">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center max-w-2xl mx-auto mb-12">
                    <p class="text-xs uppercase tracking-[0.3em] text-nepal-gold font-semibold mb-2">Sacred Artistry</p>
                    <h2 class="font-serif text-3xl sm:text-4xl text-white font-normal">Himalayan Crafts</h2>
                    <div class="w-16 h-[2px] bg-nepal-gold mx-auto mt-3"></div>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
                    <!-- Material 1 -->
                    <div class="bg-nepal-charcoal p-6 border border-white/5 hover:border-nepal-gold/40 transition-all text-center">
                        <div class="w-12 h-12 rounded-full border border-nepal-gold/40 mx-auto flex items-center justify-center text-nepal-gold mb-4">
                            <i class="fa-solid fa-feather text-lg"></i>
                        </div>
                        <h3 class="font-serif text-lg text-white mb-2">Mustang Pashmina</h3>
                        <p class="text-xs text-nepal-muted leading-relaxed font-light">Combed from high-altitude Himalayan Capra goats, providing peerless lightness and warmth.</p>
                    </div>

                    <!-- Material 2 -->
                    <div class="bg-nepal-charcoal p-6 border border-white/5 hover:border-nepal-gold/40 transition-all text-center">
                        <div class="w-12 h-12 rounded-full border border-nepal-gold/40 mx-auto flex items-center justify-center text-nepal-gold mb-4">
                            <i class="fa-solid fa-shapes text-lg"></i>
                        </div>
                        <h3 class="font-serif text-lg text-white mb-2">Palpali Dhaka Weave</h3>
                        <p class="text-xs text-nepal-muted leading-relaxed font-light">Handloom geometric patterns woven thread by thread by master artisans in Palpa and Tehrathum.</p>
                    </div>

                    <!-- Material 3 -->
                    <div class="bg-nepal-charcoal p-6 border border-white/5 hover:border-nepal-gold/40 transition-all text-center">
                        <div class="w-12 h-12 rounded-full border border-nepal-gold/40 mx-auto flex items-center justify-center text-nepal-gold mb-4">
                            <i class="fa-solid fa-crown text-lg"></i>
                        </div>
                        <h3 class="font-serif text-lg text-white mb-2">Royal Crimson Velvet</h3>
                        <p class="text-xs text-nepal-muted leading-relaxed font-light">Rich velvet textiles inspired by ancient Malla and Shah dynasty court attire.</p>
                    </div>

                    <!-- Material 4 -->
                    <div class="bg-nepal-charcoal p-6 border border-white/5 hover:border-nepal-gold/40 transition-all text-center">
                        <div class="w-12 h-12 rounded-full border border-nepal-gold/40 mx-auto flex items-center justify-center text-nepal-gold mb-4">
                            <i class="fa-solid fa-gem text-lg"></i>
                        </div>
                        <h3 class="font-serif text-lg text-white mb-2">Silversmith Accents</h3>
                        <p class="text-xs text-nepal-muted leading-relaxed font-light">Custom silver & gold buttons handcrafted by Newari artisans in Patan.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Product Catalog Section -->
        <section id="catalog" class="py-20 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-2xl mx-auto mb-12">
                <p class="text-xs uppercase tracking-[0.3em] text-nepal-gold font-semibold mb-2">Curated Runway Lineup</p>
                <h2 class="font-serif text-3xl sm:text-5xl text-white font-normal mb-4">The Collections</h2>
                <div class="w-16 h-[2px] bg-nepal-gold mx-auto mb-6"></div>
                <p class="text-xs sm:text-sm text-nepal-muted">Handcrafted garments tailored for contemporary elegance.</p>
            </div>

            <!-- Filter Buttons -->
            <div class="flex flex-wrap items-center justify-center gap-2 sm:gap-4 mb-12" id="filter-tabs">
                <button data-filter="all" class="filter-btn active px-5 py-2 text-xs uppercase tracking-widest border border-nepal-gold bg-nepal-gold text-nepal-charcoal font-semibold transition-all">All Pieces</button>
                <button data-filter="royal-men" class="filter-btn px-5 py-2 text-xs uppercase tracking-widest border border-white/10 text-nepal-ivory hover:border-nepal-gold transition-all">Royal Men</button>
                <button data-filter="heritage-women" class="filter-btn px-5 py-2 text-xs uppercase tracking-widest border border-white/10 text-nepal-ivory hover:border-nepal-gold transition-all">Heritage Women</button>
                <button data-filter="shawls" class="filter-btn px-5 py-2 text-xs uppercase tracking-widest border border-white/10 text-nepal-ivory hover:border-nepal-gold transition-all">Pashmina & Shawls</button>
                <button data-filter="dhaka-fusion" class="filter-btn px-5 py-2 text-xs uppercase tracking-widest border border-white/10 text-nepal-ivory hover:border-nepal-gold transition-all">Dhaka Fusion</button>
            </div>

            <!-- Product Grid -->
            <div id="product-grid" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-8">
                <!-- Rendered dynamically -->
            </div>
        </section>

        <!-- Royal Bespoke Tailoring CTA Banner -->
        <section id="custom-tailoring" class="py-20 bg-nepal-crimsonDark relative border-y border-nepal-gold/30 overflow-hidden">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
                <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                    <div class="space-y-6">
                        <span class="text-xs uppercase tracking-[0.3em] text-nepal-gold font-semibold">Bespoke Royal Fitting</span>
                        <h2 class="font-serif text-3xl sm:text-5xl text-white font-normal leading-tight">Tailored to Royal Precision</h2>
                        <p class="text-xs sm:text-sm text-nepal-ivory/80 leading-relaxed font-light">
                            Require custom measurements for wedding attire, formal galas, or authentic Daura-Suruwal coats? Our master tailors in Kathmandu craft bespoke garments tailored precisely to your silhouette using authentic Palpali Dhaka and raw silks.
                        </p>
                        <button onclick="openCustomTailoringModal()" class="px-8 py-4 bg-nepal-gold text-nepal-charcoal text-xs font-semibold uppercase tracking-[0.2em] hover:bg-nepal-goldLight transition-all">
                            Book Fitting Session
                        </button>
                    </div>
                    <div class="relative">
                        <div class="aspect-[4/3] overflow-hidden border border-nepal-gold/40">
                            <img src="https://images.unsplash.com/photo-1558769132-cb1aea458c5e?q=80&w=1000&auto=format&fit=crop" alt="Tailoring Craftsmanship" class="w-full h-full object-cover">
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Patron Testimonials -->
        <section id="testimonials" class="py-20 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-2xl mx-auto mb-16">
                <p class="text-xs uppercase tracking-[0.3em] text-nepal-gold font-semibold mb-2">Voices of Distinction</p>
                <h2 class="font-serif text-3xl sm:text-4xl text-white font-normal">Patron Testimonials</h2>
                <div class="w-12 h-[2px] bg-nepal-gold mx-auto mt-4"></div>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div class="bg-nepal-cardBg p-8 border border-white/5 relative">
                    <div class="text-nepal-gold text-sm mb-4">
                        <i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i>
                    </div>
                    <p class="text-xs text-nepal-ivory/90 italic font-light mb-6 leading-relaxed">
                        "The Palpali Dhaka Blazer from Aaron Fancy Store is a masterpiece. Wearing it in London drew endless compliments. True Himalayan luxury!"
                    </p>
                    <h4 class="font-serif text-sm text-white font-semibold">Prashant M. Shrestha</h4>
                    <p class="text-[10px] text-nepal-muted uppercase tracking-widest">Architect, London</p>
                </div>

                <div class="bg-nepal-cardBg p-8 border border-nepal-gold/30 relative">
                    <div class="text-nepal-gold text-sm mb-4">
                        <i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i>
                    </div>
                    <p class="text-xs text-nepal-ivory/90 italic font-light mb-6 leading-relaxed">
                        "The Mustang Pashmina Shawl feels lighter than air yet exceptionally warm. The gold embroidery details are exquisitely executed."
                    </p>
                    <h4 class="font-serif text-sm text-white font-semibold">Ananya K. Thapa</h4>
                    <p class="text-[10px] text-nepal-muted uppercase tracking-widest">Fashion Curator, Kathmandu</p>
                </div>

                <div class="bg-nepal-cardBg p-8 border border-white/5 relative">
                    <div class="text-nepal-gold text-sm mb-4">
                        <i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i>
                    </div>
                    <p class="text-xs text-nepal-ivory/90 italic font-light mb-6 leading-relaxed">
                        "Exceptional bespoke experience! They crafted a tailored velvet dinner jacket with subtle Dhaka lapels for my wedding reception."
                    </p>
                    <h4 class="font-serif text-sm text-white font-semibold">Rohan Dev Rana</h4>
                    <p class="text-[10px] text-nepal-muted uppercase tracking-widest">Entrepreneur, New York</p>
                </div>
            </div>
        </section>

        <!-- Newsletter Sign-up -->
        <section class="py-16 bg-nepal-cardBg border-t border-white/10">
            <div class="max-w-4xl mx-auto px-4 text-center">
                <i class="fa-solid fa-crown text-3xl text-nepal-gold mb-4"></i>
                <h2 class="font-serif text-3xl text-white mb-2">Join the Royal Circle</h2>
                <p class="text-xs text-nepal-muted max-w-md mx-auto mb-6">Receive 10% off your first handcrafted piece and private invitations to new Dhaka collection drops.</p>
                <form id="newsletter-form" class="flex flex-col sm:flex-row max-w-md mx-auto gap-3">
                    <input type="email" required placeholder="Enter your email address..." class="flex-1 bg-nepal-charcoal border border-white/20 py-3 px-4 text-xs text-nepal-ivory focus:outline-none focus:border-nepal-gold">
                    <button type="submit" class="px-6 py-3 bg-nepal-crimson border border-nepal-gold text-nepal-gold text-xs font-semibold uppercase tracking-widest hover:bg-nepal-gold hover:text-nepal-charcoal transition-all">
                        Subscribe
                    </button>
                </form>
            </div>
        </section>
    </main>

    <!-- Footer -->
    <footer class="bg-nepal-charcoal border-t border-nepal-gold/20 py-12 text-nepal-muted text-xs">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8 mb-10">
                <div class="space-y-3">
                    <div class="flex items-center space-x-2">
                        <div class="w-8 h-8 rounded-full border border-nepal-gold flex items-center justify-center text-nepal-gold">✦</div>
                        <span class="font-serif text-lg font-bold gold-gradient-text uppercase">Aaron Fancy Store</span>
                    </div>
                    <p class="text-nepal-muted/80 leading-relaxed">
                        High Fashion Meets Himalayan Heritage. Modern luxury crafted with centuries-old Nepalese handloom weaves and noble materials.
                    </p>
                </div>

                <div>
                    <h4 class="text-white uppercase tracking-widest font-semibold mb-3">Flagship Boutiques</h4>
                    <ul class="space-y-1.5 text-nepal-muted">
                        <li>Kathmandu: Durbar Marg</li>
                        <li>Pokhara: Lakeside Avenue</li>
                        <li>London: Mayfair Studio</li>
                        <li>New York: Fifth Avenue</li>
                    </ul>
                </div>

                <div>
                    <h4 class="text-white uppercase tracking-widest font-semibold mb-3">Client Services</h4>
                    <ul class="space-y-1.5">
                        <li><a href="#" class="hover:text-nepal-gold transition-colors">Bespoke Fittings</a></li>
                        <li><a href="#" class="hover:text-nepal-gold transition-colors">Worldwide Shipping</a></li>
                        <li><a href="#" class="hover:text-nepal-gold transition-colors">Care & Pashmina Preservation</a></li>
                        <li><a href="#" class="hover:text-nepal-gold transition-colors">Authenticity Guarantee</a></li>
                    </ul>
                </div>

                <div>
                    <h4 class="text-white uppercase tracking-widest font-semibold mb-3">Connect</h4>
                    <div class="flex space-x-4 text-base text-nepal-ivory mb-4">
                        <a href="#" class="hover:text-nepal-gold"><i class="fa-brands fa-instagram"></i></a>
                        <a href="#" class="hover:text-nepal-gold"><i class="fa-brands fa-facebook"></i></a>
                        <a href="#" class="hover:text-nepal-gold"><i class="fa-brands fa-pinterest"></i></a>
                    </div>
                    <p class="text-[11px]">Concierge: +977 1 4220000</p>
                </div>
            </div>

            <div class="border-t border-white/5 pt-6 text-center text-[11px] text-nepal-muted/60">
                <p>&copy; 2026 Aaron Fancy Store. All rights reserved. Crafted with Himalayan Craftsmanship.</p>
            </div>
        </div>
    </footer>

    <!-- Shopping Cart Drawer -->
    <div id="cart-drawer-backdrop" class="fixed inset-0 bg-black/70 backdrop-blur-sm z-50 opacity-0 pointer-events-none transition-opacity duration-300"></div>
    <div id="cart-drawer" class="fixed top-0 right-0 h-full w-full sm:w-[420px] bg-nepal-charcoal z-50 translate-x-full transition-transform duration-300 flex flex-col justify-between border-l border-nepal-gold/30">
        <!-- Cart Header -->
        <div class="p-5 border-b border-white/10 flex items-center justify-between">
            <div class="flex items-center space-x-2">
                <i class="fa-solid fa-bag-shopping text-nepal-gold"></i>
                <h3 class="font-serif text-base text-white font-medium">Your Royal Bag</h3>
            </div>
            <button id="cart-close-btn" class="text-nepal-muted hover:text-nepal-gold">
                <i class="fa-solid fa-xmark text-lg"></i>
            </button>
        </div>

        <!-- Cart Items -->
        <div id="cart-items-container" class="flex-1 overflow-y-auto p-5 space-y-4">
            <!-- Dynamic Cart Items -->
        </div>

        <!-- Cart Footer -->
        <div class="p-5 border-t border-white/10 bg-nepal-cardBg space-y-3">
            <div class="space-y-1 text-xs">
                <div class="flex justify-between text-nepal-muted">
                    <span>Subtotal</span>
                    <span id="cart-subtotal" class="text-white font-semibold">NRs. 0</span>
                </div>
                <div class="flex justify-between text-nepal-muted">
                    <span>USD Equivalent</span>
                    <span id="cart-usd-subtotal" class="text-nepal-gold">$0 USD</span>
                </div>
            </div>
            <button id="checkout-btn" class="w-full py-3.5 bg-nepal-gold text-nepal-charcoal text-xs font-semibold uppercase tracking-widest hover:bg-nepal-goldLight transition-colors">
                Proceed To Checkout
            </button>
        </div>
    </div>

    <!-- Quick View Product Modal Backdrop -->
    <div id="modal-backdrop" class="fixed inset-0 bg-black/80 backdrop-blur-md z-50 opacity-0 pointer-events-none transition-opacity duration-300 flex items-center justify-center p-4">
        <div id="product-modal" class="bg-nepal-cardBg border border-nepal-gold/40 w-full max-w-3xl overflow-hidden shadow-2xl relative scale-95 transition-transform duration-300">
            <button id="modal-close-btn" class="absolute top-4 right-4 z-10 w-8 h-8 bg-nepal-charcoal border border-white/20 text-white hover:text-nepal-gold flex items-center justify-center">
                <i class="fa-solid fa-xmark"></i>
            </button>
            <div id="modal-content" class="grid grid-cols-1 md:grid-cols-2">
                <!-- Dynamically populated -->
            </div>
        </div>
    </div>

    <!-- Custom Bespoke Modal Backdrop -->
    <div id="bespoke-modal-backdrop" class="fixed inset-0 bg-black/80 backdrop-blur-md z-50 opacity-0 pointer-events-none transition-opacity duration-300 flex items-center justify-center p-4">
        <div class="bg-nepal-cardBg border border-nepal-gold/40 w-full max-w-lg p-6 relative shadow-2xl">
            <button onclick="closeCustomTailoringModal()" class="absolute top-4 right-4 text-nepal-muted hover:text-nepal-gold">
                <i class="fa-solid fa-xmark text-lg"></i>
            </button>
            <h3 class="font-serif text-2xl text-white mb-2">Royal Bespoke Order</h3>
            <p class="text-xs text-nepal-muted mb-6">Submit custom measurements for handwoven Palpali Dhaka & Royal Velvet tailoring.</p>
            <form id="bespoke-form" class="space-y-4">
                <input type="text" required placeholder="Full Name" class="w-full bg-nepal-charcoal border border-white/20 p-3 text-xs text-white focus:outline-none focus:border-nepal-gold">
                <input type="email" required placeholder="Email Address" class="w-full bg-nepal-charcoal border border-white/20 p-3 text-xs text-white focus:outline-none focus:border-nepal-gold">
                <select class="w-full bg-nepal-charcoal border border-white/20 p-3 text-xs text-white focus:outline-none focus:border-nepal-gold">
                    <option>Palpali Dhaka Blazer</option>
                    <option>Royal Velvet Daura-Suruwal Suit</option>
                    <option>Mustang Pashmina Evening Gown</option>
                    <option>Custom Bridal / Groom Ensemble</option>
                </select>
                <textarea rows="3" placeholder="Specify size details or custom preferences..." class="w-full bg-nepal-charcoal border border-white/20 p-3 text-xs text-white focus:outline-none focus:border-nepal-gold"></textarea>
                <button type="submit" class="w-full py-3 bg-nepal-crimson border border-nepal-gold text-nepal-gold text-xs uppercase font-semibold tracking-widest hover:bg-nepal-gold hover:text-nepal-charcoal transition-all">
                    Submit Request
                </button>
            </form>
        </div>
    </div>

    <!-- Application Script -->
    <script>
        // --- PRODUCT DATA WITH DUAL CURRENCY (NPR & USD) ---
        const products = [
            {
                id: 1,
                name: "Royal Palpali Dhaka Blazer",
                category: "royal-men",
                priceNpr: 48500,
                priceUsd: 365,
                badge: "Handwoven",
                image: "https://images.unsplash.com/photo-1594938298603-c8148c4dae35?q=80&w=800&auto=format&fit=crop",
                description: "Handwoven geometric Palpali Dhaka fabric tailored into a crisp structured silhouette with custom Patan silver buttons."
            },
            {
                id: 2,
                name: "Mustang Cashmere Pashmina Wrap",
                category: "shawls",
                priceNpr: 32000,
                priceUsd: 240,
                badge: "100% Pashmina",
                image: "https://images.unsplash.com/photo-1584917865442-de89df76afd3?q=80&w=800&auto=format&fit=crop",
                description: "Featherlight high-altitude Himalayan cashmere wrap hand-dyed in deep crimson with royal gold zari trim."
            },
            {
                id: 3,
                name: "Crimson Velvet Gala Lehenga",
                category: "heritage-women",
                priceNpr: 95000,
                priceUsd: 715,
                badge: "Bestseller",
                image: "https://images.unsplash.com/photo-1566174053879-31528523f8ae?q=80&w=800&auto=format&fit=crop",
                description: "Royal velvet skirt embroidered with gold zardozi motifs and paired with a hand-loomed raw silk dupatta."
            },
            {
                id: 4,
                name: "Dhaka Pattern Tuxedo Jacket",
                category: "dhaka-fusion",
                priceNpr: 54000,
                priceUsd: 405,
                badge: "Limited Edition",
                image: "https://images.unsplash.com/photo-1507679799987-c73779587ccf?q=80&w=800&auto=format&fit=crop",
                description: "Modern black-tie tuxedo with handwoven Dhaka silk shawl lapels and tailored slim profile."
            },
            {
                id: 5,
                name: "Himalayan Velvet Bandgala",
                category: "royal-men",
                priceNpr: 42000,
                priceUsd: 315,
                badge: "New Arrival",
                image: "https://images.unsplash.com/photo-1539533018447-63fcce2678e3?q=80&w=800&auto=format&fit=crop",
                description: "Deep obsidian velvet court jacket with Mandarin collar and subtle Dhaka motif embroidery along cuffs."
            },
            {
                id: 6,
                name: "Raw Silk Sari with Dhaka Border",
                category: "heritage-women",
                priceNpr: 38000,
                priceUsd: 285,
                badge: "Handloom",
                image: "https://images.unsplash.com/photo-1515372039744-b8f02a3ae446?q=80&w=800&auto=format&fit=crop",
                description: "Pure ivory raw silk sari highlighted by an authentic red and gold Palpali Dhaka handloom border."
            },
            {
                id: 7,
                name: "Patan Silver Handcrafted Brooch",
                category: "dhaka-fusion",
                priceNpr: 18500,
                priceUsd: 140,
                badge: "Artisan Gem",
                image: "https://images.unsplash.com/photo-1599643478518-a784e5dc4c8f?q=80&w=800&auto=format&fit=crop",
                description: "Sterlin silver lapel pin featuring traditional Nepalese lotus filigree work plated in 18k gold."
            },
            {
                id: 8,
                name: "Heritage Dhaka Travel Duffle",
                category: "dhaka-fusion",
                priceNpr: 28000,
                priceUsd: 210,
                badge: "Bestseller",
                image: "https://images.unsplash.com/photo-1553062407-98eeb64c6a62?q=80&w=800&auto=format&fit=crop",
                description: "Full-grain calfskin weekend bag integrated with hand-loomed Tehrathum Dhaka side panels."
            }
        ];

        // --- APP STATE ---
        let cart = [];
        let wishlist = [];
        let activeFilter = 'all';

        // --- DOM REFERENCES ---
        const productGrid = document.getElementById('product-grid');
        const filterBtns = document.querySelectorAll('#filter-tabs button');
        const cartToggleBtn = document.getElementById('cart-toggle-btn');
        const cartCloseBtn = document.getElementById('cart-close-btn');
        const cartDrawer = document.getElementById('cart-drawer');
        const cartBackdrop = document.getElementById('cart-drawer-backdrop');
        const cartItemsContainer = document.getElementById('cart-items-container');
        const cartSubtotalEl = document.getElementById('cart-subtotal');
        const cartUsdSubtotalEl = document.getElementById('cart-usd-subtotal');
        const cartBadge = document.getElementById('cart-badge');
        const wishlistBadge = document.getElementById('wishlist-badge');
        
        const modalBackdrop = document.getElementById('modal-backdrop');
        const productModal = document.getElementById('product-modal');
        const modalContent = document.getElementById('modal-content');
        const modalCloseBtn = document.getElementById('modal-close-btn');

        const bespokeModalBackdrop = document.getElementById('bespoke-modal-backdrop');

        const searchToggleBtn = document.getElementById('search-toggle-btn');
        const searchBar = document.getElementById('search-bar');
        const searchCloseBtn = document.getElementById('search-close-btn');
        const searchInput = document.getElementById('search-input');

        const mobileMenuBtn = document.getElementById('mobile-menu-btn');
        const mobileMenu = document.getElementById('mobile-menu');

        // --- RENDER PRODUCTS ---
        function renderProducts(filter = 'all', query = '') {
            productGrid.innerHTML = '';

            const filtered = products.filter(p => {
                const matchesFilter = filter === 'all' || p.category === filter;
                const matchesSearch = p.name.toLowerCase().includes(query.toLowerCase()) ||
                                      p.description.toLowerCase().includes(query.toLowerCase());
                return matchesFilter && matchesSearch;
            });

            if (filtered.length === 0) {
                productGrid.innerHTML = `
                    <div class="col-span-full py-12 text-center text-nepal-muted">
                        <i class="fa-solid fa-magnifying-glass text-3xl mb-3 text-nepal-gold/40"></i>
                        <p class="text-sm">No Himalayan heritage pieces match your criteria.</p>
                    </div>
                `;
                return;
            }

            filtered.forEach(p => {
                const isWishlisted = wishlist.includes(p.id);
                const card = document.createElement('div');
                card.className = "bg-nepal-cardBg border border-white/5 hover:border-nepal-gold/40 transition-all duration-300 flex flex-col justify-between group relative overflow-hidden";
                card.innerHTML = `
                    <div>
                        <!-- Image Container -->
                        <div class="relative aspect-[3/4] overflow-hidden bg-nepal-charcoal">
                            <img src="${p.image}" alt="${p.name}" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-700">
                            
                            <!-- Badge -->
                            <span class="absolute top-3 left-3 bg-nepal-crimson/90 border border-nepal-gold/40 text-nepal-gold text-[9px] uppercase tracking-widest px-2 py-1 font-semibold">
                                ${p.badge}
                            </span>

                            <!-- Wishlist Toggle -->
                            <button onclick="toggleWishlist(${p.id})" class="absolute top-3 right-3 w-8 h-8 rounded-full bg-nepal-charcoal/80 border border-white/10 text-white hover:text-nepal-gold flex items-center justify-center transition-colors">
                                <i class="fa-${isWishlisted ? 'solid text-nepal-gold' : 'regular'} fa-heart"></i>
                            </button>

                            <!-- Quick Action Overlay -->
                            <div class="absolute bottom-3 left-3 right-3 flex gap-2 translate-y-4 opacity-0 group-hover:translate-y-0 group-hover:opacity-100 transition-all">
                                <button onclick="openModal(${p.id})" class="flex-1 py-2 bg-nepal-charcoal/90 border border-white/20 text-xs text-white hover:text-nepal-gold uppercase tracking-wider">
                                    Quick View
                                </button>
                                <button onclick="addToCart(${p.id})" class="py-2 px-3 bg-nepal-gold text-nepal-charcoal font-semibold hover:bg-nepal-goldLight">
                                    <i class="fa-solid fa-bag-shopping"></i>
                                </button>
                            </div>
                        </div>

                        <!-- Info -->
                        <div class="p-4 space-y-1">
                            <h3 class="font-serif text-sm text-white font-medium group-hover:text-nepal-gold transition-colors">${p.name}</h3>
                            <p class="text-[11px] text-nepal-muted line-clamp-2">${p.description}</p>
                        </div>
                    </div>

                    <div class="px-4 pb-4 pt-2 border-t border-white/5 flex items-center justify-between">
                        <div>
                            <span class="font-serif text-sm text-nepal-gold font-bold">NRs. ${p.priceNpr.toLocaleString()}</span>
                            <span class="block text-[10px] text-nepal-muted">$${p.priceUsd} USD</span>
                        </div>
                        <button onclick="addToCart(${p.id})" class="text-xs text-nepal-ivory hover:text-nepal-gold uppercase tracking-widest font-medium">
                            + Add Bag
                        </button>
                    </div>
                `;
                productGrid.appendChild(card);
            });
        }

        // --- FILTER TAB LISTENER ---
        filterBtns.forEach(btn => {
            btn.addEventListener('click', () => {
                filterBtns.forEach(b => {
                    b.classList.remove('active', 'bg-nepal-gold', 'text-nepal-charcoal', 'font-semibold');
                    b.classList.add('border-white/10', 'text-nepal-ivory');
                });
                btn.classList.add('active', 'bg-nepal-gold', 'text-nepal-charcoal', 'font-semibold');
                btn.classList.remove('border-white/10', 'text-nepal-ivory');

                activeFilter = btn.getAttribute('data-filter');
                renderProducts(activeFilter, searchInput.value);
            });
        });

        // --- WISHLIST LOGIC ---
        function toggleWishlist(productId) {
            const index = wishlist.indexOf(productId);
            if (index > -1) {
                wishlist.splice(index, 1);
                showToast("Item removed from your Wishlist.");
            } else {
                wishlist.push(productId);
                showToast("Added to your Wishlist.");
            }
            wishlistBadge.textContent = wishlist.length;
            wishlistBadge.style.opacity = wishlist.length > 0 ? '1' : '0';
            wishlistBadge.style.transform = wishlist.length > 0 ? 'scale(1)' : 'scale(0.5)';
            renderProducts(activeFilter, searchInput.value);
        }

        // --- CART LOGIC ---
        function addToCart(productId, selectedSize = 'M') {
            const product = products.find(p => p.id === productId);
            const existingIndex = cart.findIndex(item => item.id === productId && item.size === selectedSize);

            if (existingIndex > -1) {
                cart[existingIndex].quantity += 1;
            } else {
                cart.push({ ...product, size: selectedSize, quantity: 1 });
            }

            updateCartUI();
            showToast(`Added ${product.name} to your Royal Bag.`);
            openCart();
        }

        function removeFromCart(index) {
            const removed = cart[index];
            cart.splice(index, 1);
            updateCartUI();
            showToast(`Removed ${removed.name} from bag.`);
        }

        function updateQuantity(index, delta) {
            cart[index].quantity += delta;
            if (cart[index].quantity <= 0) cart.splice(index, 1);
            updateCartUI();
        }

        function updateCartUI() {
            cartItemsContainer.innerHTML = '';

            if (cart.length === 0) {
                cartItemsContainer.innerHTML = `
                    <div class="py-12 text-center text-nepal-muted">
                        <i class="fa-solid fa-bag-shopping text-4xl text-nepal-gold/20 mb-3"></i>
                        <p class="text-sm font-serif text-white">Your Royal Bag is empty.</p>
                        <p class="text-xs text-nepal-muted mt-1">Explore our Dhaka & Pashmina collection.</p>
                    </div>
                `;
            } else {
                cart.forEach((item, index) => {
                    const el = document.createElement('div');
                    el.className = "flex gap-3 pb-3 border-b border-white/5 items-center";
                    el.innerHTML = `
                        <img src="${item.image}" alt="${item.name}" class="w-16 h-20 object-cover border border-white/10">
                        <div class="flex-1 space-y-0.5">
                            <h4 class="font-serif text-xs text-white font-medium">${item.name}</h4>
                            <p class="text-[10px] text-nepal-muted">Size: <span class="text-white">${item.size}</span></p>
                            <p class="text-xs text-nepal-gold font-bold">NRs. ${item.priceNpr.toLocaleString()}</p>
                            
                            <div class="flex items-center space-x-2 pt-1">
                                <div class="flex items-center border border-white/20 bg-nepal-charcoal text-[10px]">
                                    <button onclick="updateQuantity(${index}, -1)" class="px-2 text-nepal-muted hover:text-white">-</button>
                                    <span class="px-2 text-white font-semibold">${item.quantity}</span>
                                    <button onclick="updateQuantity(${index}, 1)" class="px-2 text-nepal-muted hover:text-white">+</button>
                                </div>
                                <button onclick="removeFromCart(${index})" class="text-[10px] text-red-400 hover:underline">Remove</button>
                            </div>
                        </div>
                    `;
                    cartItemsContainer.appendChild(el);
                });
            }

            const totalNpr = cart.reduce((sum, item) => sum + (item.priceNpr * item.quantity), 0);
            const totalUsd = cart.reduce((sum, item) => sum + (item.priceUsd * item.quantity), 0);
            const totalItems = cart.reduce((sum, item) => sum + item.quantity, 0);

            cartSubtotalEl.textContent = `NRs. ${totalNpr.toLocaleString()}`;
            cartUsdSubtotalEl.textContent = `$${totalUsd.toLocaleString()} USD`;
            cartBadge.textContent = totalItems;
            
            cartBadge.style.opacity = totalItems > 0 ? '1' : '0';
            cartBadge.style.transform = totalItems > 0 ? 'scale(1)' : 'scale(0.5)';
        }

        function openCart() {
            cartDrawer.classList.remove('translate-x-full');
            cartBackdrop.classList.remove('opacity-0', 'pointer-events-none');
        }

        function closeCart() {
            cartDrawer.classList.add('translate-x-full');
            cartBackdrop.classList.add('opacity-0', 'pointer-events-none');
        }

        cartToggleBtn.addEventListener('click', openCart);
        cartCloseBtn.addEventListener('click', closeCart);
        cartBackdrop.addEventListener('click', closeCart);

        // --- QUICK VIEW MODAL ---
        function openModal(productId) {
            const product = products.find(p => p.id === productId);
            if (!product) return;

            modalContent.innerHTML = `
                <div class="aspect-[3/4] bg-nepal-charcoal relative overflow-hidden">
                    <img src="${product.image}" alt="${product.name}" class="w-full h-full object-cover">
                </div>
                <div class="p-6 flex flex-col justify-between space-y-4">
                    <div>
                        <span class="text-[9px] uppercase tracking-[0.2em] text-nepal-gold font-semibold">${product.badge}</span>
                        <h3 class="font-serif text-xl text-white mb-1">${product.name}</h3>
                        <p class="font-serif text-lg text-nepal-gold font-bold mb-3">NRs. ${product.priceNpr.toLocaleString()} <span class="text-xs text-nepal-muted font-sans">($${product.priceUsd} USD)</span></p>
                        <p class="text-xs text-nepal-ivory/80 leading-relaxed mb-4 border-y border-white/10 py-3 font-light">
                            ${product.description}
                        </p>

                        <!-- Size Options -->
                        <div class="space-y-1 mb-4">
                            <label class="block text-[10px] uppercase tracking-wider text-nepal-muted">Select Size</label>
                            <div class="flex gap-2">
                                <button onclick="selectModalSize(this)" class="modal-size-btn border border-nepal-gold bg-nepal-gold text-nepal-charcoal text-xs w-8 h-8 font-bold">S</button>
                                <button onclick="selectModalSize(this)" class="modal-size-btn border border-white/20 text-white text-xs w-8 h-8">M</button>
                                <button onclick="selectModalSize(this)" class="modal-size-btn border border-white/20 text-white text-xs w-8 h-8">L</button>
                                <button onclick="selectModalSize(this)" class="modal-size-btn border border-white/20 text-white text-xs w-8 h-8">XL</button>
                            </div>
                        </div>
                    </div>

                    <button onclick="addFromModal(${product.id})" class="w-full py-3 bg-nepal-gold text-nepal-charcoal text-xs font-semibold uppercase tracking-widest hover:bg-nepal-goldLight">
                        Add To Royal Bag
                    </button>
                </div>
            `;

            modalBackdrop.classList.remove('opacity-0', 'pointer-events-none');
            productModal.classList.remove('scale-95');
            productModal.classList.add('scale-100');
        }

        let selectedModalSize = 'S';
        function selectModalSize(btn) {
            document.querySelectorAll('.modal-size-btn').forEach(b => {
                b.classList.remove('bg-nepal-gold', 'text-nepal-charcoal', 'border-nepal-gold', 'font-bold');
                b.classList.add('border-white/20', 'text-white');
            });
            btn.classList.add('bg-nepal-gold', 'text-nepal-charcoal', 'border-nepal-gold', 'font-bold');
            selectedModalSize = btn.textContent;
        }

        function addFromModal(productId) {
            addToCart(productId, selectedModalSize);
            closeModal();
        }

        function closeModal() {
            modalBackdrop.classList.add('opacity-0', 'pointer-events-none');
            productModal.classList.remove('scale-100');
            productModal.classList.add('scale-95');
        }

        modalCloseBtn.addEventListener('click', closeModal);
        modalBackdrop.addEventListener('click', (e) => {
            if (e.target === modalBackdrop) closeModal();
        });

        // --- BESPOKE MODAL LOGIC ---
        function openCustomTailoringModal() {
            bespokeModalBackdrop.classList.remove('opacity-0', 'pointer-events-none');
        }

        function closeCustomTailoringModal() {
            bespokeModalBackdrop.classList.add('opacity-0', 'pointer-events-none');
        }

        document.getElementById('bespoke-form').addEventListener('submit', (e) => {
            e.preventDefault();
            showToast("Royal Fitting Request Received! Our Kathmandu concierge will contact you.");
            closeCustomTailoringModal();
        });

        // --- SEARCH TOGGLE ---
        searchToggleBtn.addEventListener('click', () => {
            searchBar.classList.toggle('hidden');
            if (!searchBar.classList.contains('hidden')) searchInput.focus();
        });

        searchCloseBtn.addEventListener('click', () => {
            searchBar.classList.add('hidden');
            searchInput.value = '';
            renderProducts(activeFilter, '');
        });

        searchInput.addEventListener('input', (e) => {
            renderProducts(activeFilter, e.target.value);
        });

        // --- MOBILE MENU ---
        mobileMenuBtn.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });

        // --- CHECKOUT ---
        document.getElementById('checkout-btn').addEventListener('click', () => {
            if (cart.length === 0) {
                showToast("Your bag is empty!");
                return;
            }
            showToast("Order initiated! Thank you for choosing Aaron Fancy Store.");
            cart = [];
            updateCartUI();
            closeCart();
        });

        // --- NEWSLETTER ---
        document.getElementById('newsletter-form').addEventListener('submit', (e) => {
            e.preventDefault();
            showToast("Welcome to the Royal Circle! Your 10% discount code is ROYAL10.");
            e.target.reset();
        });

        // --- TOAST NOTIFICATIONS ---
        function showToast(message) {
            const container = document.getElementById('toast-container');
            const toast = document.createElement('div');
            toast.className = "bg-nepal-cardBg border border-nepal-gold/50 text-nepal-ivory text-xs px-4 py-3 shadow-2xl flex items-center space-x-2 transition-all translate-y-4 opacity-0 pointer-events-auto";
            toast.innerHTML = `
                <i class="fa-solid fa-crown text-nepal-gold"></i>
                <span>${message}</span>
            `;
            container.appendChild(toast);

            setTimeout(() => {
                toast.classList.remove('translate-y-4', 'opacity-0');
            }, 10);

            setTimeout(() => {
                toast.classList.add('translate-y-4', 'opacity-0');
                setTimeout(() => toast.remove(), 300);
            }, 3500);
        }

        // --- INITIAL RENDER ---
        window.addEventListener('DOMContentLoaded', () => {
            renderProducts();
            updateCartUI();
        });
    </script>
</body>
</html>
```
