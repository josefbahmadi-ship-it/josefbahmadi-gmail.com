
<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>آموزیار - آموزش آنلاین</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Reset & Base Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        :root {
            --primary: #4a6bff;
            --secondary: #ff6b6b;
            --dark: #2d3748;
            --light: #f8f9fa;
            --gray: #718096;
            --success: #48bb78;
        }
        
        body {
            background-color: #f5f7ff;
            color: var(--dark);
            line-height: 1.6;
        }
        
        a {
            text-decoration: none;
            color: inherit;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }
        
        /* Header Styles */
        header {
            background-color: white;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 0;
        }
        
        .logo {
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--primary);
        }
        
        .logo i {
            color: var(--secondary);
        }
        
        .nav-links {
            display: flex;
            list-style: none;
            gap: 25px;
        }
        
        .nav-links a {
            font-weight: 600;
            transition: color 0.3s;
            position: relative;
        }
        
        .nav-links a:hover {
            color: var(--primary);
        }
        
        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            right: 0;
            width: 0;
            height: 2px;
            background-color: var(--primary);
            transition: width 0.3s;
        }
        
        .nav-links a:hover::after {
            width: 100%;
        }
        
        .cta-button {
            background-color: var(--primary);
            color: white;
            padding: 10px 20px;
            border-radius: 30px;
            font-weight: 600;
            transition: all 0.3s;
        }
        
        .cta-button:hover {
            background-color: #3a5bff;
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(74, 107, 255, 0.2);
        }
        
        .mobile-menu {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
        }
        
        /* Hero Section */
        .hero {
            padding: 80px 0;
            background: linear-gradient(135deg, #f5f7ff 0%, #e3e9ff 100%);
        }
        
        .hero-container {
            display: flex;
            align-items: center;
            gap: 40px;
        }
        
        .hero-text {
            flex: 1;
        }
        
        .hero-image {
            flex: 1;
            text-align: center;
        }
        
        .hero-image img {
            max-width: 100%;
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }
        
        .hero h1 {
            font-size: 2.8rem;
            margin-bottom: 20px;
            color: var(--dark);
            line-height: 1.2;
        }
        
        .hero p {
            font-size: 1.1rem;
            color: var(--gray);
            margin-bottom: 30px;
        }
        
        .hero-buttons {
            display: flex;
            gap: 15px;
        }
        
        .btn {
            padding: 12px 25px;
            border-radius: 30px;
            font-weight: 600;
            transition: all 0.3s;
            display: inline-flex;
            align-items: center;
            gap: 8px;
        }
        
        .btn-primary {
            background-color: var(--primary);
            color: white;
        }
        
        .btn-secondary {
            background-color: white;
            color: var(--primary);
            border: 2px solid var(--primary);
        }
        
        .btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        /* Courses Section */
        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }
        
        .section-title h2 {
            font-size: 2.2rem;
            margin-bottom: 15px;
            color: var(--dark);
        }
        
        .section-title p {
            color: var(--gray);
            max-width: 600px;
            margin: 0 auto;
        }
        
        .courses {
            padding: 80px 0;
        }
        
        .course-cards {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .course-card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .course-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.1);
        }
        
        .course-img {
            height: 180px;
            background-color: var(--primary);
            background-image: linear-gradient(to right, #4a6bff, #6a8bff);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 3rem;
        }
        
        .course-content {
            padding: 25px;
        }
        
        .course-category {
            display: inline-block;
            background-color: #e9f7fe;
            color: #3182ce;
            padding: 5px 12px;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: 600;
            margin-bottom: 10px;
        }
        
        .course-title {
            font-size: 1.3rem;
            margin-bottom: 10px;
            color: var(--dark);
        }
        
        .course-desc {
            color: var(--gray);
            font-size: 0.95rem;
            margin-bottom: 20px;
        }
        
        .course-footer {
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-top: 1px solid #eee;
            padding-top: 15px;
        }
        
        .course-price {
            font-weight: 700;
            color: var(--primary);
            font-size: 1.2rem;
        }
        
        .course-button {
            color: var(--primary);
            font-weight: 600;
            font-size: 0.9rem;
            transition: color 0.3s;
        }
        
        .course-button:hover {
            color: var(--secondary);
        }
        
        /* Features Section */
        .features {
            padding: 80px 0;
            background-color: white;
        }
        
        .feature-cards {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 30px;
        }
        
        .feature-card {
            text-align: center;
            padding: 30px 20px;
            border-radius: 10px;
            background-color: #f8f9fa;
            transition: all 0.3s;
        }
        
        .feature-card:hover {
            background-color: white;
            box-shadow: 0 10px 25px rgba(0,0,0,0.05);
        }
        
        .feature-icon {
            width: 70px;
            height: 70px;
            background-color: rgba(74, 107, 255, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 20px;
            font-size: 1.8rem;
            color: var(--primary);
        }
        
        .feature-card h3 {
            margin-bottom: 15px;
            color: var(--dark);
        }
        
        .feature-card p {
            color: var(--gray);
            font-size: 0.95rem;
        }
        
        /* Footer */
        footer {
            background-color: var(--dark);
            color: white;
            padding: 60px 0 30px;
        }
        
        .footer-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }
        
        .footer-col h3 {
            font-size: 1.3rem;
            margin-bottom: 20px;
            position: relative;
            padding-bottom: 10px;
        }
        
        .footer-col h3::after {
            content: '';
            position: absolute;
            bottom: 0;
            right: 0;
            width: 40px;
            height: 2px;
            background-color: var(--primary);
        }
        
        .footer-links {
            list-style: none;
        }
        
        .footer-links li {
            margin-bottom: 10px;
        }
        
        .footer-links a {
            color: #cbd5e0;
            transition: color 0.3s;
        }
        
        .footer-links a:hover {
            color: white;
            padding-right: 5px;
        }
        
        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }
        
        .social-links a {
            width: 40px;
            height: 40px;
            background-color: rgba(255,255,255,0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.3s;
        }
        
        .social-links a:hover {
            background-color: var(--primary);
            transform: translateY(-3px);
        }
        
        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255,255,255,0.1);
            color: #a0aec0;
            font-size: 0.9rem;
        }
        
        /* Responsive */
        @media (max-width: 992px) {
            .hero-container {
                flex-direction: column;
            }
            
            .hero-text, .hero-image {
                text-align: center;
            }
            
            .hero-buttons {
                justify-content: center;
            }
        }
        
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .mobile-menu {
                display: block;
            }
            
            .hero h1 {
                font-size: 2.2rem;
            }
            
            .course-cards, .feature-cards {
                grid-template-columns: 1fr;
            }
            
            .footer-container {
                grid-template-columns: 1fr;
                gap: 30px;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-container">
            <a href="#" class="logo">
                <i class="fas fa-graduation-cap"></i>
                <span>آموزیار</span>
            </a>
            
            <ul class="nav-links">
                <li><a href="#">خانه</a></li>
                <li><a href="#courses">دوره‌ها</a></li>
                <li><a href="#features">ویژگی‌ها</a></li>
                <li><a href="#">درباره ما</a></li>
                <li><a href="#">تماس با ما</a></li>
            </ul>
            
            <a href="#" class="cta-button">ورود / ثبت‌نام</a>
            
            <div class="mobile-menu">
                <i class="fas fa-bars"></i>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container hero-container">
            <div class="hero-text">
                <h1>یادگیری آنلاین با بهترین اساتید</h1>
                <p>در آموزیار، به هزاران دوره آموزشی در زمینه‌های برنامه‌نویسی، طراحی، بازاریابی، زبان و مهارت‌های فردی دسترسی دارید. هر زمان و هر کجا که بخواهید یاد بگیرید.</p>
                <div class="hero-buttons">
                    <a href="#courses" class="btn btn-primary">
                        <i class="fas fa-play-circle"></i> مشاهده دوره‌ها
                    </a>
                    <a href="#" class="btn btn-secondary">
                        <i class="fas fa-user"></i> عضویت رایگان
                    </a>
                </div>
            </div>
            <div class="hero-image">
                <!-- Placeholder for image -->
                <div style="background-color: #4a6bff; color: white; padding: 40px; border-radius: 10px; font-size: 1.5rem;">
                    <i class="fas fa-laptop-code" style="font-size: 5rem; margin-bottom: 20px;"></i>
                    <p>آموزش آنلاین تعاملی</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Courses Section -->
    <section id="courses" class="courses">
        <div class="container">
            <div class="section-title">
                <h2>دوره‌های محبوب</h2>
                <p>با کیفیت‌ترین دوره‌های آموزشی را با تدریس اساتید مجرب تجربه کنید</p>
            </div>
            
            <div class="course-cards">
                <!-- Course 1 -->
                <div class="course-card">
                    <div class="course-img">
                        <i class="fas fa-code"></i>
                    </div>
                    <div class="course-content">
                        <span class="course-category">برنامه‌نویسی</span>
                        <h3 class="course-title">دوره جامع توسعه وب</h3>
                        <p class="course-desc">یادگیری HTML, CSS, JavaScript و React از صفر تا صد با پروژه‌های عملی</p>
                        <div class="course-footer">
                            <div class="course-price">۴۹۰,۰۰۰ تومان</div>
                            <a href="#" class="course-button">مشاهده دوره →</a>
                        </div>
                    </div>
                </div>
                
                <!-- Course 2 -->
                <div class="course-card">
                    <div class="course-img">
                        <i class="fas fa-palette"></i>
                    </div>
                    <div class="course-content">
                        <span class="course-category">طراحی</span>
                        <h3 class="course-title">طراحی رابط کاربری (UI/UX)</h3>
                        <p class="course-desc">اصول طراحی تجربه کاربری و رابط کاربری با Figma و Adobe XD</p>
                        <div class="course-footer">
                            <div class="course-price">۳۶۰,۰۰۰ تومان</div>
                            <a href="#" class="course-button">مشاهده دوره →</a>
                        </div>
                    </div>
                </div>
                
                <!-- Course 3 -->
                <div class="course-card">
                    <div class="course-img">
                        <i class="fas fa-chart-line"></i>
                    </div>
                    <div class="course-content">
                        <span class="course-category">بازاریابی</span>
                        <h3 class="course-title">دیجیتال مارکتینگ پیشرفته</h3>
                        <p class="course-desc">استراتژی‌های بازاریابی در شبکه‌های اجتماعی و سئو برای کسب‌وکارها</p>
                        <div class="course-footer">
                            <div class="course-price">۴۲۰,۰۰۰ تومان</div>
                            <a href="#" class="course-button">مشاهده دوره →</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section id="features" class="features">
        <div class="container">
            <div class="section-title">
                <h2>چرا آموزیار؟</h2>
                <p>ویژگی‌هایی که آموزیار را به بهترین پلتفرم آموزشی تبدیل می‌کند</p>
            </div>
            
            <div class="feature-cards">
                <!-- Feature 1 -->
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-play-circle"></i>
                    </div>
                    <h3>دوره‌های ویدیویی</h3>
                    <p>دسترسی به باکیفیت‌ترین ویدیوهای آموزشی با قابلیت پخش در همه دستگاه‌ها</p>
                </div>
                
                <!-- Feature 2 -->
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-user-graduate"></i>
                    </div>
                    <h3>اساتید مجرب</h3>
                    <p>یادگیری از برترین اساتید هر حوزه با سال‌ها تجربه کاری و تدریس</p>
                </div>
                
                <!-- Feature 3 -->
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-certificate"></i>
                    </div>
                    <h3>گواهی معتبر</h3>
                    <p>دریافت گواهی پایان دوره معتبر پس از اتمام موفقیت‌آمیز هر دوره</p>
                </div>
                
                <!-- Feature 4 -->
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-headset"></i>
                    </div>
                    <h3>پشتیبانی ۲۴/۷</h3>
                    <p>پشتیبانی همه‌روزه و پاسخ به سوالات شما توسط تیم پشتیبانی آموزیار</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-container">
                <!-- Column 1 -->
                <div class="footer-col">
                    <h3>آموزیار</h3>
                    <p>پلتفرم آموزش آنلاین با هدف دسترسی همه به آموزش‌های باکیفیت در هر زمان و مکان</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-telegram"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-youtube"></i></a>
                    </div>
                </div>
                
                <!-- Column 2 -->
                <div class="footer-col">
                    <h3>لینک‌های سریع</h3>
                    <ul class="footer-links">
                        <li><a href="#">خانه</a></li>
                        <li><a href="#courses">دوره‌ها</a></li>
                        <li><a href="#features">ویژگی‌ها</a></li>
                        <li><a href="#">درباره ما</a></li>
                        <li><a href="#">تماس با ما</a></li>
                    </ul>
                </div>
                
                <!-- Column 3 -->
                <div class="footer-col">
                    <h3>دسته‌بندی دوره‌ها</h3>
                    <ul class="footer-links">
                        <li><a href="#">برنامه‌نویسی</a></li>
                        <li><a href="#">طراحی و گرافیک</a></li>
                        <li><a href="#">بازاریابی</a></li>
                        <li><a href="#">زبان‌های خارجی</a></li>
                        <li><a href="#">مهارت‌های فردی</a></li>
                    </ul>
                </div>
                
                <!-- Column 4 -->
                <div class="footer-col">
                    <h3>تماس با ما</h3>
                    <ul class="footer-links">
                        <li><i class="fas fa-map-marker-alt"></i> تهران، خیابان آزادی</li>
                        <li><i class="fas fa-phone"></i> ۰۲۱-۱۲۳۴۵۶۷۸</li>
                        <li><i class="fas fa-envelope"></i> info@amoozhyar.com</li>
                    </ul>
                </div>
            </div>
            
            <div class="copyright">
                <p>© ۲۰۲۳ کلیه حقوق برای آموزیار محفوظ است.</p>
            </div>
        </div>
    </footer>

    <script>
        // Mobile menu toggle
        const mobileMenuBtn = document.querySelector('.mobile-menu');
        const navLinks = document.querySelector('.nav-links');
        
        mobileMenuBtn.addEventListener('click', () => {
            navLinks.style.display = navLinks.style.display === 'flex' ? 'none' : 'flex';
        });
        
        // Close mobile menu on window resize
        window.addEventListener('resize', () => {
            if (window.innerWidth > 768) {
                navLinks.style.display = 'flex';
            } else {
                navLinks.style.display = 'none';
            }
        });
        
        // Smooth scroll for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if (targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                    
                    // Close mobile menu if open
                    if (window.innerWidth <= 768) {
                        navLinks.style.display = 'none';
                    }
                }
            });
        });
    </script>
</body>
</html>![Banner-min-2](https://github.com/user-attachments/assets/f150e9b0-73f3-4a7d-914d-67c995129560)
<img width="1300" height="731" alt="web-dising3-1300x731" src="https://github.com/user-attachments/assets/b868d828-8d02-4e3a-9cf8-f6dde6c7e20a" />
