<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>LOCALBOX – Gói Trọn Hương Vị Việt | Hộp Quà Đặc Sản Địa Phương</title>
  <!-- Google Fonts & FontAwesome Icons -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700;800&family=Merriweather:ital,wght@0,300;0,400;0,700;1,300&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

  <style>
    /* ==========================================
       1. BRAND IDENTITY & COLOR PALETTE
       ========================================== */
    :root {
      --color-primary-green: #173F2A; /* Forest Green (60% background/headers) */
      --color-cream-bg: #F5F0E3;      /* Cream (Main Canvas) */
      --color-olive: #6D8146;         /* Olive Accent */
      --color-terracotta: #D99332;    /* Terracotta Gold/Action Buttons */
      --color-kraft-brown: #B99568;    /* Kraft Paper Brown */
      --color-text-dark: #2C3531;
      --color-text-light: #F5F0E3;
      --color-white: #FFFFFF;
      --color-border: #E0D8C3;
      --font-title: 'Merriweather', serif;
      --font-body: 'Montserrat', sans-serif;
      --radius-sm: 8px;
      --radius-md: 12px;
      --radius-lg: 20px;
      --shadow-soft: 0 10px 30px rgba(23, 63, 42, 0.08);
      --shadow-hover: 0 15px 35px rgba(23, 63, 42, 0.15);
      --transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: var(--font-body);
      background-color: var(--color-cream-bg);
      color: var(--color-text-dark);
      line-height: 1.6;
      overflow-x: hidden;
    }

    h1, h2, h3, h4 {
      font-family: var(--font-title);
      color: var(--color-primary-green);
      line-height: 1.3;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    ul {
      list-style: none;
    }

    img {
      max-width: 100%;
      height: auto;
      display: block;
    }

    /* Container Standard */
    .container {
      width: 90%;
      max-width: 1240px;
      margin: 0 auto;
      padding: 0 15px;
    }

    /* Buttons */
    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 10px;
      padding: 12px 28px;
      font-size: 0.95rem;
      font-weight: 600;
      border-radius: var(--radius-sm);
      cursor: pointer;
      transition: var(--transition);
      border: none;
    }

    .btn-primary {
      background-color: var(--color-terracotta);
      color: var(--color-white);
    }
    .btn-primary:hover {
      background-color: #c07d24;
      transform: translateY(-2px);
      box-shadow: 0 5px 15px rgba(217, 147, 50, 0.3);
    }

    .btn-secondary {
      background-color: var(--color-primary-green);
      color: var(--color-cream-bg);
    }
    .btn-secondary:hover {
      background-color: #0f2b1d;
      transform: translateY(-2px);
    }

    .btn-outline {
      border: 2px solid var(--color-primary-green);
      color: var(--color-primary-green);
      background: transparent;
    }
    .btn-outline:hover {
      background-color: var(--color-primary-green);
      color: var(--color-cream-bg);
    }

    /* Section Typography */
    .section-title {
      font-size: 2.2rem;
      text-align: center;
      margin-bottom: 12px;
      position: relative;
    }
    .section-subtitle {
      text-align: center;
      color: #555;
      max-width: 650px;
      margin: 0 auto 40px auto;
      font-size: 1rem;
    }

    /* Header Nav */
    header {
      position: sticky;
      top: 0;
      background-color: rgba(245, 240, 227, 0.95);
      backdrop-filter: blur(10px);
      z-index: 1000;
      border-bottom: 1px solid var(--color-border);
      padding: 15px 0;
    }
    .nav-wrapper {
      display: flex;
      align-items: center;
      justify-content: space-between;
    }
    .logo-brand {
      display: flex;
      align-items: center;
      gap: 12px;
    }
    .logo-brand img {
      width: 52px;
      height: 52px;
      border-radius: 50%;
      object-fit: cover;
    }
    .logo-brand-text {
      font-family: var(--font-title);
      font-weight: 800;
      font-size: 1.4rem;
      color: var(--color-primary-green);
      letter-spacing: 0.5px;
    }
    .logo-brand-text span {
      display: block;
      font-family: var(--font-body);
      font-size: 0.7rem;
      font-weight: 500;
      color: var(--color-terracotta);
      letter-spacing: 1px;
    }

    .nav-menu {
      display: flex;
      gap: 25px;
      align-items: center;
    }
    .nav-link {
      font-weight: 600;
      font-size: 0.9rem;
      color: var(--color-text-dark);
      padding: 6px 0;
      position: relative;
      transition: var(--transition);
    }
    .nav-link:hover, .nav-link.active {
      color: var(--color-terracotta);
    }
    .nav-link.active::after {
      content: '';
      position: absolute;
      bottom: 0;
      left: 0;
      width: 100%;
      height: 2px;
      background-color: var(--color-terracotta);
    }

    .nav-actions {
      display: flex;
      align-items: center;
      gap: 15px;
    }
    .cart-btn {
      position: relative;
      background: var(--color-white);
      border: 1px solid var(--color-border);
      width: 42px;
      height: 42px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      color: var(--color-primary-green);
      font-size: 1.1rem;
      cursor: pointer;
    }
    .cart-badge {
      position: absolute;
      top: -5px;
      right: -5px;
      background-color: var(--color-terracotta);
      color: white;
      font-size: 0.7rem;
      font-weight: 700;
      width: 18px;
      height: 18px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    /* Mobile Hamburger */
    .mobile-toggle {
      display: none;
      font-size: 1.5rem;
      color: var(--color-primary-green);
      cursor: pointer;
    }

    /* SPA Page Visibility Switcher */
    .page-section {
      display: none;
      padding: 50px 0;
      animation: fadeIn 0.4s ease-in-out;
    }
    .page-section.active-page {
      display: block;
    }
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(10px); }
      to { opacity: 1; transform: translateY(0); }
    }

    /* Hero Banner */
    .hero {
      background-color: var(--color-primary-green);
      color: var(--color-cream-bg);
      padding: 70px 0;
      border-radius: var(--radius-lg);
      margin-top: 15px;
      position: relative;
      overflow: hidden;
    }
    .hero-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 40px;
      align-items: center;
    }
    .hero-content h1 {
      color: var(--color-cream-bg);
      font-size: 2.8rem;
      margin-bottom: 15px;
    }
    .hero-content p {
      font-size: 1.1rem;
      margin-bottom: 30px;
      color: rgba(245, 240, 227, 0.85);
    }
    .hero-buttons {
      display: flex;
      gap: 15px;
      flex-wrap: wrap;
    }
    .hero-img-box {
      position: relative;
      border-radius: var(--radius-md);
      overflow: hidden;
      box-shadow: 0 20px 40px rgba(0,0,0,0.3);
      border: 4px solid var(--color-kraft-brown);
    }
    .hero-img-box img {
      width: 100%;
      height: 380px;
      object-fit: cover;
      transition: var(--transition);
    }
    .hero-img-box:hover img {
      transform: scale(1.03);
    }

    /* Cards Grid */
    .grid-3 {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
      gap: 30px;
    }
    .grid-4 {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 25px;
    }

    /* Product Card */
    .product-card {
      background-color: var(--color-white);
      border-radius: var(--radius-md);
      overflow: hidden;
      border: 1px solid var(--color-border);
      box-shadow: var(--shadow-soft);
      transition: var(--transition);
      display: flex;
      flex-direction: column;
      position: relative;
    }
    .product-card:hover {
      transform: translateY(-5px);
      box-shadow: var(--shadow-hover);
    }
    .product-badge {
      position: absolute;
      top: 15px;
      left: 15px;
      background-color: var(--color-olive);
      color: white;
      font-size: 0.75rem;
      font-weight: 700;
      padding: 4px 10px;
      border-radius: 20px;
      z-index: 2;
    }
    .product-img {
      height: 220px;
      width: 100%;
      object-fit: cover;
      background-color: #f0ebd9;
    }
    .product-body {
      padding: 20px;
      display: flex;
      flex-direction: column;
      flex-grow: 1;
    }
    .product-title {
      font-size: 1.2rem;
      margin-bottom: 8px;
    }
    .product-price {
      font-weight: 700;
      color: var(--color-terracotta);
      font-size: 1.15rem;
      margin-bottom: 12px;
    }
    .product-desc {
      font-size: 0.88rem;
      color: #666;
      margin-bottom: 15px;
      flex-grow: 1;
    }
    .product-items {
      font-size: 0.8rem;
      background-color: var(--color-cream-bg);
      padding: 10px;
      border-radius: var(--radius-sm);
      margin-bottom: 15px;
      color: var(--color-primary-green);
    }
    .product-actions {
      display: flex;
      gap: 10px;
    }

    /* Tab Switcher on Page 3 */
    .tab-navigation {
      display: flex;
      justify-content: center;
      gap: 15px;
      margin-bottom: 35px;
      flex-wrap: wrap;
    }
    .tab-btn {
      padding: 12px 24px;
      background-color: var(--color-white);
      border: 1px solid var(--color-border);
      border-radius: 30px;
      font-weight: 600;
      font-size: 0.95rem;
      color: var(--color-primary-green);
      cursor: pointer;
      transition: var(--transition);
    }
    .tab-btn.active, .tab-btn:hover {
      background-color: var(--color-primary-green);
      color: var(--color-cream-bg);
      border-color: var(--color-primary-green);
    }

    /* Page 4: Builder Layout */
    .builder-grid {
      display: grid;
      grid-template-columns: 1.6fr 1fr;
      gap: 30px;
      align-items: start;
    }
    .builder-box {
      background: var(--color-white);
      padding: 25px;
      border-radius: var(--radius-md);
      border: 1px solid var(--color-border);
      margin-bottom: 25px;
    }
    .builder-step-title {
      font-size: 1.1rem;
      margin-bottom: 15px;
      display: flex;
      align-items: center;
      gap: 10px;
      color: var(--color-primary-green);
    }
    .builder-step-title i {
      color: var(--color-terracotta);
    }

    .item-select-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
      gap: 15px;
    }
    .item-select-card {
      border: 1px solid var(--color-border);
      border-radius: var(--radius-sm);
      padding: 10px;
      text-align: center;
      cursor: pointer;
      transition: var(--transition);
    }
    .item-select-card:hover, .item-select-card.selected {
      border-color: var(--color-terracotta);
      background-color: rgba(217, 147, 50, 0.05);
    }
    .item-select-card img {
      height: 90px;
      object-fit: cover;
      margin: 0 auto 8px auto;
      border-radius: 4px;
    }
    .item-select-card h5 {
      font-size: 0.85rem;
      margin-bottom: 4px;
    }
    .item-select-card .price {
      font-size: 0.8rem;
      font-weight: 700;
      color: var(--color-terracotta);
    }

    .builder-summary {
      background-color: var(--color-primary-green);
      color: var(--color-cream-bg);
      padding: 25px;
      border-radius: var(--radius-md);
      position: sticky;
      top: 90px;
    }
    .builder-summary h3 {
      color: var(--color-cream-bg);
      border-bottom: 1px solid rgba(245, 240, 227, 0.2);
      padding-bottom: 12px;
      margin-bottom: 20px;
    }
    .selected-list {
      margin-bottom: 20px;
      max-height: 250px;
      overflow-y: auto;
    }
    .selected-item-row {
      display: flex;
      justify-content: space-between;
      font-size: 0.85rem;
      margin-bottom: 8px;
      padding-bottom: 8px;
      border-bottom: 1px stroke rgba(255,255,255,0.1);
    }

    /* Modal Styling */
    .modal-overlay {
      position: fixed;
      top: 0; left: 0; right: 0; bottom: 0;
      background: rgba(0,0,0,0.6);
      display: none;
      justify-content: center;
      align-items: center;
      z-index: 2000;
      padding: 20px;
    }
    .modal-card {
      background: var(--color-white);
      max-width: 600px;
      width: 100%;
      border-radius: var(--radius-md);
      padding: 30px;
      position: relative;
      max-height: 90vh;
      overflow-y: auto;
    }
    .modal-close {
      position: absolute;
      top: 15px; right: 20px;
      font-size: 1.5rem;
      cursor: pointer;
      color: #888;
    }

    /* Footer */
    footer {
      background-color: var(--color-primary-green);
      color: var(--color-cream-bg);
      padding: 60px 0 20px 0;
      margin-top: 60px;
      border-top: 4px solid var(--color-kraft-brown);
    }
    .footer-grid {
      display: grid;
      grid-template-columns: 1.5fr 1fr 1fr 1fr;
      gap: 30px;
      margin-bottom: 40px;
    }
    .footer-col h4 {
      color: var(--color-terracotta);
      font-size: 1.1rem;
      margin-bottom: 18px;
    }
    .footer-col ul li {
      margin-bottom: 10px;
    }
    .footer-col ul li a {
      color: rgba(245, 240, 227, 0.8);
      font-size: 0.9rem;
      transition: var(--transition);
    }
    .footer-col ul li a:hover {
      color: var(--color-terracotta);
      padding-left: 5px;
    }
    .footer-bottom {
      border-top: 1px solid rgba(245, 240, 227, 0.15);
      padding-top: 20px;
      text-align: center;
      font-size: 0.85rem;
      color: rgba(245, 240, 227, 0.6);
    }

    /* Form Fields */
    .form-group {
      margin-bottom: 18px;
    }
    .form-group label {
      display: block;
      font-weight: 600;
      font-size: 0.88rem;
      margin-bottom: 6px;
    }
    .form-control {
      width: 100%;
      padding: 12px;
      border: 1px solid var(--color-border);
      border-radius: var(--radius-sm);
      font-family: inherit;
      font-size: 0.95rem;
      background-color: #fcfbfa;
    }
    .form-control:focus {
      outline: none;
      border-color: var(--color-primary-green);
      background-color: #fff;
    }

    /* Responsive */
    @media (max-width: 992px) {
      .hero-grid, .builder-grid, .footer-grid {
        grid-template-columns: 1fr;
      }
      .nav-menu {
        display: none;
      }
      .mobile-toggle {
        display: block;
      }
    }
  </style>
</head>
<body>

  <!-- ==========================================
       HEADER & NAVIGATION
       ========================================== -->
  <header>
    <div class="container nav-wrapper">
      <a href="#" onclick="switchPage('home')" class="logo-brand">
        <!-- Logo thương hiệu đã upload -->
        <img src="logo.png" alt="LOCALBOX Logo" onerror="this.src='https://placehold.co/100x100/173F2A/F5F0E3?text=LOCALBOX'">
        <div class="logo-brand-text">
          LOCALBOX
          <span>GÓI TRỌN HƯƠNG VỊ VIỆT</span>
        </div>
      </a>

      <nav class="nav-menu" id="navMenu">
        <a href="#" class="nav-link active" onclick="switchPage('home')">Trang chủ</a>
        <a href="#" class="nav-link" onclick="switchPage('about')">Giới thiệu</a>
        <a href="#" class="nav-link" onclick="switchPage('products')">Hộp quà</a>
        <a href="#" class="nav-link" onclick="switchPage('builder')">Tự chọn hộp</a>
        <a href="#" class="nav-link" onclick="switchPage('b2b')">Doanh nghiệp</a>
        <a href="#" class="nav-link" onclick="switchPage('ordering')">Đặt hàng</a>
        <a href="#" class="nav-link" onclick="switchPage('contact')">Liên hệ</a>
      </nav>

      <div class="nav-actions">
        <div class="cart-btn" onclick="openCartModal()">
          <i class="fa-solid fa-bag-shopping"></i>
          <span class="cart-badge" id="cartCount">0</span>
        </div>
        <button class="btn btn-primary" onclick="switchPage('builder')">Tạo Hộp Quà</button>
        <div class="mobile-toggle" onclick="toggleMobileNav()">
          <i class="fa-solid fa-bars"></i>
        </div>
      </div>
    </div>
  </header>

  <main class="container">

    <!-- ==========================================
         TRANG 1: TRANG CHỦ (HOME)
         ========================================== -->
    <section id="page-home" class="page-section active-page">
      <!-- Hero Banner -->
      <div class="hero">
        <div class="container hero-grid">
          <div class="hero-content">
            <h1>Gói Trọn Một Việt Nam Trong Chiếc Hộp Quà</h1>
            <p>Tuyển chọn những sản vật địa phương tinh túy nhất từ mọi miền Tổ quốc. Thiết kế hiện đại, bao bì tối ưu di chuyển cho khách du lịch và người tiêu dùng trẻ.</p>
            <div class="hero-buttons">
              <button class="btn btn-primary" onclick="switchPage('products')"><i class="fa-solid fa-gift"></i> Khám phá hộp quà</button>
              <button class="btn btn-outline" style="color:var(--color-cream-bg); border-color:var(--color-cream-bg);" onclick="switchPage('builder')"><i class="fa-solid fa-sliders"></i> Tự chọn hộp quà</button>
            </div>
          </div>
          <div class="hero-img-box">
            <!-- Ảnh sản phẩm chụp thật từ nhóm -->
            <img src="sản phẩm.png" alt="LocalBox Sản Phẩm Thực Tế" onerror="this.src='https://placehold.co/600x400/173F2A/F5F0E3?text=LocalBox+Product'">
          </div>
        </div>
      </div>

      <!-- Giới thiệu ngắn & 4 Lý do chọn LocalBox -->
      <div style="margin-top: 60px;">
        <h2 class="section-title">Tại Sao Chọn LocalBox?</h2>
        <p class="section-subtitle">LocalBox giải quyết khó khăn trong việc chọn đặc sản làm quà cồng kềnh, thiếu liên kết hay lo lắng chất lượng bằng giải pháp trọn gói hiện đại.</p>

        <div class="grid-4">
          <div class="product-card" style="padding: 25px; text-align: center;">
            <i class="fa-solid fa-certificate" style="font-size: 2.5rem; color: var(--color-terracotta); margin-bottom: 15px;"></i>
            <h3>Tuyển Chọn OCOP</h3>
            <p style="font-size: 0.88rem; color: #666; margin-top: 8px;">100% đặc sản địa phương minh bạch nguồn gốc, đạt chuẩn OCOP và vệ sinh an toàn thực phẩm.</p>
          </div>
          <div class="product-card" style="padding: 25px; text-align: center;">
            <i class="fa-solid fa-plane-departure" style="font-size: 2.5rem; color: var(--color-terracotta); margin-bottom: 15px;"></i>
            <h3>Chuẩn Khí Khẩu</h3>
            <p style="font-size: 0.88rem; color: #666; margin-top: 8px;">Kích thước hộp chuẩn tối ưu xách tay hoặc ký gửi máy bay, không lo va đập móp móp.</p>
          </div>
          <div class="product-card" style="padding: 25px; text-align: center;">
            <i class="fa-solid fa-book-open-reader" style="font-size: 2.5rem; color: var(--color-terracotta); margin-bottom: 15px;"></i>
            <h3>Kể Chuyện Văn Hóa</h3>
            <p style="font-size: 0.88rem; color: #666; margin-top: 8px;">Mỗi hộp quà đều kèm postcard hoặc mã QR thông minh dẫn lối câu chuyện làng nghề truyền thống.</p>
          </div>
          <div class="product-card" style="padding: 25px; text-align: center;">
            <i class="fa-solid fa-wand-magic-sparkles" style="font-size: 2.5rem; color: var(--color-terracotta); margin-bottom: 15px;"></i>
            <h3>Cá Nhân Hóa</h3>
            <p style="font-size: 0.88rem; color: #666; margin-top: 8px;">Linh hoạt mix-and-match sản phẩm, viết thiệp chúc mừng hoặc in ấn thương hiệu riêng.</p>
          </div>
        </div>
      </div>

      <!-- Phân khúc giá tham chiếu -->
      <div style="margin-top: 60px;">
        <h2 class="section-title">Các Phân Khúc Hộp Quà Dự Kiến</h2>
        <p class="section-subtitle">Đa dạng ngân sách phục vụ du khách, học sinh sinh viên đến doanh nghiệp biếu tặng.</p>

        <div class="grid-3">
          <div class="product-card">
            <span class="product-badge">Phổ Thông</span>
            <img src="sản phẩm.png" class="product-img" alt="Hộp Phổ Thông">
            <div class="product-body">
              <h3 class="product-title">Dòng Phổ Thông</h3>
              <div class="product-price">150.000đ – 250.000đ</div>
              <p class="product-desc">Phù hợp làm quà nhỏ, du khách trẻ, học sinh sinh viên mua trải nghiệm đặc sản nhanh gọn.</p>
              <button class="btn btn-outline" onclick="switchPage('products')">Xem hộp quà</button>
            </div>
          </div>

          <div class="product-card" style="border: 2px solid var(--color-terracotta);">
            <span class="product-badge" style="background-color: var(--color-terracotta);">Bán Chạy Nhất</span>
            <img src="sản phẩm.png" class="product-img" alt="Hộp Tiêu Chuẩn">
            <div class="product-body">
              <h3 class="product-title">Dòng Tiêu Chuẩn</h3>
              <div class="product-price">300.000đ – 450.000đ</div>
              <p class="product-desc">Set quà phổ biến nhất gồm Cà phê Buôn Ma Thuột, Mật ong hoa cà phê, Xoài sấy dẻo và Bánh cốm Hà Nội.</p>
              <button class="btn btn-primary" onclick="switchPage('products')">Xem hộp quà</button>
            </div>
          </div>

          <div class="product-card">
            <span class="product-badge" style="background-color: var(--color-primary-green);">Cao Cấp</span>
            <img src="sản phẩm.png" class="product-img" alt="Hộp Cao Cấp">
            <div class="product-body">
              <h3 class="product-title">Dòng Cao Cấp</h3>
              <div class="product-price">500.000đ – 700.000đ</div>
              <p class="product-desc">Set quà biếu sang trọng kết hợp đặc sản OCOP chọn lọc và ly gốm lưu niệm độc bản.</p>
              <button class="btn btn-outline" onclick="switchPage('products')">Xem hộp quà</button>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- ==========================================
         TRANG 2: GIỚI THIỆU (ABOUT US)
         ========================================== -->
    <section id="page-about" class="page-section">
      <h2 class="section-title">Về Chúng Tôi – LocalBox</h2>
      <p class="section-subtitle">Dự án khởi nghiệp của Nhóm 9 - Lớp DHTMDT20C, Khoa QTKD, Trường Đại học Công nghiệp TP. Hồ Chí Minh (IUH).</p>

      <div class="builder-box">
        <h3 style="margin-bottom: 15px;">Ý Nghĩa Thương Hiệu</h3>
        <p><strong>LOCAL (Bản địa):</strong> Ký ức chắt chiu qua những thửa ruộng bậc thang, bàn tay người nghệ nhân gìn giữ làng nghề. Hồn cốt văn hóa Việt được giữ trọn vẹn.</p>
        <p style="margin-top: 10px;"><strong>BOX (Chiếc hộp):</strong> Cầu nối giữa giá trị truyền thống xưa và tư duy thẩm mỹ hiện đại. Hộp đóng gói tinh tế, nhỏ gọn, chuẩn tối ưu cho khách mang theo khi di chuyển hoặc đi máy bay.</p>
      </div>

      <div class="builder-box">
        <h3 style="margin-bottom: 20px;">Đội Ngũ Sáng Lập (Nhóm 9 - IUH)</h3>
        <div class="grid-4">
          <div style="text-align: center; padding: 15px; border: 1px solid var(--color-border); border-radius: var(--radius-sm);">
            <i class="fa-solid fa-user-gear" style="font-size: 2rem; color: var(--color-primary-green);"></i>
            <h4 style="margin-top: 10px; font-size: 1rem;">Nguyễn Thị Như Ngọc</h4>
            <p style="font-size: 0.8rem; color: var(--color-terracotta);">Quản lý LocalBox</p>
          </div>
          <div style="text-align: center; padding: 15px; border: 1px solid var(--color-border); border-radius: var(--radius-sm);">
            <i class="fa-solid fa-bullhorn" style="font-size: 2rem; color: var(--color-primary-green);"></i>
            <h4 style="margin-top: 10px; font-size: 1rem;">Lê Thị Ngọc Ánh</h4>
            <p style="font-size: 0.8rem; color: var(--color-terracotta);">Marketing & Content</p>
          </div>
          <div style="text-align: center; padding: 15px; border: 1px solid var(--color-border); border-radius: var(--radius-sm);">
            <i class="fa-solid fa-store" style="font-size: 2rem; color: var(--color-primary-green);"></i>
            <h4 style="margin-top: 10px; font-size: 1rem;">Nguyễn Ngọc Bảo Trâm</h4>
            <p style="font-size: 0.8rem; color: var(--color-terracotta);">Bán hàng</p>
          </div>
          <div style="text-align: center; padding: 15px; border: 1px solid var(--color-border); border-radius: var(--radius-sm);">
            <i class="fa-solid fa-boxes-packing" style="font-size: 2rem; color: var(--color-primary-green);"></i>
            <h4 style="margin-top: 10px; font-size: 1rem;">Giáp Thị Hằng</h4>
            <p style="font-size: 0.8rem; color: var(--color-terracotta);">Kho - Vận hành</p>
          </div>
          <div style="text-align: center; padding: 15px; border: 1px solid var(--color-border); border-radius: var(--radius-sm);">
            <i class="fa-solid fa-box-open" style="font-size: 2rem; color: var(--color-primary-green);"></i>
            <h4 style="margin-top: 10px; font-size: 1rem;">Ngô Kim Anh</h4>
            <p style="font-size: 0.8rem; color: var(--color-terracotta);">Đóng gói</p>
          </div>
          <div style="text-align: center; padding: 15px; border: 1px solid var(--color-border); border-radius: var(--radius-sm);">
            <i class="fa-solid fa-headset" style="font-size: 2rem; color: var(--color-primary-green);"></i>
            <h4 style="margin-top: 10px; font-size: 1rem;">Trần Duy Hưng Thịnh</h4>
            <p style="font-size: 0.8rem; color: var(--color-terracotta);">CSKH & Xử lý sự cố</p>
          </div>
          <div style="text-align: center; padding: 15px; border: 1px solid var(--color-border); border-radius: var(--radius-sm);">
            <i class="fa-solid fa-calculator" style="font-size: 2rem; color: var(--color-primary-green);"></i>
            <h4 style="margin-top: 10px; font-size: 1rem;">Lê Quỳnh Trân</h4>
            <p style="font-size: 0.8rem; color: var(--color-terracotta);">Tài chính - Kế toán</p>
          </div>
          <div style="text-align: center; padding: 15px; border: 1px solid var(--color-border); border-radius: var(--radius-sm);">
            <i class="fa-solid fa-users" style="font-size: 2rem; color: var(--color-primary-green);"></i>
            <h4 style="margin-top: 10px; font-size: 1rem;">Võ Thị Thu Thảo</h4>
            <p style="font-size: 0.8rem; color: var(--color-terracotta);">Nhân sự - Hành chính</p>
          </div>
        </div>
      </div>
    </section>

    <!-- ==========================================
         TRANG 3: HỘP QUÀ LOCALBOX (CÓ 4 TAB HOẠT ĐỘNG)
         ========================================== -->
    <section id="page-products" class="page-section">
      <h2 class="section-title">Danh Mục Hộp Quà LocalBox</h2>
      <p class="section-subtitle">Khám phá các bộ quà tặng đặc sản địa phương được phối sẵn tinh tế theo nhiều góc độ lựa chọn.</p>

      <!-- 4 TAB ĐIỀU HƯỚNG TRỌNG TÂM -->
      <div class="tab-navigation">
        <button class="tab-btn active" onclick="switchProductTab('sample')">Hộp Mẫu Phối Sẵn</button>
        <button class="tab-btn" onclick="switchProductTab('region')">Theo Vùng Miền</button>
        <button class="tab-btn" onclick="switchProductTab('occasion')">Theo Dịp Tặng</button>
        <button class="tab-btn" onclick="switchProductTab('budget')">Theo Mức Giá</button>
      </div>

      <!-- TAB 1: HỘP MẪU -->
      <div id="tab-content-sample" class="tab-content-item">
        <div class="grid-3" id="sample-products-container">
          <!-- Rendered by JS -->
        </div>
      </div>

      <!-- TAB 2: THEO VÙNG -->
      <div id="tab-content-region" class="tab-content-item" style="display:none;">
        <div style="margin-bottom: 25px; text-align: center;">
          <button class="btn btn-outline" onclick="filterByRegion('all')">Tất cả</button>
          <button class="btn btn-outline" onclick="filterByRegion('Tây Bắc')">Tây Bắc</button>
          <button class="btn btn-outline" onclick="filterByRegion('Tây Nguyên')">Tây Nguyên</button>
          <button class="btn btn-outline" onclick="filterByRegion('Miền Tây')">Miền Tây</button>
          <button class="btn btn-outline" onclick="filterByRegion('Hà Nội')">Hà Nội</button>
        </div>
        <div class="grid-3" id="region-products-container">
          <!-- Rendered by JS -->
        </div>
      </div>

      <!-- TAB 3: THEO DỊP -->
      <div id="tab-content-occasion" class="tab-content-item" style="display:none;">
        <div style="margin-bottom: 25px; text-align: center;">
          <button class="btn btn-outline" onclick="filterByOccasion('all')">Tất cả dịp</button>
          <button class="btn btn-outline" onclick="filterByOccasion('Du lịch')">Du lịch</button>
          <button class="btn btn-outline" onclick="filterByOccasion('Lễ Tết')">Quà Lễ Tết</button>
          <button class="btn btn-outline" onclick="filterByOccasion('Doanh nghiệp')">Doanh nghiệp</button>
        </div>
        <div class="grid-3" id="occasion-products-container">
          <!-- Rendered by JS -->
        </div>
      </div>

      <!-- TAB 4: THEO MỨC GIÁ -->
      <div id="tab-content-budget" class="tab-content-item" style="display:none;">
        <div style="margin-bottom: 25px; text-align: center;">
          <button class="btn btn-outline" onclick="filterByBudget('all')">Tất cả khoảng giá</button>
          <button class="btn btn-outline" onclick="filterByBudget('low')">Phổ thông (< 250k)</button>
          <button class="btn btn-outline" onclick="filterByBudget('mid')">Tiêu chuẩn (300k - 450k)</button>
          <button class="btn btn-outline" onclick="filterByBudget('high')">Cao cấp (> 500k)</button>
        </div>
        <div class="grid-3" id="budget-products-container">
          <!-- Rendered by JS -->
        </div>
      </div>
    </section>

    <!-- ==========================================
         TRANG 4: TỰ CHỌN HỘP (MIX-AND-MATCH BUILDER)
         ========================================== -->
    <section id="page-builder" class="page-section">
      <h2 class="section-title">Tự Thiết Kế Hộp Quà LocalBox</h2>
      <p class="section-subtitle">Tự do phối kết hợp các món đặc sản địa phương yêu thích thành hộp quà mang dấu ấn cá nhân.</p>

      <div class="builder-grid">
        <!-- Cột Trái: Các bước chọn -->
        <div>
          <!-- Bước 1: Chọn ngân sách dự kiến -->
          <div class="builder-box">
            <div class="builder-step-title"><i class="fa-solid fa-circle-1"></i> Chọn Mức Ngân Sách Định Hướng</div>
            <div style="display: flex; gap: 15px; flex-wrap: wrap;">
              <label><input type="radio" name="builderBudget" value="250000" checked onchange="updateBuilderSummary()"> Phổ thông (~250k)</label>
              <label><input type="radio" name="builderBudget" value="350000" onchange="updateBuilderSummary()"> Tiêu chuẩn (~350k)</label>
              <label><input type="radio" name="builderBudget" value="600000" onchange="updateBuilderSummary()"> Cao cấp (~600k)</label>
            </div>
          </div>

          <!-- Bước 2: Chọn đặc sản -->
          <div class="builder-box">
            <div class="builder-step-title"><i class="fa-solid fa-circle-2"></i> Chọn Các Món Đặc Sản Đưa Vào Hộp</div>
            <div class="item-select-grid" id="builder-items-options">
              <!-- Rendered via JS -->
            </div>
          </div>

          <!-- Bước 3 & 4: Dịp & Lời chúc -->
          <div class="builder-box">
            <div class="builder-step-title"><i class="fa-solid fa-circle-3"></i> Thông Tin Lời Chúc & Dịp Tặng</div>
            <div class="form-group">
              <label>Dịp tặng quà:</label>
              <select class="form-control" id="builderOccasionSelect">
                <option value="Quà Du Lịch">Quà Du Lịch Kỷ Niệm</option>
                <option value="Quà Sinh Nhật">Mừng Sinh Nhật</option>
                <option value="Quà Lễ Tết">Quà Biếu Lễ Tết</option>
                <option value="Quà Tri Ân">Tri Ân Đối Tác / Bạn Bè</option>
              </select>
            </div>
            <div class="form-group">
              <label>Lời chúc in trên thiệp Storytelling LocalBox:</label>
              <textarea class="form-control" id="builderCardMessage" rows="3" placeholder="Nhập lời nhắn cá nhân của bạn..."></textarea>
            </div>
          </div>
        </div>

        <!-- Cột Phải: Bảng Tóm Tắt Realtime -->
        <div class="builder-summary">
          <h3>Tóm Tắt Hộp Quà Của Bạn</h3>
          <div class="selected-list" id="builderSelectedList">
            <p style="font-size:0.85rem; opacity:0.7;">Chưa chọn món nào...</p>
          </div>

          <div style="border-top: 1px solid rgba(255,255,255,0.2); padding-top: 15px; margin-top: 15px;">
            <div style="display: flex; justify-content: space-between; margin-bottom: 8px;">
              <span>Tiền sản phẩm:</span>
              <strong id="builderItemsPrice">0đ</strong>
            </div>
            <div style="display: flex; justify-content: space-between; margin-bottom: 8px;">
              <span>Phí vỏ hộp & phụ kiện:</span>
              <strong>42.000đ</strong>
            </div>
            <div style="display: flex; justify-content: space-between; font-size: 1.2rem; color: var(--color-terracotta); margin-top: 12px; border-top: 1px dashed rgba(255,255,255,0.3); padding-top: 10px;">
              <span>Tổng chi phí:</span>
              <strong id="builderTotalPrice">42.000đ</strong>
            </div>
          </div>

          <button class="btn btn-primary" style="width: 100%; margin-top: 20px;" onclick="addCustomBoxToCart()">
            <i class="fa-solid fa-cart-plus"></i> Thêm Hộp Này Vào Giỏ
          </button>
        </div>
      </div>
    </section>

    <!-- ==========================================
         TRANG 5: DOANH NGHIỆP (B2B SOLUTIONS)
         ========================================== -->
    <section id="page-b2b" class="page-section">
      <h2 class="section-title">Giải Pháp Quà Tặng Doanh Nghiệp (B2B)</h2>
      <p class="section-subtitle">LocalBox cung cấp giải pháp quà đối ngoại, quà tri ân đối tác và quà Tết nhân viên số lượng lớn từ 50 hộp trở lên.</p>

      <div class="builder-grid">
        <div>
          <div class="builder-box">
            <h3>Năng Lực Cung Ứng & Cá Nhân Hóa B2B</h3>
            <ul style="margin-top: 15px; font-size: 0.95rem; line-height: 1.8;">
              <li><i class="fa-solid fa-check" style="color:var(--color-terracotta);"></i> <strong>In ấn Logo thương hiệu:</strong> Ép kim, khắc logo công ty trực tiếp lên vỏ hộp quà sang trọng.</li>
              <li><i class="fa-solid fa-check" style="color:var(--color-terracotta);"></i> <strong>Tùy chỉnh bao bì:</strong> Lựa chọn tông màu và thông điệp thương hiệu riêng cho doanh nghiệp.</li>
              <li><i class="fa-solid fa-check" style="color:var(--color-terracotta);"></i> <strong>Thiệp chúc riêng:</strong> Thiết kế thư cảm ơn và thông điệp tri ân độc quyền.</li>
              <li><i class="fa-solid fa-check" style="color:var(--color-terracotta);"></i> <strong>Đầy đủ chứng từ:</strong> Hóa đơn VAT, chứng nhận nguồn gốc xuất xứ và kiểm định ATTP.</li>
            </ul>
          </div>

          <div class="builder-box">
            <h3>Quy Trình Xử Lý Đơn Hàng B2B</h3>
            <div style="display:flex; gap:10px; margin-top:15px; font-size:0.85rem;">
              <div style="flex:1; background:var(--color-cream-bg); padding:10px; border-radius:4px; text-align:center;">1. Tiếp nhận yêu cầu</div>
              <div style="flex:1; background:var(--color-cream-bg); padding:10px; border-radius:4px; text-align:center;">2. Tư vấn & Gửi mẫu</div>
              <div style="flex:1; background:var(--color-cream-bg); padding:10px; border-radius:4px; text-align:center;">3. Báo giá & Hợp đồng</div>
              <div style="flex:1; background:var(--color-cream-bg); padding:10px; border-radius:4px; text-align:center;">4. Sản xuất & Giao hàng</div>
            </div>
          </div>
        </div>

        <div class="builder-box">
          <h3 style="margin-bottom: 15px;">Đăng Ký Nhận Báo Giá B2B</h3>
          <form onsubmit="handleFormSubmit(event, 'Yêu cầu báo giá B2B đã được gửi thành công!')">
            <div class="form-group">
              <label>Tên Doanh Nghiệp / Tổ Chức *</label>
              <input type="text" class="form-control" required placeholder="Công ty ABC...">
            </div>
            <div class="form-group">
              <label>Người Liên Hệ *</label>
              <input type="text" class="form-control" required placeholder="Nguyễn Văn A">
            </div>
            <div class="form-group">
              <label>Số Điện Thoại / Zalo *</label>
              <input type="tel" class="form-control" required placeholder="0901234567">
            </div>
            <div class="form-group">
              <label>Số Lượng Hộp Dự Kiến (Từ 50 hộp) *</label>
              <input type="number" class="form-control" min="50" value="50" required>
            </div>
            <div class="form-group">
              <label>Ghi Chú Yêu Cầu Cá Nhân Hóa</label>
              <textarea class="form-control" rows="3" placeholder="In logo, ngân sách dự kiến/hộp..."></textarea>
            </div>
            <button class="btn btn-primary" style="width: 100%;">Gửi Yêu Cầu Báo Giá</button>
          </form>
        </div>
      </div>
    </section>

    <!-- ==========================================
         TRANG 6: ĐẶT HÀNG (ORDERING PROCESS)
         ========================================== -->
    <section id="page-ordering" class="page-section">
      <h2 class="section-title">Quy Trình Đặt Hàng 7 Bước</h2>
      <p class="section-subtitle">Minh bạch quy trình tiếp nhận, giao nhận và hậu mãi chăm sóc khách hàng tại LocalBox.</p>

      <div class="grid-3" style="margin-top: 30px;">
        <div class="builder-box">
          <h4><i class="fa-solid fa-magnifying-glass" style="color:var(--color-terracotta);"></i> Bước 1: Khám Phá</h4>
          <p style="font-size:0.88rem; color:#555; margin-top:8px;">Tham khảo các bộ hộp quà có sẵn trên Website hoặc tự phối theo sở thích.</p>
        </div>
        <div class="builder-box">
          <h4><i class="fa-solid fa-list-check" style="color:var(--color-terracotta);"></i> Bước 2: Chọn Hộp</h4>
          <p style="font-size:0.88rem; color:#555; margin-top:8px;">Lựa chọn dòng sản phẩm Phổ thông, Tiêu chuẩn hoặc Cao cấp phù hợp ngân sách.</p>
        </div>
        <div class="builder-box">
          <h4><i class="fa-solid fa-paper-plane" style="color:var(--color-terracotta);"></i> Bước 3: Gửi Đơn</h4>
          <p style="font-size:0.88rem; color:#555; margin-top:8px;">Nhập thông tin giao hàng, thiệp chúc mừng và gửi yêu cầu trực tuyến.</p>
        </div>
        <div class="builder-box">
          <h4><i class="fa-solid fa-phone-volume" style="color:var(--color-terracotta);"></i> Bước 4: Xác Nhận</h4>
          <p style="font-size:0.88rem; color:#555; margin-top:8px;">Đội ngũ LocalBox liên hệ xác nhận thông tin đơn hàng và ngày nhận cụ thể.</p>
        </div>
        <div class="builder-box">
          <h4><i class="fa-solid fa-box-archive" style="color:var(--color-terracotta);"></i> Bước 5: Đóng Gói</h4>
          <p style="font-size:0.88rem; color:#555; margin-top:8px;">Kiểm tra chất lượng đặc sản OCOP, đóng gói chuẩn tối ưu di chuyển.</p>
        </div>
        <div class="builder-box">
          <h4><i class="fa-solid fa-truck-fast" style="color:var(--color-terracotta);"></i> Bước 6 & 7: Giao Hàng & Hậu Mãi</h4>
          <p style="font-size:0.88rem; color:#555; margin-top:8px;">Giao hàng qua GHN/GHTK, cập nhật mã vận đơn và lắng nghe phản hồi trải nghiệm.</p>
        </div>
      </div>
    </section>

    <!-- ==========================================
         TRANG 7: LIÊN HỆ (CONTACT)
         ========================================== -->
    <section id="page-contact" class="page-section">
      <h2 class="section-title">Liên Hệ Với LocalBox</h2>
      <p class="section-subtitle">Chúng tôi luôn sẵn sàng lắng nghe mọi góp ý và hỗ trợ tư vấn hộp quà phù hợp nhất với bạn.</p>

      <div class="builder-grid">
        <div class="builder-box">
          <h3>Thông Tin Liên Hệ Official</h3>
          <p style="margin-top: 15px;"><i class="fa-solid fa-envelope" style="color:var(--color-terracotta);"></i> <strong>Email:</strong> LocalBox.vn@gmail.com</p>
          <p style="margin-top: 10px;"><i class="fa-solid fa-location-dot" style="color:var(--color-terracotta);"></i> <strong>Trụ sở dự án:</strong> Trường Đại học Công nghiệp TP. Hồ Chí Minh (IUH)</p>
          <p style="margin-top: 10px;"><i class="fa-solid fa-globe" style="color:var(--color-terracotta);"></i> <strong>Kênh bán hàng chính thức:</strong> Website, TikTok Shop, Shopee, Fanpage LocalBox</p>
        </div>

        <div class="builder-box">
          <h3 style="margin-bottom: 15px;">Gửi Tin Nhắn Cho Chúng Tôi</h3>
          <form onsubmit="handleFormSubmit(event, 'Cảm ơn bạn đã liên hệ! LocalBox sẽ phản hồi trong thời gian sớm nhất.')">
            <div class="form-group">
              <label>Họ và tên *</label>
              <input type="text" class="form-control" required placeholder="Nguyễn Văn A">
            </div>
            <div class="form-group">
              <label>Email liên hệ *</label>
              <input type="email" class="form-control" required placeholder="email@example.com">
            </div>
            <div class="form-group">
              <label>Chủ đề *</label>
              <input type="text" class="form-control" required placeholder="Tư vấn mua hộp quà...">
            </div>
            <div class="form-group">
              <label>Nội dung *</label>
              <textarea class="form-control" rows="4" required placeholder="Nội dung thắc mắc hoặc góp ý..."></textarea>
            </div>
            <button class="btn btn-primary" style="width:100%;">Gửi Tin Nhắn</button>
          </form>
        </div>
      </div>
    </section>

  </main>

  <!-- ==========================================
       MODAL VIEW DETAILS & CART
       ========================================== -->
  <!-- Product Detail Modal -->
  <div class="modal-overlay" id="productModal">
    <div class="modal-card">
      <span class="modal-close" onclick="closeModal('productModal')">&times;</span>
      <div id="modalProductContent"></div>
    </div>
  </div>

  <!-- Shopping Cart Modal -->
  <div class="modal-overlay" id="cartModal">
    <div class="modal-card">
      <span class="modal-close" onclick="closeModal('cartModal')">&times;</span>
      <h3 style="margin-bottom: 20px;">Giỏ Hàng Của Bạn</h3>
      <div id="cartItemsList">
        <p style="text-align:center; opacity:0.6;">Giỏ hàng đang trống.</p>
      </div>
      <div style="border-top:1px solid var(--color-border); padding-top:15px; margin-top:15px; display:flex; justify-content:space-between; font-weight:700; font-size:1.1rem;">
        <span>Tổng thanh toán:</span>
        <span id="cartTotalPrice" style="color:var(--color-terracotta);">0đ</span>
      </div>
      <button class="btn btn-primary" style="width:100%; margin-top:20px;" onclick="checkoutCart()">Gửi Đơn Đặt Hàng</button>
    </div>
  </div>

  <!-- ==========================================
       FOOTER
       ========================================== -->
  <footer>
    <div class="container footer-grid">
      <div>
        <div class="logo-brand-text" style="color:var(--color-cream-bg); margin-bottom:15px;">
          LOCALBOX
          <span style="color:var(--color-terracotta);">GÓI TRỌN HƯƠNG VỊ VIỆT</span>
        </div>
        <p style="font-size:0.85rem; color:rgba(245,240,227,0.7);">
          Dự án kinh doanh hộp quà đặc sản địa phương tiện lợi dành cho khách du lịch và người tiêu dùng trẻ tại Việt Nam.
        </p>
      </div>

      <div class="footer-col">
        <h4>Trang Chính</h4>
        <ul>
          <li><a href="#" onclick="switchPage('home')">Trang chủ</a></li>
          <li><a href="#" onclick="switchPage('about')">Giới thiệu</a></li>
          <li><a href="#" onclick="switchPage('products')">Hộp quà</a></li>
          <li><a href="#" onclick="switchPage('builder')">Tự chọn hộp</a></li>
        </ul>
      </div>

      <div class="footer-col">
        <h4>Dịch Vụ</h4>
        <ul>
          <li><a href="#" onclick="switchPage('b2b')">Quà tặng doanh nghiệp</a></li>
          <li><a href="#" onclick="switchPage('ordering')">Quy trình đặt hàng</a></li>
          <li><a href="#" onclick="switchPage('contact')">Liên hệ & Góp ý</a></li>
        </ul>
      </div>

      <div class="footer-col">
        <h4>Liên Hệ Official</h4>
        <p style="font-size:0.88rem; color:rgba(245,240,227,0.8);">
          <i class="fa-solid fa-envelope" style="color:var(--color-terracotta);"></i> LocalBox.vn@gmail.com
        </p>
      </div>
    </div>

    <div class="footer-bottom">
      <p>&copy; 2026 LocalBox - Nhóm 9 - DHTMDT20C - Đại học Công nghiệp TP.HCM (IUH). All rights reserved.</p>
    </div>
  </footer>

  <!-- ==========================================
       JAVASCRIPT APP LOGIC
       ========================================== -->
  <script>
    /* ==========================================
       DỮ LIỆU SẢN PHẨM CHUẨN (LOCALBOX DATA)
       ========================================== */
    const PRODUCTS_DATA = [
      {
        id: "BOX-01",
        name: "Hộp Quà Tiêu Chuẩn LocalBox",
        price: 350000,
        badge: "Bán Chạy Nhất",
        region: "Tây Nguyên / Hà Nội",
        occasion: "Du lịch",
        budgetGroup: "mid",
        image: "sản phẩm.png",
        desc: "Set quà tuyển chọn đặc sắc hội tụ hương vị từ Tây Nguyên đến Thủ đô Hà Nội.",
        items: ["Cà phê Buôn Ma Thuột 100% nguyên chất", "Mật ong hoa cà phê", "Xoài sấy dẻo Miền Tây", "Bánh cốm Hà Nội đặc sản"]
      },
      {
        id: "BOX-02",
        name: "Hộp Quà Hương Vị Tây Bắc",
        price: 420000,
        badge: "OCOP Tuyển Chọn",
        region: "Tây Bắc",
        occasion: "Lễ Tết",
        budgetGroup: "mid",
        image: "sản phẩm.png",
        desc: "Đậm đà hương vị núi rừng Tây Bắc với trà xanh Thái Nguyên tuyển chọn.",
        items: ["Trà xanh Thái Nguyên thượng hạng", "Hạt dinh dưỡng cao cấp", "Thịt lợn gác bếp truyền thống"]
      },
      {
        id: "BOX-03",
        name: "Hộp Quà Thẩm Mỹ Cao Cấp",
        price: 650000,
        badge: "Cao Cấp Biếu Tặng",
        region: "Tây Nguyên",
        occasion: "Doanh nghiệp",
        budgetGroup: "high",
        image: "sản phẩm.png",
        desc: "Set quà sang trọng tích hợp ly gốm lưu niệm Việt Nam độc bản.",
        items: ["Mật ong hoa cà phê Tây Nguyên", "Cà phê Buôn Ma Thuột", "Ly gốm lưu niệm họa tiết Việt Nam", "Xoài sấy dẻo"]
      },
      {
        id: "BOX-04",
        name: "Hộp Quà Nhỏ Xinh Du Lịch",
        price: 220000,
        badge: "Phổ Thông",
        region: "Miền Tây",
        occasion: "Du lịch",
        budgetGroup: "low",
        image: "sản phẩm.png",
        desc: "Gọn nhẹ, dễ xách tay mang lên máy bay dành cho du khách trẻ.",
        items: ["Xoài sấy dẻo Miền Tây", "Bánh cốm Hà Nội", "Trà xanh túi lọc"]
      }
    ];

    const SINGLE_ITEMS_DATA = [
      { id: "ITEM-01", name: "Cà phê Buôn Ma Thuột (100% nguyên chất)", price: 85000, image: "sản phẩm.png" },
      { id: "ITEM-02", name: "Mật ong Hoa Cà Phê Tây Nguyên", price: 95000, image: "sản phẩm.png" },
      { id: "ITEM-03", name: "Xoài Sấy Dẻo Miền Tây", price: 65000, image: "sản phẩm.png" },
      { id: "ITEM-04", name: "Trà Xanh Thái Nguyên Thượng Hạng", price: 75000, image: "sản phẩm.png" },
      { id: "ITEM-05", name: "Bánh Cốm Hà Nội Truyền Thống", price: 50000, image: "sản phẩm.png" },
      { id: "ITEM-06", name: "Ly Gốm Lưu Niệm Việt Nam", price: 120000, image: "sản phẩm.png" }
    ];

    // App State
    let cart = JSON.parse(localStorage.getItem('localbox_cart')) || [];
    let selectedBuilderItems = [];

    // Init App
    document.addEventListener("DOMContentLoaded", function() {
      updateCartBadge();
      renderProductTabs();
      renderBuilderOptions();
    });

    /* ==========================================
       SPA PAGE NAVIGATION
       ========================================== */
    function switchPage(pageId) {
      document.querySelectorAll('.page-section').forEach(sec => sec.classList.remove('active-page'));
      document.querySelectorAll('.nav-link').forEach(link => link.classList.remove('active'));

      const target = document.getElementById('page-' + pageId);
      if(target) {
        target.classList.add('active-page');
        window.scrollTo({ top: 0, behavior: 'smooth' });
      }

      // Close mobile menu if open
      document.getElementById('navMenu').style.display = '';
    }

    function toggleMobileNav() {
      const menu = document.getElementById('navMenu');
      menu.style.display = (menu.style.display === 'flex') ? 'none' : 'flex';
      menu.style.flexDirection = 'column';
      menu.style.position = 'absolute';
      menu.style.top = '70px';
      menu.style.left = '0';
      menu.style.width = '100%';
      menu.style.background = 'var(--color-cream-bg)';
      menu.style.padding = '20px';
      menu.style.borderBottom = '1px solid var(--color-border)';
    }

    /* ==========================================
       PAGE 3: TAB SWITCHING & RENDERERS
       ========================================== */
    function switchProductTab(tabName) {
      document.querySelectorAll('.tab-btn').forEach(btn => btn.classList.remove('active'));
      document.querySelectorAll('.tab-content-item').forEach(content => content.style.display = 'none');

      event.target.classList.add('active');
      document.getElementById('tab-content-' + tabName).style.display = 'block';
    }

    function createProductCardHTML(p) {
      return `
        <div class="product-card">
          <span class="product-badge">${p.badge}</span>
          <img src="${p.image}" class="product-img" alt="${p.name}" onerror="this.src='https://placehold.co/400x300/173F2A/F5F0E3?text=LocalBox'">
          <div class="product-body">
            <h3 class="product-title">${p.name}</h3>
            <div class="product-price">${p.price.toLocaleString('vi-VN')}đ</div>
            <p class="product-desc">${p.desc}</p>
            <div class="product-items">
              <strong>Thành phần:</strong> ${p.items.join(', ')}
            </div>
            <div class="product-actions">
              <button class="btn btn-outline" style="flex:1;" onclick="viewProductDetail('${p.id}')">Chi Tiết</button>
              <button class="btn btn-primary" style="flex:1;" onclick="addToCart('${p.id}')"><i class="fa-solid fa-cart-plus"></i> Chọn</button>
            </div>
          </div>
        </div>
      `;
    }

    function renderProductTabs() {
      // Tab 1: Sample
      const sampleContainer = document.getElementById('sample-products-container');
      sampleContainer.innerHTML = PRODUCTS_DATA.map(p => createProductCardHTML(p)).join('');

      // Tab 2: Region
      filterByRegion('all');
      // Tab 3: Occasion
      filterByOccasion('all');
      // Tab 4: Budget
      filterByBudget('all');
    }

    function filterByRegion(region) {
      const container = document.getElementById('region-products-container');
      const list = (region === 'all') ? PRODUCTS_DATA : PRODUCTS_DATA.filter(p => p.region.includes(region));
      container.innerHTML = list.length ? list.map(p => createProductCardHTML(p)).join('') : '<p>Chưa có sản phẩm thuộc vùng này.</p>';
    }

    function filterByOccasion(occ) {
      const container = document.getElementById('occasion-products-container');
      const list = (occ === 'all') ? PRODUCTS_DATA : PRODUCTS_DATA.filter(p => p.occasion.includes(occ));
      container.innerHTML = list.length ? list.map(p => createProductCardHTML(p)).join('') : '<p>Chưa có sản phẩm phù hợp dịp này.</p>';
    }

    function filterByBudget(group) {
      const container = document.getElementById('budget-products-container');
      const list = (group === 'all') ? PRODUCTS_DATA : PRODUCTS_DATA.filter(p => p.budgetGroup === group);
      container.innerHTML = list.length ? list.map(p => createProductCardHTML(p)).join('') : '<p>Chưa có sản phẩm khoảng giá này.</p>';
    }

    /* ==========================================
       PAGE 4: BUILDER MIX-AND-MATCH
       ========================================== */
    function renderBuilderOptions() {
      const container = document.getElementById('builder-items-options');
      container.innerHTML = SINGLE_ITEMS_DATA.map(item => `
        <div class="item-select-card" id="builder-card-${item.id}" onclick="toggleBuilderItem('${item.id}')">
          <img src="${item.image}" alt="${item.name}" onerror="this.src='https://placehold.co/100x100/173F2A/F5F0E3?text=Item'">
          <h5>${item.name}</h5>
          <div class="price">${item.price.toLocaleString('vi-VN')}đ</div>
        </div>
      `).join('');
    }

    function toggleBuilderItem(itemId) {
      const card = document.getElementById('builder-card-' + itemId);
      const index = selectedBuilderItems.findIndex(i => i.id === itemId);

      if(index > -1) {
        selectedBuilderItems.splice(index, 1);
        card.classList.remove('selected');
      } else {
        const item = SINGLE_ITEMS_DATA.find(i => i.id === itemId);
        selectedBuilderItems.push(item);
        card.classList.add('selected');
      }
      updateBuilderSummary();
    }

    function updateBuilderSummary() {
      const listContainer = document.getElementById('builderSelectedList');
      const itemsPriceEl = document.getElementById('builderItemsPrice');
      const totalPriceEl = document.getElementById('builderTotalPrice');

      if(selectedBuilderItems.length === 0) {
        listContainer.innerHTML = '<p style="font-size:0.85rem; opacity:0.7;">Chưa chọn món nào...</p>';
        itemsPriceEl.innerText = '0đ';
        totalPriceEl.innerText = '42.000đ';
        return;
      }

      let itemsSum = 0;
      listContainer.innerHTML = selectedBuilderItems.map(i => {
        itemsSum += i.price;
        return `
          <div class="selected-item-row">
            <span>${i.name}</span>
            <strong>${i.price.toLocaleString('vi-VN')}đ</strong>
          </div>
        `;
      }).join('');

      itemsPriceEl.innerText = itemsSum.toLocaleString('vi-VN') + 'đ';
      totalPriceEl.innerText = (itemsSum + 42000).toLocaleString('vi-VN') + 'đ';
    }

    function addCustomBoxToCart() {
      if(selectedBuilderItems.length === 0) {
        alert('Vui lòng chọn ít nhất 1 đặc sản để tạo hộp quà!');
        return;
      }
      const occasion = document.getElementById('builderOccasionSelect').value;
      const message = document.getElementById('builderCardMessage').value;
      const total = selectedBuilderItems.reduce((sum, i) => sum + i.price, 0) + 42000;

      const customBox = {
        id: 'CUSTOM-' + Date.now(),
        name: 'Hộp Quà Tự Thiết Kế (' + occasion + ')',
        price: total,
        image: 'sản phẩm.png',
        desc: 'Thiệp chúc: "' + (message || 'Không có') + '"',
        items: selectedBuilderItems.map(i => i.name)
      };

      cart.push(customBox);
      saveCart();
      alert('Đã thêm Hộp Quà Tự Thiết Kế vào giỏ hàng!');
    }

    /* ==========================================
       CART & MODAL MANAGEMENT
       ========================================== */
    function addToCart(productId) {
      const p = PRODUCTS_DATA.find(item => item.id === productId);
      if(p) {
        cart.push(p);
        saveCart();
        alert('Đã thêm "' + p.name + '" vào giỏ hàng!');
      }
    }

    function saveCart() {
      localStorage.setItem('localbox_cart', JSON.stringify(cart));
      updateCartBadge();
    }

    function updateCartBadge() {
      document.getElementById('cartCount').innerText = cart.length;
    }

    function openCartModal() {
      const container = document.getElementById('cartItemsList');
      const totalEl = document.getElementById('cartTotalPrice');

      if(cart.length === 0) {
        container.innerHTML = '<p style="text-align:center; opacity:0.6;">Giỏ hàng đang trống.</p>';
        totalEl.innerText = '0đ';
      } else {
        let total = 0;
        container.innerHTML = cart.map((item, idx) => {
          total += item.price;
          return `
            <div style="display:flex; justify-size:space-between; align-items:center; margin-bottom:12px; padding-bottom:8px; border-bottom:1px solid var(--color-border);">
              <div>
                <strong>${item.name}</strong>
                <div style="font-size:0.8rem; color:var(--color-terracotta);">${item.price.toLocaleString('vi-VN')}đ</div>
              </div>
              <button style="background:none; border:none; color:red; cursor:pointer;" onclick="removeFromCart(${idx})"><i class="fa-solid fa-trash"></i></button>
            </div>
          `;
        }).join('');
        totalEl.innerText = total.toLocaleString('vi-VN') + 'đ';
      }

      document.getElementById('cartModal').style.display = 'flex';
    }

    function removeFromCart(index) {
      cart.splice(index, 1);
      saveCart();
      openCartModal();
    }

    function checkoutCart() {
      if(cart.length === 0) {
        alert('Giỏ hàng của bạn đang trống!');
        return;
      }
      alert('Cảm ơn bạn đã đặt hàng! LocalBox sẽ liên hệ qua điện thoại để xác nhận đơn hàng.');
      cart = [];
      saveCart();
      closeModal('cartModal');
    }

    function viewProductDetail(productId) {
      const p = PRODUCTS_DATA.find(item => item.id === productId);
      if(!p) return;

      const content = document.getElementById('modalProductContent');
      content.innerHTML = `
        <h3 style="margin-bottom:10px;">${p.name}</h3>
        <div style="font-size:1.2rem; font-weight:700; color:var(--color-terracotta); margin-bottom:15px;">${p.price.toLocaleString('vi-VN')}đ</div>
        <img src="${p.image}" style="width:100%; height:250px; object-fit:cover; border-radius:8px; margin-bottom:15px;" onerror="this.src='https://placehold.co/500x300/173F2A/F5F0E3?text=LocalBox'">
        <p><strong>Mô tả:</strong> ${p.desc}</p>
        <p style="margin-top:10px;"><strong>Thành phần chi tiết:</strong></p>
        <ul>${p.items.map(i => '<li>- ' + i + '</li>').join('')}</ul>
        <button class="btn btn-primary" style="width:100%; margin-top:20px;" onclick="addToCart('${p.id}'); closeModal('productModal');">Thêm Vào Giỏ Hàng</button>
      `;

      document.getElementById('productModal').style.display = 'flex';
    }

    function closeModal(modalId) {
      document.getElementById(modalId).style.display = 'none';
    }

    function handleFormSubmit(event, successMsg) {
      event.preventDefault();
      alert(successMsg);
      event.target.reset();
    }
  </script>
</body>
</html>
