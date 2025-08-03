<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Merge Magic - Enter the Portal</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;900&display=swap');
    
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    
    body {
      font-family: 'Inter', sans-serif;
      background: #0a0a0a;
      color: white;
      overflow-x: hidden;
      min-height: 100vh;
      position: relative;
      cursor: none;
    }
    
    /* Custom Cursor */
    .custom-cursor {
      position: fixed;
      width: 20px;
      height: 20px;
      background: radial-gradient(circle, #ff6b6b, #4ecdc4);
      border-radius: 50%;
      pointer-events: none;
      z-index: 9999;
      transition: transform 0.1s ease;
      mix-blend-mode: difference;
    }
    
    /* Animated Background */
    .bg-animation {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: 
        radial-gradient(ellipse at top left, rgba(255, 107, 107, 0.1) 0%, transparent 50%),
        radial-gradient(ellipse at top right, rgba(78, 205, 196, 0.1) 0%, transparent 50%),
        radial-gradient(ellipse at bottom left, rgba(255, 159, 243, 0.1) 0%, transparent 50%),
        radial-gradient(ellipse at bottom right, rgba(84, 160, 255, 0.1) 0%, transparent 50%),
        linear-gradient(135deg, #0a0a0a 0%, #1a1a2e 50%, #16213e 100%);
      animation: bgMove 20s ease-in-out infinite;
    }
    
    @keyframes bgMove {
      0%, 100% { transform: scale(1) rotate(0deg); }
      50% { transform: scale(1.1) rotate(2deg); }
    }
    
    /* Geometric Shapes */
    .geometric-bg {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      pointer-events: none;
      z-index: 1;
    }
    
    .shape {
      position: absolute;
      opacity: 0.1;
      animation: float 8s ease-in-out infinite;
    }
    
    .shape:nth-child(1) {
      top: 10%;
      left: 10%;
      width: 100px;
      height: 100px;
      background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
      clip-path: polygon(50% 0%, 0% 100%, 100% 100%);
      animation-delay: 0s;
    }
    
    .shape:nth-child(2) {
      top: 20%;
      right: 15%;
      width: 80px;
      height: 80px;
      background: linear-gradient(45deg, #54a0ff, #ff9ff3);
      border-radius: 50%;
      animation-delay: 2s;
    }
    
    .shape:nth-child(3) {
      bottom: 30%;
      left: 20%;
      width: 120px;
      height: 60px;
      background: linear-gradient(45deg, #5f27cd, #00d2d3);
      clip-path: polygon(25% 0%, 100% 0%, 75% 100%, 0% 100%);
      animation-delay: 4s;
    }
    
    .shape:nth-child(4) {
      bottom: 10%;
      right: 10%;
      width: 90px;
      height: 90px;
      background: linear-gradient(45deg, #ff9ff3, #54a0ff);
      clip-path: polygon(30% 0%, 70% 0%, 100% 30%, 100% 70%, 70% 100%, 30% 100%, 0% 70%, 0% 30%);
      animation-delay: 6s;
    }
    
    @keyframes float {
      0%, 100% { transform: translateY(0px) rotate(0deg); }
      50% { transform: translateY(-20px) rotate(180deg); }
    }
    
    /* Holographic Grid */
    .holo-grid {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-image: 
        linear-gradient(rgba(78, 205, 196, 0.03) 1px, transparent 1px),
        linear-gradient(90deg, rgba(78, 205, 196, 0.03) 1px, transparent 1px);
      background-size: 50px 50px;
      animation: gridMove 15s linear infinite;
      pointer-events: none;
      z-index: 1;
    }
    
    @keyframes gridMove {
      0% { transform: translate(0, 0); }
      100% { transform: translate(50px, 50px); }
    }
    
    .container {
      max-width: 600px;
      width: 90%;
      margin: 0 auto;
      padding: 60px 20px;
      text-align: center;
      position: relative;
      z-index: 10;
    }
    
    /* 3D Hero Card */
    .hero-card {
      background: rgba(255, 255, 255, 0.03);
      backdrop-filter: blur(20px);
      border: 1px solid rgba(255, 255, 255, 0.1);
      border-radius: 30px;
      padding: 50px 40px;
      margin-bottom: 40px;
      transform-style: preserve-3d;
      transition: transform 0.6s ease;
      position: relative;
      overflow: hidden;
    }
    
    .hero-card::before {
      content: '';
      position: absolute;
      top: 0;
      left: -100%;
      width: 100%;
      height: 100%;
      background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.1), transparent);
      transition: left 2s;
      animation: shine 3s ease-in-out infinite;
    }
    
    @keyframes shine {
      0% { left: -100%; }
      50% { left: 100%; }
      100% { left: 100%; }
    }
    
    .hero-card:hover {
      transform: rotateX(5deg) rotateY(5deg) translateZ(20px);
    }
    
    /* Holographic Title */
    .holo-title {
      font-size: 4.5em;
      font-weight: 900;
      background: linear-gradient(45deg, #ff6b6b, #4ecdc4, #54a0ff, #ff9ff3, #5f27cd);
      background-size: 400% 400%;
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      animation: holoShift 4s ease-in-out infinite, titleFloat 6s ease-in-out infinite;
      margin-bottom: 20px;
      text-shadow: 0 0 50px rgba(255, 107, 107, 0.5);
      position: relative;
    }
    
    .holo-title::after {
      content: '🧩 MERGE MAGIC 🧩';
      position: absolute;
      top: 0;
      left: 0;
      background: linear-gradient(45deg, #4ecdc4, #54a0ff);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      z-index: -1;
      transform: translate(3px, 3px);
      opacity: 0.3;
    }
    
    @keyframes holoShift {
      0%, 100% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
    }
    
    @keyframes titleFloat {
      0%, 100% { transform: translateY(0px) scale(1); }
      50% { transform: translateY(-10px) scale(1.02); }
    }
    
    .tagline {
      font-size: 1.5em;
      font-weight: 300;
      color: rgba(255, 255, 255, 0.8);
      margin-bottom: 40px;
      animation: fadeInUp 2s ease-out;
    }
    
    @keyframes fadeInUp {
      from {
        opacity: 0;
        transform: translateY(30px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }
    
    /* 3D Game Preview */
    .game-preview {
      perspective: 1000px;
      margin-bottom: 40px;
    }
    
    .preview-container {
      position: relative;
      transform-style: preserve-3d;
      transition: transform 0.6s ease;
    }
    
    .preview-container:hover {
      transform: rotateY(10deg) rotateX(5deg);
    }
    
    .game-image {
      width: 100%;
      border-radius: 25px;
      box-shadow: 
        0 20px 40px rgba(0, 0, 0, 0.3),
        0 0 80px rgba(255, 107, 107, 0.2);
      transition: all 0.6s ease;
      position: relative;
    }
    
    .preview-container:hover .game-image {
      box-shadow: 
        0 30px 60px rgba(0, 0, 0, 0.4),
        0 0 100px rgba(255, 107, 107, 0.4);
    }
    
    /* Morphing Features */
    .features-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 20px;
      margin-bottom: 40px;
    }
    
    .feature-morph {
      background: rgba(255, 255, 255, 0.05);
      backdrop-filter: blur(15px);
      border: 1px solid rgba(255, 255, 255, 0.1);
      border-radius: 20px;
      padding: 25px 20px;
      text-align: center;
      transition: all 0.6s cubic-bezier(0.175, 0.885, 0.32, 1.275);
      position: relative;
      overflow: hidden;
    }
    
    .feature-morph::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: linear-gradient(45deg, rgba(255, 107, 107, 0.1), rgba(78, 205, 196, 0.1));
      opacity: 0;
      transition: opacity 0.3s ease;
    }
    
    .feature-morph:hover::before {
      opacity: 1;
    }
    
    .feature-morph:hover {
      transform: translateY(-10px) scale(1.05);
      box-shadow: 0 20px 40px rgba(0, 0, 0, 0.2);
    }
    
    .feature-icon {
      font-size: 2.5em;
      margin-bottom: 15px;
      display: block;
      animation: iconPulse 2s ease-in-out infinite;
    }
    
    @keyframes iconPulse {
      0%, 100% { transform: scale(1); }
      50% { transform: scale(1.1); }
    }
    
    .feature-text {
      font-size: 0.95em;
      line-height: 1.4;
      position: relative;
      z-index: 1;
    }
    
    /* Quantum CTA Button */
    .quantum-cta {
      position: relative;
      display: inline-block;
      padding: 25px 50px;
      background: transparent;
      border: 2px solid #ff6b6b;
      border-radius: 50px;
      color: white;
      font-size: 1.4em;
      font-weight: 700;
      text-decoration: none;
      text-transform: uppercase;
      letter-spacing: 2px;
      transition: all 0.6s ease;
      overflow: hidden;
      animation: borderGlow 2s ease-in-out infinite alternate;
    }
    
    .quantum-cta::before {
      content: '';
      position: absolute;
      top: 0;
      left: -100%;
      width: 100%;
      height: 100%;
      background: linear-gradient(45deg, #ff6b6b, #4ecdc4, #54a0ff, #ff9ff3);
      transition: left 0.6s ease;
      z-index: -1;
    }
    
    .quantum-cta:hover::before {
      left: 0;
    }
    
    .quantum-cta:hover {
      transform: translateY(-5px);
      box-shadow: 0 15px 30px rgba(255, 107, 107, 0.4);
      border-color: transparent;
    }
    
    @keyframes borderGlow {
      from { box-shadow: 0 0 20px rgba(255, 107, 107, 0.5); }
      to { box-shadow: 0 0 30px rgba(255, 107, 107, 0.8), 0 0 40px rgba(78, 205, 196, 0.3); }
    }
    
    /* Neural Network Reviews */
    .neural-reviews {
      margin-top: 60px;
    }
    
    .review-neural {
      background: rgba(255, 255, 255, 0.02);
      backdrop-filter: blur(10px);
      border: 1px solid rgba(255, 255, 255, 0.1);
      border-radius: 20px;
      padding: 25px;
      margin-bottom: 20px;
      position: relative;
      transition: all 0.6s ease;
      animation: reviewFloat 8s ease-in-out infinite;
    }
    
    .review-neural:nth-child(even) {
      animation-delay: 2s;
    }
    
    .review-neural:nth-child(3) {
      animation-delay: 4s;
    }
    
    @keyframes reviewFloat {
      0%, 100% { transform: translateX(0); }
      50% { transform: translateX(10px); }
    }
    
    .review-neural:hover {
      transform: translateX(15px) !important;
      background: rgba(255, 255, 255, 0.05);
    }
    
    .review-stars {
      color: #ffd700;
      font-size: 1.3em;
      margin-bottom: 10px;
      animation: starTwinkle 3s ease-in-out infinite;
    }
    
    @keyframes starTwinkle {
      0%, 100% { opacity: 1; }
      50% { opacity: 0.7; }
    }
    
    .review-text {
      font-size: 1.1em;
      line-height: 1.5;
      margin-bottom: 10px;
    }
    
    .review-author {
      color: rgba(255, 255, 255, 0.6);
      font-style: italic;
    }
    
    /* Quantum Footer */
    .quantum-footer {
      margin-top: 60px;
      background: rgba(255, 255, 255, 0.02);
      backdrop-filter: blur(15px);
      border: 1px solid rgba(255, 255, 255, 0.1);
      border-radius: 25px;
      padding: 30px;
      position: relative;
      overflow: hidden;
    }
    
    .quantum-footer::before {
      content: '';
      position: absolute;
      top: -50%;
      left: -50%;
      width: 200%;
      height: 200%;
      background: conic-gradient(from 0deg, transparent, rgba(255, 107, 107, 0.03), transparent, rgba(78, 205, 196, 0.03), transparent);
      animation: quantumSpin 10s linear infinite;
    }
    
    @keyframes quantumSpin {
      0% { transform: rotate(0deg); }
      100% { transform: rotate(360deg); }
    }
    
    .footer-content {
      position: relative;
      z-index: 1;
      font-size: 1.1em;
      line-height: 1.6;
    }
    
    @media (max-width: 768px) {
      .holo-title { font-size: 3em; }
      .features-grid { grid-template-columns: 1fr; }
      .quantum-cta { font-size: 1.2em; padding: 20px 40px; }
      .hero-card { padding: 40px 25px; }
    }
  </style>
</head>
<body>
  <div class="custom-cursor"></div>
  <div class="bg-animation"></div>
  <div class="holo-grid"></div>
  
  <div class="geometric-bg">
    <div class="shape"></div>
    <div class="shape"></div>
    <div class="shape"></div>
    <div class="shape"></div>
  </div>

  <div class="container">
    <div class="hero-card">
      <h1 class="holo-title">🧩 MERGE MAGIC 🧩</h1>
      <p class="tagline">Enter a realm where reality bends to your imagination</p>
      
      <div class="game-preview">
        <div class="preview-container">
          <img src="https://i.pinimg.com/736x/72/21/7e/72217e2aa3c129705e8ee60eaa1f9539.jpg" alt="Merge Magic Portal" class="game-image" />
        </div>
      </div>
    </div>
    
    <div class="features-grid">
      <div class="feature-morph">
        <span class="feature-icon">🌟</span>
        <div class="feature-text">Quantum merging mechanics that defy physics</div>
      </div>
      <div class="feature-morph">
        <span class="feature-icon">🐉</span>
        <div class="feature-text">Evolve legendary creatures from stardust</div>
      </div>
      <div class="feature-morph">
        <span class="feature-icon">💎</span>
        <div class="feature-text">Exclusive rewards for dimensional travelers</div>
      </div>
      <div class="feature-morph">
        <span class="feature-icon">⚡</span>
        <div class="feature-text">Limited-time portal access available</div>
      </div>
    </div>
    
    <a href="https://installchecker.com/cl/i/dv6dmw
" class="quantum-cta" target="_blank">🎮 Play Now – It's Free</a>
    
    <div class="neural-reviews">
      <div class="review-neural">
        <div class="review-stars">✦ ✦ ✦ ✦ ✦</div>
        <div class="review-text">"This isn't just a game... it's a gateway to another dimension. I've been hooked for weeks and the magic never stops." </div>
        <div class="review-author">— Digital Explorer #4721</div>
      </div>
      <div class="review-neural">
        <div class="review-stars">✦ ✦ ✦ ✦ ✦</div>
        <div class="review-text">"The merging system is pure genius. Every combination creates something unexpected. It's like conducting a symphony of possibilities."</div>
        <div class="review-author">— Reality Architect</div>
      </div>
      <div class="review-neural">
        <div class="review-stars">✦ ✦ ✦ ✦ ✦</div>
        <div class="review-text">"I thought I knew mobile gaming... until I entered this portal. Absolutely mind-bending experience."</div>
        <div class="review-author">— Quantum Gamer</div>
      </div>
    </div>
    
    <div class="quantum-footer">
      <div class="footer-content">
        🚀 Instant portal access • Compatible across all dimensions<br>
        🔮 Secure reality bridge • Join 50M+ interdimensional travelers<br>
        ⭐ Zero signup required • Pure magic awaits within
      </div>
    </div>
  </div>

  <script>
    // Custom cursor follow
    const cursor = document.querySelector('.custom-cursor');
    
    document.addEventListener('mousemove', (e) => {
      cursor.style.left = e.clientX - 10 + 'px';
      cursor.style.top = e.clientY - 10 + 'px';
    });
    
    // Enhanced hover effects
    document.addEventListener('mouseenter', (e) => {
      if (e.target.matches('a, .feature-morph, .review-neural')) {
        cursor.style.transform = 'scale(2)';
      }
    });
    
    document.addEventListener('mouseleave', (e) => {
      if (e.target.matches('a, .feature-morph, .review-neural')) {
        cursor.style.transform = 'scale(1)';
      }
    });
    
    // Parallax effect on scroll
    window.addEventListener('scroll', () => {
      const scrolled = window.pageYOffset;
      const shapes = document.querySelectorAll('.shape');
      shapes.forEach((shape, index) => {
        const speed = 0.5 + (index * 0.1);
        shape.style.transform = `translateY(${scrolled * speed}px) rotate(${scrolled * 0.1}deg)`;
      });
    });
  </script>
</body>
</html>
