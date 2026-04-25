<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>XI-TKJ 1 - Animasi Premium</title>

<!-- Bootstrap 5 (Update) -->
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
<!-- Font Awesome 6 -->
<link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet">
<!-- Google Fonts -->
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Poppins', sans-serif;
    overflow-x: hidden;
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    min-height: 100vh;
}

/* 🔥 PARTICLE BACKGROUND */
#particles {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: -1;
    opacity: 0.3;
}

/* Navbar Glassmorphism */
.navbar {
    background: rgba(76, 73, 73, 0.95) !important;
    backdrop-filter: blur(20px);
    box-shadow: 0 8px 32px rgba(0,0,0,0.3);
    transition: all 0.3s ease;
    padding: 1rem 0;
}

.navbar.scrolled {
    background: rgba(76, 73, 73, 0.98) !important;
    padding: 0.5rem 0;
}

.navbar-brand {
    font-weight: 700 !important;
    font-size: 1.5rem !important;
    background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    animation: glow 2s ease-in-out infinite alternate;
}

@keyframes glow {
    from { filter: drop-shadow(0 0 5px #ff6b6b); }
    to { filter: drop-shadow(0 0 20px #4ecdc4); }
}

.nav-link {
    position: relative;
    transition: all 0.3s ease;
}

.nav-link::after {
    content: '';
    position: absolute;
    width: 0;
    height: 2px;
    bottom: -5px;
    left: 0;
    background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
    transition: width 0.3s ease;
}

.nav-link:hover::after {
    width: 100%;
}

/* Hero Slider Enhanced */
.carousel-item img {
    height: 500px;
    object-fit: cover;
    filter: brightness(0.7);
    transition: transform 0.5s ease;
}

.carousel-item:hover img {
    transform: scale(1.05);
}

.carousel-control-prev, .carousel-control-next {
    width: 5%;
    opacity: 0.8;
}

/* ✨ SCROLL ANIMATIONS */
.fade-in-up {
    opacity: 0;
    transform: translateY(50px);
    transition: all 0.8s ease-out;
}

.fade-in-up.visible {
    opacity: 1;
    transform: translateY(0);
}

/* Card Animations */
.card {
    background: rgba(255,255,255,0.95) !important;
    backdrop-filter: blur(10px);
    border: none;
    border-radius: 20px;
    transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
    overflow: hidden;
    position: relative;
    box-shadow: 0 10px 30px rgba(0,0,0,0.2);
}

.card::before {
    content: '';
    position: absolute;
    top: 0;
    left: -100%;
    width: 100%;
    height: 100%;
    background: linear-gradient(90deg, transparent, rgba(255,255,255,0.4), transparent);
    transition: left 0.5s;
}

.card:hover::before {
    left: 100%;
}

.card:hover {
    transform: translateY(-15px) scale(1.05) rotateX(5deg);
    box-shadow: 0 25px 50px rgba(0,0,0,0.3);
}

.card img {
    transition: all 0.3s ease;
    border-radius: 15px;
}

.card:hover img {
    transform: scale(1.1);
}

/* Floating Animation for Menu Cards */
.card-menu {
    animation: float 6s ease-in-out infinite;
}

.card-menu:nth-child(1) { animation-delay: 0s; }
.card-menu:nth-child(2) { animation-delay: 1s; }
.card-menu:nth-child(3) { animation-delay: 2s; }
.card-menu:nth-child(4) { animation-delay: 3s; }

@keyframes float {
    0%, 100% { transform: translateY(0px); }
    50% { transform: translateY(-10px); }
}

/* Typing Effect */
.typing {
    overflow: hidden;
    border-right: 3px solid #ff6b6b;
    white-space: nowrap;
    animation: typing 3s steps(40, end), blink-caret 0.75s step-end infinite;
}

@keyframes typing {
    from { width: 0; }
    to { width: 100%; }
}

@keyframes blink-caret {
    from, to { border-color: transparent; }
    50% { border-color: #ff6b6b; }
}

/* Footer */
footer {
    background: rgba(0,0,0,0.9) !important;
    backdrop-filter: blur(20px);
}

/* Responsive */
@media (max-width: 768px) {
    .carousel-item img { height: 300px; }
    body { margin-top: 70px; }
}
</style>
</head>

<body>
<!-- 🔥 PARTICLE BACKGROUND -->
<canvas id="particles"></canvas>

<!-- NAVBAR -->
<nav class="navbar navbar-expand-lg navbar-dark fixed-top">
<div class="container">
<a class="navbar-brand" href="X-TKJ 1.html"><i class="fas fa-graduation-cap"></i> XI-TKJ 1</a>
<button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#menu">
<span class="navbar-toggler-icon"></span>
</button>
<div class="collapse navbar-collapse" id="menu">
<ul class="navbar-nav ms-auto">
<li class="nav-item"><a class="nav-link" href="#"><i class="fas fa-home"></i> BERANDA</a></li>
<li class="nav-item"><a class="nav-link" href="tentang.html"><i class="fas fa-info-circle"></i> TENTANG</a></li>
<li class="nav-item"><a class="nav-link" href="Galeri.html"><i class="fas fa-images"></i> GALERI</a></li>
<li class="nav-item"><a class="nav-link" href="cerita.html"><i class="fas fa-book"></i> CERITA</a></li>
</ul>
</div>
</div>
</nav>

<!-- SLIDER -->
<div id="slider" class="carousel slide carousel-fade" data-bs-ride="carousel" style="margin-top: 80px;">
<div class="carousel-indicators">
<button type="button" data-bs-target="#slider="0" class="active"></button>
<button type="button" data-bs-target="#slider" data-bs-slide-to="1"></button>
</div>
<div class="carousel-inner">
<div class="carousel-item active">
<img src="https://picsum.photos/1400/600?1" class="d-block w-100" alt="Slide 1">
<div class="carousel-caption d-none d-md-block">
<h1 class="typing">Selamat Datang di <strong>XI-TKJ 1</strong></h1>
<p>Kelas Teknik Komputer dan Jaringan Terbaik</p>
</div>
</div>
<div class="carousel-item">
<img src="https://picsum.photos/1400/600?2" class="d-block w-100" alt="Slide 2">
<div class="carousel-caption d-none d-md-block">
<h1 class="typing">Future is Here</h1>
<p>Membangun Generasi IT Masa Depan</p>
</div>
</div>
</div>
<a class="carousel-control-prev" href="#slider" role="button" data-bs-slide="prev">
<span class="carousel-control-prev-icon" aria-hidden="true"></span>
</a>
<a class="carousel-control-next" href="#slider" role="button" data-bs-slide="next">
<span class="carousel-control-next-icon" aria-hidden="true"></span>
</a>
</div>

<!-- MENU -->
<div class="container mt-5 mb-5">
<div class="row justify-content-center">
<div class="col-md-8 text-center fade-in-up">
<h2 class="display-5 mb-4"><i class="fas fa-chalkboard-teacher"></i> TENTANG KELAS</h2>
<p class="lead mb-5">kelas Teknik Komputer dan Jaringan favorit Anda</p>
</div>
</div>

<div class="row text-center">
<a href="X - TKJ 1.html" class="col-md-3 col-sm-6 mb-4">
<div class="card card-menu shadow-lg fade-in-up">
<i class="fas fa-arrow-left fa-2x mb-3 text-primary"></i>
<h5>X-TKJ 1</h5>
</div>
</a>


<div class="col-md-3 col-sm-6 mb-4">
    <a href="XI - TKJ 1.html" style="text-decoration: none; color: inherit;">
        <div class="card card-menu shadow-lg fade-in-up">
            <i class="fas fa-laptop-code fa-2x mb-3 text-success"></i>
            <h5>XI-TKJ 1</h5>
        </div>
    </a>
</div>


<div class="col-md-3 col-sm-6 mb-4">
<div class="card card-menu shadow-lg fade-in-up">
<i class="fas fa-graduation-cap fa-2x mb-3 text-warning"></i>
<h5>XII-TKJ 1</h5>
</div>
</div>

<div class="col-md-3 col-sm-6 mb-4">
    <a href="Galeri.html" style="text-decoration: none; color: inherit;">
        <div class="card card-menu shadow-lg fade-in-up">
            <i class="fas fa-images fa-2x mb-3 text-info"></i>
            <h5>GALERI
        </div>
    </a>
</div>

<!-- BERITA -->
<div class="container-fluid py-5" style="background: rgba(255,255,255,0.1);">
<div class="container">
<div class="row justify-content-center">
<div class="col-md-8 text-center mb-5 fade-in-up">
<h2 class="display-5"><i class="fas fa-newspaper"></i> Cerita Terbaru</h2>
</div>
</div>

<div class="row">
<div class="col-md-6 mb-4">
<div class="card h-100 shadow-lg fade-in-up">
<img src="https://picsum.photos/500/300?3" class="card-img-top" alt="Berita 1">
<div class="card-body">
<h5 class="card-title">Lomba Lomba Yang di Ikuti</h5>
<p class="card-text">Lomba nya cuma juan yg jgo</p>
<a href="#" class="btn btn-primary">Baca Selengkapnya <i class="fas fa-arrow-right"></i></a>
</div>
</div>
</div>

<div class="col-md-6 mb-4">
<div class="card h-100 shadow-lg fade-in-up">
<img src="https://picsum.photos/500/300?4" class="card-img-top" alt="Berita 2">
<div class="card-body">
<h5 class="card-title">Workshop Jaringan Cisco</h5>
<p class="card-text">Kelas XI-TKJ 1 mengikuti workshop CCNA...</p>
<a href="#" class="btn btn-success">Baca Selengkapnya <i class="fas fa-arrow-right"></i></a>
</div>
</div>
</div>
</div>
</div>
</div>

<!-- FOOTER -->
<footer class="bg-dark text-white text-center py-4 mt-5">
<div class="container">
<p><i class="fas fa-heart text-danger"></i> @ 2026 XI-TKJ 1 - Teknik Komputer & Jaringan</p>
<p class="small">Made with ❤️ by bg Aljuan</p>
</div>
</footer>

<!-- Bootstrap 5 JS -->
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>

<script>
/* 🔥 PARTICLE SYSTEM */
const canvas = document.getElementById('particles');
const ctx = canvas.getContext('2d');

canvas.width = window.innerWidth;
canvas.height = window.innerHeight;

const particles = [];
const particleCount = 80;

class Particle {
    constructor() {
        this.x = Math.random() * canvas.width;
        this.y = Math.random() * canvas.height;
        this.size = Math.random() * 2 + 1;
        this.speedX = Math.random() * 0.3 - 0.15;
        this.speedY = Math.random() * 0.3 - 0.15;
        this.hue = Math.random() * 60 + 200; // Cyan to Blue
    }
    update() {
        this.x += this.speedX;
        this.y += this.speedY;
        if (this.x > canvas.width || this.x < 0) this.speedX *= -1;
        if (this.y > canvas.height || this.y < 0) this.speedY *= -1;
    }
    draw() {
        ctx.fillStyle = `hsl(${this.hue}, 70%, 60%)`;
        ctx.beginPath();
        ctx.arc(this.x, this.y, this.size, 0, Math.PI * 2);
        ctx.fill();
        ctx.shadowBlur = 10;
        ctx.shadowColor = `hsl(${this.hue}, 70%, 60%)`;
    }
}

for(let i = 0; i < particleCount; i++) {
    particles.push(new Particle());
}

function animateParticles() {
    ctx.fillStyle = 'rgba(102, 126, 234, 0.05)';
    ctx.fillRect(0, 0, canvas.width, canvas.height);
    
    particles.forEach(p => {
        p.update();
        p.draw();
    });
    requestAnimationFrame(animateParticles);
}
animateParticles();

window.addEventListener('resize', () => {
    canvas.width = window.innerWidth;
    canvas.height = window.innerHeight;
});

/* Navbar Scroll Effect */
window.addEventListener('scroll', () => {
    const navbar = document.querySelector('.navbar');
    if(window.scrollY > 50) {
        navbar.classList.add('scrolled');
    } else {
        navbar.classList.remove('scrolled');
    }
});

/* ✨ SCROLL ANIMATIONS */
const observerOptions = {
    threshold: 0.1,
    rootMargin: '0px 0px -50px 0px'
};

const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
        if(entry.isIntersecting) {
            entry.target.classList.add('visible');
        }
    });
}, observerOptions);

document.querySelectorAll('.fade-in-up').forEach(el => {
    observer.observe(el);
});

/* Typing Animation Reset */
const typingElements = document.querySelectorAll('.typing');
typingElements.forEach((el, index) => {
    setTimeout(() => {
        el.classList.add('typing');
    }, index * 1000);
});
</script>

</body>
</html>
