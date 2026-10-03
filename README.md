<svg width="100%" height="320" viewBox="0 0 800 320" xmlns="http://www.w3.org/2000/svg" style="background: radial-gradient(circle at 50% 50%, #0d0f18 0%, #05060b 100%); border-radius: 12px; box-shadow: 0 8px 32px rgba(121, 40, 202, 0.2);">
  <defs>
    <!-- Glow filters -->
    <filter id="glow" x="-20%" y="-20%" width="140%" height="140%">
      <feGaussianBlur />
      <feComposite in="SourceGraphic" in2="blur" operator="over" />
    </filter>
    <filter id="spark-glow">
      <feGaussianBlur />
      
        
        
      
    </filter>
    <!-- Gradients -->
    <radialGradient id="saturn-grad" cx="30%" cy="30%" r="70%">
      <stop offset="0%" stop-color="#f39c12" />
      <stop offset="60%" stop-color="#d35400" />
      <stop offset="100%" stop-color="#78281f" />
    </radialGradient>
    <radialGradient id="jupiter-grad" cx="40%" cy="30%" r="70%">
      <stop offset="0%" stop-color="#e67e22" />
      <stop offset="40%" stop-color="#d35400" />
      <stop offset="80%" stop-color="#873600" />
      <stop offset="100%" stop-color="#512e5f" />
    </radialGradient>
    <radialGradient id="flash-grad" cx="50%" cy="50%" r="50%">
      <stop offset="0%" stop-color="#ffffff" />
      <stop offset="40%" stop-color="#3498db" />
      <stop offset="80%" stop-color="#9b59b6" />
      <stop offset="100%" stop-color="transparent" />
    </radialGradient>
  </defs>

  

  <!-- Starfield Layer -->
  <g>
    <circle class="star" cx="100" cy="60" r="1.5" />
    <circle class="star" cx="250" cy="40" r="2" />
    <circle class="star" cx="700" cy="80" r="1" />
    <circle class="star" cx="650" cy="250" r="2.5" />
    <circle class="star" cx="150" cy="270" r="1.5" />
    <circle class="star" cx="400" cy="40" r="1.2" />
    <circle class="star" cx="350" cy="280" r="2" />
    <circle class="star" cx="550" cy="60" r="1.8" />
  </g>

  <!-- Central Scene Anchor -->
  <g transform="translate(400, 160)">
    
    <!-- Shockwave / Flash on Impact -->
    <circle class="collision-flash" cx="0" cy="0" r="60" fill="url(#flash-grad)" filter="url(#glow)" />

    <!-- Saturn-like Planet System (Approaching from Left) -->
    <g class="planet-saturn">
      <!-- Back Ring Arc -->
      <path d="M -70 -15 C -70 20, 70 20, 70 -15" stroke="#d4ac0d" stroke-width="4" fill="none" opacity="0.6" stroke-dasharray="3 1" />
      <!-- Planet Body -->
      <circle cx="0" cy="0" r="38" fill="url(#saturn-grad)" filter="url(#glow)" />
      <!-- Front Ring Arc -->
      <path d="M 70 -15 C 70 -35, -70 -35, -70 -15" stroke="#f1c40f" stroke-width="8" stroke-linecap="round" fill="none" filter="url(#glow)" />
    </g>

    <!-- Jupiter-like Planet System (Approaching from Right) -->
    <g class="planet-jupiter">
      <!-- Planet Body -->
      <circle cx="0" cy="0" r="45" fill="url(#jupiter-grad)" filter="url(#glow)" />
      <!-- Atmospheric Storm Bands -->
      <path d="M -35 -15 Q 0 -5 35 -15" stroke="#b9770e" stroke-width="3" fill="none" opacity="0.6" />
      <path d="M -40 10 Q 0 20 40 10" stroke="#78281f" stroke-width="4" fill="none" opacity="0.5" />
      <path d="M -25 25 Q 0 32 25 25" stroke="#b9770e" stroke-width="2" fill="none" opacity="0.7" />
    </g>

    <!-- Collision Sparks / Debris Particles -->
    <g>
      <circle class="debris" cx="0" cy="0" r="3" fill="#00ffff" filter="url(#spark-glow)" style="--dx: -90px; --dy: -40px;" />
      <circle class="debris" cx="0" cy="0" r="4" fill="#ff7675" filter="url(#spark-glow)" style="--dx: 110px; --dy: -60px;" />
      <circle class="debris" cx="0" cy="0" r="2.5" fill="#ffeaa7" filter="url(#spark-glow)" style="--dx: -70px; --dy: 70px;" />
      <circle class="debris" cx="0" cy="0" r="3.5" fill="#a29bfe" filter="url(#spark-glow)" style="--dx: 80px; --dy: 50px;" />
      <circle class="debris" cx="0" cy="0" r="2" fill="#55efc4" filter="url(#spark-glow)" style="--dx: -130px; --dy: 10px;" />
      <circle class="debris" cx="0" cy="0" r="3" fill="#fab1a0" filter="url(#spark-glow)" style="--dx: 130px; --dy: -10px;" />
    </g>

  </g>
</svg>
