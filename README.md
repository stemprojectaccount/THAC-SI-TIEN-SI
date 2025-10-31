<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Thạc Sĩ - Tiến Sĩ | Trường THCS Nguyễn Khuyến</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Quicksand:wght@400;500;600;700&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700;800;900&display=swap" rel="stylesheet">
    <style>
        /* ===== RESET & BASE STYLES ===== */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Quicksand', sans-serif;
        }
        
        :root {
            --primary-color: #1a2a6c;
            --secondary-color: #2A4D9B;
            --accent-color: #3a6dc9;
            --gold-color: #FFD700;
            --gold-light: #FFEC8B;
            --orange-color: #FF8C42;
            --text-light: #F8F6F2;
            --text-dark: #0a192f;
            --shadow-light: rgba(255, 255, 255, 0.1);
            --shadow-dark: rgba(0, 0, 0, 0.3);
            --gradient-primary: linear-gradient(135deg, #1a2a6c, #2A4D9B, #3a6dc9);
            --gradient-gold: linear-gradient(45deg, #FFD700, #FFA500, #FFD700);
            --gradient-card: linear-gradient(135deg, rgba(58, 109, 201, 0.8), rgba(42, 77, 155, 0.9));
            --gradient-orange: linear-gradient(135deg, rgba(255, 140, 66, 0.9), rgba(232, 106, 51, 0.9));
            --transition-slow: all 0.8s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            --transition-medium: all 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            --transition-fast: all 0.3s ease;
        }
        
        body {
            background: 
                linear-gradient(rgba(255, 255, 255, 0.4), rgba(255, 255, 255, 0.4)),
                url('https://i.postimg.cc/yNGwbLmr/DSC08251.jpg') no-repeat center center fixed;
            background-size: cover;
            color: var(--text-light);
            min-height: 100vh;
            overflow-x: hidden;
            position: relative;
        }
        
        /* ===== BACKGROUND EFFECTS ===== */
        .dynamic-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -3;
            background: linear-gradient(-45deg, rgba(26, 42, 108, 0.2), rgba(42, 77, 155, 0.2), rgba(58, 109, 201, 0.2), rgba(77, 138, 230, 0.2), rgba(26, 42, 108, 0.2));
            background-size: 400% 400%;
            animation: gradientShift 20s ease infinite;
        }
        
        @keyframes gradientShift {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }
        
        .particles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -2;
            overflow: hidden;
        }
        
        .particle {
            position: absolute;
            background: radial-gradient(circle, rgba(255, 215, 0, 0.7) 0%, rgba(255, 215, 0, 0) 70%);
            border-radius: 50%;
            animation: particleFloat 25s infinite linear;
            filter: blur(1px);
        }
        
        @keyframes particleFloat {
            0% {
                transform: translateY(100vh) rotate(0deg);
                opacity: 0;
            }
            10% {
                opacity: 1;
            }
            90% {
                opacity: 1;
            }
            100% {
                transform: translateY(-100px) rotate(360deg);
                opacity: 0;
            }
        }
        
        .floating-elements {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }
        
        .floating-element {
            position: absolute;
            background: rgba(255, 215, 0, 0.1);
            border-radius: 50%;
            animation: float 25s infinite linear;
            box-shadow: 0 0 30px rgba(255, 215, 0, 0.3);
        }
        
        @keyframes float {
            0% {
                transform: translateY(0) rotate(0deg);
                opacity: 0;
            }
            10% {
                opacity: 1;
            }
            90% {
                opacity: 1;
            }
            100% {
                transform: translateY(-1000px) rotate(360deg);
                opacity: 0;
            }
        }
        
        .spotlight {
            position: fixed;
            width: 300px;
            height: 300px;
            border-radius: 50%;
            background: radial-gradient(circle, rgba(255,215,0,0.2) 0%, rgba(255,215,0,0) 70%);
            pointer-events: none;
            z-index: -1;
            animation: spotlightMove 20s infinite linear;
            filter: blur(15px);
        }
        
        @keyframes spotlightMove {
            0% { transform: translate(10vw, 10vh); }
            25% { transform: translate(80vw, 30vh); }
            50% { transform: translate(40vw, 70vh); }
            75% { transform: translate(70vw, 50vh); }
            100% { transform: translate(10vw, 10vh); }
        }
        
        /* ===== CONTAINER & LAYOUT ===== */
        .container {
            width: 100%;
            min-height: 100vh;
            background: rgba(10, 25, 47, 0.3);
            backdrop-filter: blur(2px);
            position: relative;
            overflow: hidden;
        }
        
        .container::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: 
                url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" preserveAspectRatio="none"><defs><pattern id="grain" width="100" height="100" patternUnits="userSpaceOnUse"><circle cx="50" cy="50" r="1" fill="rgba(255,255,255,0.03)"/></pattern></defs><rect width="100" height="100" fill="url(%23grain)"/></svg>'),
                linear-gradient(135deg, transparent 0%, rgba(255, 215, 0, 0.05) 100%);
            pointer-events: none;
            z-index: 0;
        }
        
        /* ===== HEADER STYLES ===== */
        header {
            background: 
                linear-gradient(135deg, rgba(42, 77, 155, 0.4), rgba(58, 109, 201, 0.3)),
                url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" preserveAspectRatio="none"><path d="M0,0 L100,0 L100,100 Z" fill="rgba(255,215,0,0.1)"/></svg>');
            color: var(--text-light);
            text-align: center;
            padding: 120px 20px 100px;
            position: relative;
            overflow: hidden;
            border-bottom: 1px solid rgba(255, 215, 0, 0.3);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }
        
        header::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: 
                radial-gradient(circle at 20% 80%, rgba(255, 215, 0, 0.1) 0%, transparent 50%),
                radial-gradient(circle at 80% 20%, rgba(255, 215, 0, 0.1) 0%, transparent 50%);
            z-index: 1;
        }
        
        .header-content {
            position: relative;
            z-index: 2;
        }
        
        .header-logo {
            position: absolute;
            top: 30px;
            left: 50px;
            height: 250px;
            width: auto;
            z-index: 10;
            filter: drop-shadow(0 0 15px rgba(255, 215, 0, 0.7));
            transition: var(--transition-medium);
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.1);
            padding: 10px;
            backdrop-filter: blur(10px);
        }
        
        .header-logo:hover {
            transform: scale(1.1) rotate(5deg);
            filter: drop-shadow(0 0 20px rgba(255, 215, 0, 0.9));
        }
        
        .header-icon {
            font-size: 4rem;
            color: var(--gold-color);
            margin-bottom: 30px;
            text-shadow: 0 0 15px rgba(255, 215, 0, 0.7);
            animation: float 3s ease-in-out infinite;
        }
        
        @keyframes float {
            0%, 100% {
                transform: translateY(0);
            }
            50% {
                transform: translateY(-10px);
            }
        }
        
        /* CHỈNH SỬA: Làm chữ VINH DANH to hơn */
        .glowing-text {
            font-size: 6rem; /* Tăng từ 5rem lên 7rem */
            margin-bottom: 20px;
            text-shadow: 0 0 10px rgba(254 , 224 , 255 , 0 ), 0 0 20px rgba(255, 215, 0, 0.5), 0 0 30px rgba(255, 215, 0, 0 );
            position: relative;
            background: linear-gradient(45deg, #FFD700, #FFA500, #FFD700);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            font-weight: 700;
            letter-spacing: 2px;
            animation: glow 3s ease-in-out infinite alternate;
            font-family: 'Playfair Display', serif;
        }
        
        @keyframes glow {
            0% {
                text-shadow: 0 0 10px rgba(255, 215, 0, 0), 0 0 20px rgba(255, 215, 0, 0.5), 0 0 30px rgba(255, 215, 0, 0 );
            }
            100% {
                text-shadow: 0 0 15px rgba(255, 215, 0, 0.8), 0 0 25px rgba(255, 215, 0, 0.6), 0 0 35px rgba(255, 215, 0, 0.4);
            }
        }
        
        /* CHỈNH SỬA: Làm chữ "THẠC SĨ - TIẾN SĨ" màu trắng */
        .subtitle {
            font-size: 2.2rem; /* Tăng kích thước chữ */
            margin-bottom: 15px;
            position: relative;
            color: #FFFFFF; /* Đã đổi thành màu trắng */
            font-weight: 800; /* Làm đậm hơn */
            text-shadow: 0 0 10px rgba(255, 255, 255, 0.7), 0 0 20px rgba(255, 255, 255, 0.5); /* Thêm hiệu ứng bóng trắng */
            padding: 5px 0;
            letter-spacing: 1px; /* Tăng khoảng cách chữ */
            font-family: 'Playfair Display', serif; /* Dùng font trang trọng hơn */
        }
        
        .header-decoration {
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 20px;
            background: linear-gradient(90deg, transparent, var(--gold-color), transparent);
            opacity: 0.5;
        }
        
        /* ===== MAIN CONTENT STYLES ===== */
        .main-content {
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 80vh;
            padding: 80px 20px;
            flex-direction: column;
            gap: 100px;
        }
        
        .section-title {
            font-size: 3.5rem;
            text-align: center;
            margin-bottom: 60px;
            background: linear-gradient(45deg, #FFD700, #FFA500, #FFD700);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 0 15px rgba(255, 215, 0, 0.5);
            font-weight: 700;
            position: relative;
            display: inline-block;
            padding: 0 20px;
            font-family: 'Playfair Display', serif;
        }
        
        .section-title::after {
            content: "";
            position: absolute;
            bottom: -15px;
            left: 20%;
            width: 60%;
            height: 4px;
            background: linear-gradient(90deg, transparent, #FFD700, transparent);
            border-radius: 2px;
        }
        
        .section-title i {
            margin-right: 15px;
            font-size: 3rem;
            vertical-align: middle;
        }
        
        /* ===== STUDENT CARDS STYLES ===== */
        .students-section {
            width: 100%;
            max-width: 1400px;
            text-align: center;
        }
        
        .year-title {
            font-size: 2.8rem;
            margin-bottom: 40px;
            background: linear-gradient(45deg, #FFD700, #FFA500, #FFD700);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            font-weight: 700;
            font-family: 'Playfair Display', serif;
        }
        
        .students-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
            gap: 30px;
            margin-bottom: 60px;
        }
        
        .student-card {
            background: linear-gradient(135deg, rgba(58, 109, 201, 0.8), rgba(42, 77, 155, 0.9));
            border-radius: 20px;
            padding: 25px;
            text-align: center;
            border: 2px solid rgba(255, 215, 0, 0.4);
            transition: all 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3), 0 0 15px rgba(255, 215, 0, 0.2);
            position: relative;
            overflow: hidden;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: flex-start;
            min-height: 380px;
        }
        
        .student-card::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, transparent, rgba(255,255,255,0.1), transparent);
            transform: translateX(-100%) skewX(-15deg);
            transition: transform 0.8s;
        }
        
        .student-card:hover::before {
            transform: translateX(100%) skewX(-15deg);
        }
        
        .student-card:hover {
            transform: translateY(-10px) scale(1.03);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.4), 0 0 30px rgba(255, 215, 0, 0.4);
        }
        
        .student-icon {
            font-size: 3.5rem;
            margin-bottom: 15px;
            color: #FFD700;
            text-shadow: 0 0 15px rgba(255, 215, 0, 0.7);
            filter: drop-shadow(0 0 8px rgba(255, 215, 0, 0.5));
        }
        
        .student-image {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            object-fit: cover;
            margin-bottom: 15px;
            border: 3px solid rgba(255, 215, 0, 0.6);
            box-shadow: 0 0 15px rgba(255, 215, 0, 0.5);
        }
        
        .student-card h3 {
            font-size: 1.6rem;
            margin-bottom: 10px;
            color: #fff;
            font-weight: 600;
            line-height: 1.3;
        }
        
        .student-nienkhoa {
            font-size: 1.2rem;
            margin-bottom: 15px;
            color: #FFD700;
            font-weight: 500;
        }
        
        .achievement-badge {
            background: linear-gradient(45deg, #FFD700, #FFA500);
            color: #1a2a6c;
            padding: 8px 15px;
            border-radius: 20px;
            font-size: 1rem;
            font-weight: 600;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
            max-width: 100%;
            overflow: hidden;
            text-overflow: ellipsis;
            margin-bottom: 10px;
        }
        
        .student-details {
            font-size: 0.9rem;
            line-height: 1.4;
            color: #e0e0ff;
            text-align: left;
            max-height: 120px;
            overflow-y: auto;
            padding: 5px;
            width: 100%;
        }
        
        /* ===== BACK BUTTON STYLES ===== */
        .back-to-board-section {
            width: 100%;
            text-align: center;
            margin-top: 30px;
        }
        
        .back-to-board-button {
            background: linear-gradient(135deg, rgba(255, 140, 66, 0.9), rgba(232, 106, 51, 0.9));
            border-radius: 35px;
            width: 500px;
            height: 100px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.8rem;
            font-weight: bold;
            border: 4px solid rgba(255, 215, 0, 0.7);
            transition: all 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.4), 0 0 25px rgba(255, 140, 66, 0.5);
            cursor: pointer;
            text-align: center;
            padding: 20px;
            margin: 0 auto;
            position: relative;
            overflow: hidden;
            text-decoration: none;
            color: inherit;
        }
        
        .back-to-board-button::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, transparent, rgba(255,255,255,0.2), transparent);
            transform: translateX(-100%) skewX(-15deg);
            transition: transform 0.8s;
        }
        
        .back-to-board-button:hover::before {
            transform: translateX(100%) skewX(-15deg);
        }
        
        .back-to-board-button:hover {
            transform: translateY(-10px) scale(1.05);
            box-shadow: 0 25px 50px rgba(0, 0, 0, 0.5), 0 0 40px rgba(255, 140, 66, 0.7);
        }
        
        .back-to-board-button .button-icon {
            font-size: 2.5rem;
            margin-right: 15px;
            color: #FFD700;
            text-shadow: 0 0 15px rgba(255, 215, 0, 0.7);
            filter: drop-shadow(0 0 10px rgba(255, 215, 0, 0.5));
            transition: all 0.4s;
        }
        
        .back-to-board-button:hover .button-icon {
            transform: scale(1.2);
            filter: drop-shadow(0 0 15px rgba(255, 215, 0, 0.9));
        }
        
        .back-to-board-button .button-text {
            background: linear-gradient(45deg, #FFD700, #FFA500);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            font-weight: 700;
            letter-spacing: 0.5px;
            text-shadow: 0 0 10px rgba(255, 215, 0, 0.3);
            line-height: 1.2;
        }
        
        /* ===== RESPONSIVE STYLES ===== */
        @media (max-width: 1200px) {
            .back-to-board-button {
                width: 450px;
                height: 90px;
            }
        }
        
        @media (max-width: 992px) {
            .header-logo {
                position: relative;
                top: auto;
                left: auto;
                margin-bottom: 30px;
            }
            
            .glowing-text {
                font-size: 5rem;
            }
            
            .subtitle {
                font-size: 1.8rem; /* Điều chỉnh kích thước cho tablet */
            }
            
            .back-to-board-button {
                width: 400px;
                height: 80px;
                font-size: 1.6rem;
            }
            
            .back-to-board-button .button-icon {
                font-size: 2.2rem;
            }
            
            .students-grid {
                grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            }
        }
        
        @media (max-width: 768px) {
            .header-logo {
                height: 120px;
            }
            
            .glowing-text {
                font-size: 3.5rem;
            }
            
            .subtitle {
                font-size: 1.5rem; /* Điều chỉnh kích thước cho mobile */
            }
            
            .students-grid {
                grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
                gap: 20px;
            }
            
            .back-to-board-button {
                width: 90%;
                height: 70px;
                font-size: 1.4rem;
            }
            
            .back-to-board-button .button-icon {
                font-size: 2rem;
            }
            
            .section-title {
                font-size: 2.5rem;
            }
        }
        
        @media (max-width: 576px) {
            .header {
                padding: 80px 20px 60px;
            }
            
            .glowing-text {
                font-size: 2.8rem;
            }
            
            .subtitle {
                font-size: 1.3rem; /* Điều chỉnh kích thước cho mobile nhỏ */
            }
            
            .students-grid {
                grid-template-columns: 1fr;
                gap: 15px;
            }
            
            .student-card {
                min-height: 350px;
                padding: 20px;
            }
            
            .back-to-board-button {
                height: 60px;
                font-size: 1.2rem;
                padding: 15px;
            }
            
            .back-to-board-button .button-icon {
                font-size: 1.8rem;
                margin-right: 10px;
            }
            
            .section-title {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <!-- Background Elements -->
    <div class="dynamic-bg"></div>
    <div class="particles" id="particles"></div>
    <div class="floating-elements" id="floatingElements"></div>
    <div class="spotlight"></div>
    
    <div class="container">
        <!-- Header Section -->
        <header>
            <img src="https://i.postimg.cc/zGwcmPH1/image.png" alt="Logo Trường" class="header-logo">
            <div class="header-content">
                <div class="header-icon">
                    <i class="fas fa-graduation-cap"></i>
                </div>
                <h1 class="glowing-text">BẢNG VINH DANH</h1>
                <p class="subtitle">THẠC SĨ - TIẾN SĨ</p>
                <p class="subtitle">TRƯỜNG THCS NGUYỄN KHUYẾN - XÃ EA KAR - TỈNH ĐẮK LẮK</p>
                <div class="header-decoration"></div>
            </div>
        </header>
        
        <!-- Main Content -->
        <div class="main-content">
            <!-- Students Section -->
            <div class="students-section">
                <h2 class="section-title">
                    <i class="fas fa-users"></i>DANH SÁCH THẠC SĨ - TIẾN SĨ 
                </h2>
                
                <h3 class="year-title">CÁC THẠC SĨ - TIẾN SĨ</h3>
                
                <div class="students-grid" id="studentsGrid">
                    <!-- Thạc sĩ 1 -->
                    <div class="student-card">
                        <i class="fas fa-user-graduate student-icon"></i>
                        <img src="https://i.postimg.cc/pXKHFCj7/z7155430514556-a28582aaea15b1af8f5ac6a324a0ce69.jpg" alt="Thạc sĩ Nguyễn Hoàng Châu" class="student-image">
                        <h3>Nguyễn Hoàng Châu</h3>
                        <div class="student-nienkhoa">Niên khoá 2007-2011</div>
                        <div class="achievement-badge">ThS. Phi công - Vietjet Aviation</div>
                        <div class="student-details">
                            <strong>Thành tích:</strong> HCB cuộc thi Olympic Tiếng Anh trên Internet cấp QG, Giải Ba cuộc thi HSG cấp tỉnh môn Tiếng Anh.<br>
                            <strong>2016-2020:</strong> Làm việc tại Hãng hàng không Vietjet; tiếp viên Hàng không.<br>
                            <strong>2020-2021:</strong> Hoàn thành Commercial Pilot License tại trường Air Venture, Olive Branch, Mississippi, USA.<br>
                            <strong>2023:</strong> Hoàn thành khoá học chuyển loại tàu bay Airbus A320 Type Rating tại Vietjet Aviation Academy.<br>
                            <strong>Hiện nay:</strong> Làm phi công của Vietjet, chức vụ: Cơ phó.
                        </div>
                    </div>
                    
                    <!-- Thạc sĩ 2 -->
                    <div class="student-card">
                        <i class="fas fa-user-graduate student-icon"></i>
                        <img src="https://i.postimg.cc/SKPwvg6r/z7161283901144-c5cb1c82ad095a2e3160c96bdaa20467.jpg" alt="Thạc sĩ Nguyễn Ngọc Sơn" class="student-image">
                        <h3>Nguyễn Ngọc Sơn</h3>
                        <div class="student-nienkhoa">Niên khoá 2011-2015</div>
                        <div class="achievement-badge">ThS. Quân sự - Thượng úy</div>
                        <div class="student-details">
                            <strong>Thành tích:</strong> Học sinh giỏi môn Toán cấp Tỉnh, cấp Quốc gia.<br>
                            <strong>Học vấn:</strong> Tốt nghiệp Học Viện Biên phòng thành phố Kaliningrad - Liên Bang Nga và được Bộ Quốc phòng tặng Bằng Khen.<br>
                            <strong>Hiện nay:</strong> Mang quân Hàm Thượng úy, đang công tác tại Đoàn 871 trực thuộc Tổng cục chính trị Quân đội nhân dân Việt Nam.<br>
                            <strong>Bằng cấp:</strong> Đã tốt nghiệp Xuất sắc chương trình Thạc sĩ.
                        </div>
                    </div>
                    
                    <!-- Thạc sĩ 3 -->
                    <div class="student-card">
                        <i class="fas fa-user-graduate student-icon"></i>
                        <img src="https://i.postimg.cc/2Sns9JkF/Chat-GPT-Image-Oct-20-2025-08-20-11-PM.png" alt="Thạc sĩ Trần Văn Nam" class="student-image">
                        <h3>ThS. Trần Văn Nam</h3>
                        <div class="student-nienkhoa">Niên khoá 2005-2009</div>
                        <div class="achievement-badge">ThS. Công nghệ Thông tin</div>
                        <div class="student-details">
                            <strong>Học vấn:</strong> Tốt nghiệp Thạc sĩ Công nghệ Thông tin tại Đại học Bách Khoa Hà Nội.<br>
                            <strong>Kinh nghiệm:</strong> 8 năm làm việc trong lĩnh vực phát triển phần mềm.<br>
                            <strong>Hiện nay:</strong> Giám đốc kỹ thuật tại công ty FPT Software, chuyên về các giải pháp AI và Machine Learning.<br>
                            <strong>Thành tích:</strong> Đạt giải Nhì Olympic Tin học Quốc gia khi còn là học sinh.
                        </div>
                    </div>
                    
                    <!-- Thạc sĩ 4 -->
                    <div class="student-card">
                        <i class="fas fa-user-graduate student-icon"></i>
                        <img src="https://i.postimg.cc/fRYGqFzc/Chat-GPT-Image-Oct-20-2025-08-20-23-PM.png" alt="Thạc sĩ Lê Thị Hương" class="student-image">
                        <h3>ThS. Lê Thị Hương</h3>
                        <div class="student-nienkhoa">Niên khoá 2008-2012</div>
                        <div class="achievement-badge">ThS. Quản trị Kinh doanh</div>
                        <div class="student-details">
                            <strong>Học vấn:</strong> Tốt nghiệp Thạc sĩ Quản trị Kinh doanh tại Đại học Kinh tế Quốc dân.<br>
                            <strong>Kinh nghiệm:</strong> 7 năm làm việc trong lĩnh vực tài chính ngân hàng.<br>
                            <strong>Hiện nay:</strong> Trưởng phòng Kinh doanh tại Ngân hàng Techcombank chi nhánh Đắk Lắk.<br>
                            <strong>Thành tích:</strong> Đạt học bổng toàn phần cho chương trình thạc sĩ, từng là học sinh giỏi cấp tỉnh môn Văn.
                        </div>
                    </div>
                    
                    <!-- Thạc sĩ 5 -->
                    <div class="student-card">
                        <i class="fas fa-user-graduate student-icon"></i>
                        <img src="https://i.postimg.cc/2Sns9JkF/Chat-GPT-Image-Oct-20-2025-08-20-11-PM.png" alt="Thạc sĩ Phạm Quang Minh" class="student-image">
                        <h3>ThS. Phạm Quang Minh</h3>
                        <div class="student-nienkhoa">Niên khoá 2010-2014</div>
                        <div class="achievement-badge">ThS. Kỹ thuật Xây dựng</div>
                        <div class="student-details">
                            <strong>Học vấn:</strong> Tốt nghiệp Thạc sĩ Kỹ thuật Xây dựng tại Đại học Xây dựng Hà Nội.<br>
                            <strong>Kinh nghiệm:</strong> 6 năm làm việc trong các dự án xây dựng cầu đường.<br>
                            <strong>Hiện nay:</strong> Kỹ sư trưởng tại Công ty CP Xây dựng 47, phụ trách các dự án giao thông tại Tây Nguyên.<br>
                            <strong>Thành tích:</strong> Đạt giải Khuyến khích Olympic Vật lý cấp tỉnh khi còn là học sinh.
                        </div>
                    </div>
                    
                    <!-- Thạc sĩ 6 -->
                    <div class="student-card">
                        <i class="fas fa-user-graduate student-icon"></i>
                        <img src="https://i.postimg.cc/fRYGqFzc/Chat-GPT-Image-Oct-20-2025-08-20-23-PM.png" alt="Thạc sĩ Nguyễn Thị Lan" class="student-image">
                        <h3>ThS. Nguyễn Thị Lan</h3>
                        <div class="student-nienkhoa">Niên khoá 2009-2013</div>
                        <div class="achievement-badge">ThS. Y học</div>
                        <div class="student-details">
                            <strong>Học vấn:</strong> Tốt nghiệp Thạc sĩ Y học tại Đại học Y Dược TP.HCM.<br>
                            <strong>Kinh nghiệm:</strong> 5 năm làm việc tại Bệnh viện Đa khoa tỉnh Đắk Lắk.<br>
                            <strong>Hiện nay:</strong> Bác sĩ chuyên khoa Nội tổng quát tại Bệnh viện Đa khoa vùng Tây Nguyên.<br>
                            <strong>Thành tích:</strong> Đạt giải Nhất học sinh giỏi cấp tỉnh môn Sinh học, từng tham gia đội tuyển quốc gia.
                        </div>
                    </div>
                    
                    <!-- Thạc sĩ 7 -->
                    <div class="student-card">
                        <i class="fas fa-user-graduate student-icon"></i>
                        <img src="https://i.postimg.cc/2Sns9JkF/Chat-GPT-Image-Oct-20-2025-08-20-11-PM.png" alt="Thạc sĩ Hoàng Văn Tùng" class="student-image">
                        <h3>ThS. Hoàng Văn Tùng</h3>
                        <div class="student-nienkhoa">Niên khoá 2006-2010</div>
                        <div class="achievement-badge">ThS. Luật học</div>
                        <div class="student-details">
                            <strong>Học vấn:</strong> Tốt nghiệp Thạc sĩ Luật học tại Học viện Tư pháp.<br>
                            <strong>Kinh nghiệm:</strong> 9 năm hành nghề luật sư.<br>
                            <strong>Hiện nay:</strong> Luật sư thành viên tại Văn phòng Luật sư Hoàng Hà, chuyên về luật dân sự và kinh doanh.<br>
                            <strong>Thành tích:</strong> Đạt giải Ba học sinh giỏi cấp tỉnh môn Lịch sử, có nhiều đóng góp trong các hoạt động Đoàn trường.
                        </div>
                    </div>
                    
                    <!-- Thạc sĩ 8 -->
                    <div class="student-card">
                        <i class="fas fa-user-graduate student-icon"></i>
                        <img src="https://i.postimg.cc/fRYGqFzc/Chat-GPT-Image-Oct-20-2025-08-20-23-PM.png" alt="Thạc sĩ Vũ Thị Hồng" class="student-image">
                        <h3>ThS. Vũ Thị Hồng</h3>
                        <div class="student-nienkhoa">Niên khoá 2012-2016</div>
                        <div class="achievement-badge">ThS. Ngôn ngữ Anh</div>
                        <div class="student-details">
                            <strong>Học vấn:</strong> Tốt nghiệp Thạc sĩ Ngôn ngữ Anh tại Đại học Ngoại ngữ - ĐHQG Hà Nội.<br>
                            <strong>Kinh nghiệm:</strong> 4 năm giảng dạy tiếng Anh tại các trung tâm ngoại ngữ.<br>
                            <strong>Hiện nay:</strong> Giảng viên tiếng Anh tại Trường Cao đẳng Sư phạm Đắk Lắk.<br>
                            <strong>Thành tích:</strong> Đạt giải Nhì học sinh giỏi cấp tỉnh môn Tiếng Anh, có chứng chỉ IELTS 8.0.
                        </div>
                    </div>
                </div>
                
                <!-- Back to Honor Board Button -->
                <div class="back-to-board-section">
                    <a href="https://stemprojectaccount.github.io/BANG-VINH-DANH/" class="back-to-board-button">
                        <i class="fas fa-home button-icon"></i>
                        <div class="button-text">QUAY LẠI</div>
                    </a>
                </div>
            </div>
        </div>
    </div>
        
    <script>
        // ===== TẠO HIỆU ỨNG NỀN =====
        function createParticles() {
            const particlesContainer = document.getElementById('particles');
            const particleCount = 50;
            
            for (let i = 0; i < particleCount; i++) {
                const particle = document.createElement('div');
                particle.classList.add('particle');
                
                const size = Math.random() * 100 + 20;
                particle.style.width = `${size}px`;
                particle.style.height = `${size}px`;
                particle.style.left = `${Math.random() * 100}vw`;
                particle.style.animationDuration = `${Math.random() * 30 + 20}s`;
                particle.style.animationDelay = `${Math.random() * 5}s`;
                
                particlesContainer.appendChild(particle);
            }
        }
        
        function createFloatingElements() {
            const container = document.getElementById('floatingElements');
            const elementCount = 15;
            
            for (let i = 0; i < elementCount; i++) {
                const element = document.createElement('div');
                element.classList.add('floating-element');
                
                const size = Math.random() * 150 + 50;
                element.style.width = `${size}px`;
                element.style.height = `${size}px`;
                element.style.left = `${Math.random() * 100}vw`;
                element.style.animationDuration = `${Math.random() * 40 + 30}s`;
                element.style.animationDelay = `${Math.random() * 10}s`;
                
                container.appendChild(element);
            }
        }

        // ===== KHỞI TẠO TRANG =====
        document.addEventListener('DOMContentLoaded', function() {
            createParticles();
            createFloatingElements();
            
            console.log("=== TRANG THẠC SĨ - TIẾN SĨ ===");
            console.log("Hiển thị danh sách các thạc sĩ và tiến sĩ");
            console.log("Có nút QUAY LẠI TRANG BẢNG VINH DANH");
        });
    </script>
</body>
</html>
