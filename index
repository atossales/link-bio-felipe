<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Felipe Martins | Reallizi</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    :root {
      --blue-deep: #0A1628;
      --blue-primary: #1A56DB;
      --blue-brand: #2563EB;
      --blue-light: #3B82F6;
      --blue-glow: #60A5FA;
      --orange-accent: #F97316;
      --orange-bright: #FB923C;
      --white: #FFFFFF;
      --gray-light: #E2E8F0;
      --green-whatsapp: #25D366;
    }

    html, body {
      min-height: 100vh;
      font-family: 'Plus Jakarta Sans', sans-serif;
      background: var(--blue-deep);
      color: var(--white);
      overflow-x: hidden;
    }

    body {
      display: flex;
      justify-content: center;
      align-items: flex-start;
      padding: 0;
    }

    /* Background effects */
    .bg-effects {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      pointer-events: none;
      z-index: 0;
      overflow: hidden;
    }

    .bg-effects::before {
      content: '';
      position: absolute;
      top: -30%;
      left: 50%;
      transform: translateX(-50%);
      width: 600px;
      height: 600px;
      background: radial-gradient(circle, rgba(37, 99, 235, 0.25) 0%, rgba(37, 99, 235, 0.08) 40%, transparent 70%);
      border-radius: 50%;
    }

    .bg-effects::after {
      content: '';
      position: absolute;
      bottom: -20%;
      left: 50%;
      transform: translateX(-50%);
      width: 500px;
      height: 500px;
      background: radial-gradient(circle, rgba(249, 115, 22, 0.1) 0%, transparent 60%);
      border-radius: 50%;
    }

    .bg-grid {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-image: 
        linear-gradient(rgba(37, 99, 235, 0.03) 1px, transparent 1px),
        linear-gradient(90deg, rgba(37, 99, 235, 0.03) 1px, transparent 1px);
      background-size: 40px 40px;
      pointer-events: none;
      z-index: 0;
    }

    /* Container */
    .container {
      position: relative;
      z-index: 1;
      width: 100%;
      max-width: 440px;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 40px 20px 60px;
    }

    /* Profile section */
    .profile-section {
      display: flex;
      flex-direction: column;
      align-items: center;
      margin-bottom: 36px;
      animation: fadeInDown 0.8s ease-out;
    }

    .photo-wrapper {
      position: relative;
      width: 140px;
      height: 140px;
      margin-bottom: 20px;
    }

    .photo-ring {
      position: absolute;
      inset: -4px;
      border-radius: 50%;
      background: linear-gradient(135deg, var(--blue-brand), var(--orange-accent));
      animation: ringPulse 3s ease-in-out infinite;
    }

    .photo-ring-outer {
      position: absolute;
      inset: -12px;
      border-radius: 50%;
      border: 1px solid rgba(37, 99, 235, 0.2);
      animation: ringPulse 3s ease-in-out infinite 0.5s;
    }

    .photo {
      position: relative;
      width: 140px;
      height: 140px;
      border-radius: 50%;
      overflow: hidden;
      border: 3px solid var(--blue-deep);
      z-index: 1;
    }

    .photo img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      object-position: center top;
    }

    .verified-badge {
      position: absolute;
      bottom: 4px;
      right: 4px;
      width: 32px;
      height: 32px;
      background: var(--blue-brand);
      border-radius: 50%;
      border: 3px solid var(--blue-deep);
      display: flex;
      align-items: center;
      justify-content: center;
      z-index: 2;
    }

    .verified-badge svg {
      width: 16px;
      height: 16px;
      fill: white;
    }

    .profile-name {
      font-size: 22px;
      font-weight: 800;
      letter-spacing: -0.02em;
      margin-bottom: 4px;
    }

    .profile-handle {
      font-size: 14px;
      color: var(--blue-glow);
      font-weight: 500;
      margin-bottom: 10px;
      opacity: 0.8;
    }

    .profile-tagline {
      font-size: 14px;
      color: var(--gray-light);
      text-align: center;
      line-height: 1.5;
      max-width: 320px;
      opacity: 0.7;
    }

    .profile-tagline strong {
      color: var(--white);
      opacity: 1;
    }

    /* Links section */
    .links-section {
      width: 100%;
      display: flex;
      flex-direction: column;
      gap: 14px;
    }

    .link-card {
      position: relative;
      display: flex;
      align-items: center;
      width: 100%;
      padding: 16px 20px;
      border-radius: 16px;
      text-decoration: none;
      color: var(--white);
      transition: all 0.35s cubic-bezier(0.4, 0, 0.2, 1);
      overflow: hidden;
      cursor: pointer;
    }

    /* Gradient border */
    .link-card::before {
      content: '';
      position: absolute;
      inset: 0;
      border-radius: 16px;
      padding: 1px;
      background: linear-gradient(135deg, rgba(37, 99, 235, 0.4), rgba(37, 99, 235, 0.1));
      -webkit-mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
      mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
      -webkit-mask-composite: xor;
      mask-composite: exclude;
      transition: all 0.35s ease;
    }

    /* Shimmer sweep effect */
    .link-card::after {
      content: '';
      position: absolute;
      top: 0;
      left: -100%;
      width: 60%;
      height: 100%;
      background: linear-gradient(90deg, transparent, rgba(255,255,255,0.06), transparent);
      z-index: 2;
      pointer-events: none;
      transition: none;
    }

    .link-card:hover::after {
      animation: shimmerSweep 0.7s ease-out forwards;
    }

    .link-card-bg {
      position: absolute;
      inset: 0;
      background: linear-gradient(135deg, rgba(26, 86, 219, 0.15), rgba(10, 22, 40, 0.8));
      backdrop-filter: blur(12px);
      border-radius: 16px;
      z-index: 0;
      transition: all 0.35s ease;
    }

    /* Hover glow shadow */
    .link-card:hover {
      transform: translateY(-4px) scale(1.02);
      box-shadow: 0 8px 30px rgba(37, 99, 235, 0.2), 0 0 0 1px rgba(96, 165, 250, 0.15);
    }

    .link-card:hover::before {
      background: linear-gradient(135deg, rgba(96, 165, 250, 0.6), rgba(37, 99, 235, 0.3));
    }

    .link-card:hover .link-card-bg {
      background: linear-gradient(135deg, rgba(26, 86, 219, 0.3), rgba(10, 22, 40, 0.9));
    }

    .link-card:hover .link-arrow {
      transform: translateX(6px);
      opacity: 1;
    }

    .link-card:hover .link-icon {
      animation: iconBounce 0.5s cubic-bezier(0.4, 0, 0.2, 1);
      background: rgba(255, 255, 255, 0.15);
    }

    .link-card:hover .link-title {
      text-shadow: 0 0 20px rgba(96, 165, 250, 0.3);
    }

    .link-card:active {
      transform: translateY(0) scale(0.98);
      box-shadow: none;
      transition: all 0.1s ease;
    }

    /* Highlight card - simulador */
    .link-card.highlight {
      animation: fadeInUp 0.6s ease-out 0.1s both, highlightPulse 3s ease-in-out 1.5s infinite;
    }

    .link-card.highlight .link-card-bg {
      background: linear-gradient(135deg, var(--blue-brand), #1E40AF);
    }

    .link-card.highlight::before {
      background: linear-gradient(135deg, var(--blue-light), var(--blue-glow));
    }

    .link-card.highlight::after {
      animation: shimmerSweep 1.2s ease-out 2s;
    }

    .link-card.highlight:hover {
      box-shadow: 0 8px 40px rgba(37, 99, 235, 0.4), 0 0 60px rgba(37, 99, 235, 0.15);
      animation: none;
      transform: translateY(-4px) scale(1.02);
    }

    .link-card.highlight:hover::after {
      animation: shimmerSweep 0.7s ease-out forwards;
    }

    .link-card.highlight:hover .link-card-bg {
      background: linear-gradient(135deg, var(--blue-light), var(--blue-brand));
    }

    .link-icon {
      position: relative;
      z-index: 1;
      width: 44px;
      height: 44px;
      border-radius: 12px;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-right: 14px;
      flex-shrink: 0;
      background: rgba(255, 255, 255, 0.08);
      transition: all 0.35s ease;
    }

    .link-card.highlight .link-icon {
      background: rgba(255, 255, 255, 0.2);
    }

    .link-icon svg {
      width: 22px;
      height: 22px;
    }

    .link-content {
      position: relative;
      z-index: 1;
      flex: 1;
    }

    .link-title {
      font-size: 15px;
      font-weight: 700;
      letter-spacing: -0.01em;
      line-height: 1.3;
      transition: text-shadow 0.35s ease;
    }

    .link-subtitle {
      font-size: 12px;
      opacity: 0.6;
      margin-top: 2px;
      font-weight: 400;
    }

    .link-arrow {
      position: relative;
      z-index: 1;
      opacity: 0.5;
      transition: all 0.35s cubic-bezier(0.4, 0, 0.2, 1);
      flex-shrink: 0;
      margin-left: 8px;
    }

    .link-arrow svg {
      width: 18px;
      height: 18px;
    }

    /* Staggered animation */
    .link-card:nth-child(2) { animation: fadeInUp 0.6s ease-out 0.2s both; }
    .link-card:nth-child(3) { animation: fadeInUp 0.6s ease-out 0.3s both; }
    .link-card:nth-child(4) { animation: fadeInUp 0.6s ease-out 0.4s both; }
    .link-card:nth-child(5) { animation: fadeInUp 0.6s ease-out 0.5s both; }

    /* Footer */
    .footer {
      margin-top: 40px;
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 16px;
      animation: fadeInUp 0.6s ease-out 0.7s both;
    }

    .social-links {
      display: flex;
      gap: 12px;
    }

    .social-link {
      width: 40px;
      height: 40px;
      border-radius: 50%;
      background: rgba(37, 99, 235, 0.1);
      border: 1px solid rgba(37, 99, 235, 0.2);
      display: flex;
      align-items: center;
      justify-content: center;
      text-decoration: none;
      color: var(--blue-glow);
      transition: all 0.3s ease;
    }

    .social-link:hover {
      background: rgba(37, 99, 235, 0.25);
      transform: translateY(-2px);
    }

    .social-link svg {
      width: 18px;
      height: 18px;
    }

    .footer-brand {
      display: flex;
      align-items: center;
      gap: 6px;
      opacity: 0.3;
      font-size: 11px;
      font-weight: 500;
      letter-spacing: 0.05em;
    }

    .footer-brand svg {
      width: 14px;
      height: 14px;
    }

    /* Animations */
    @keyframes fadeInDown {
      from { opacity: 0; transform: translateY(-20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    @keyframes fadeInUp {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    @keyframes ringPulse {
      0%, 100% { opacity: 1; transform: scale(1); }
      50% { opacity: 0.6; transform: scale(1.03); }
    }

    @keyframes shimmerSweep {
      0% { left: -100%; }
      100% { left: 150%; }
    }

    @keyframes iconBounce {
      0% { transform: scale(1); }
      30% { transform: scale(0.85); }
      60% { transform: scale(1.15); }
      80% { transform: scale(0.95); }
      100% { transform: scale(1); }
    }

    @keyframes highlightPulse {
      0%, 100% { 
        box-shadow: 0 0 0 0 rgba(37, 99, 235, 0), 0 4px 15px rgba(37, 99, 235, 0.1);
      }
      50% { 
        box-shadow: 0 0 20px 4px rgba(37, 99, 235, 0.15), 0 4px 25px rgba(37, 99, 235, 0.2);
      }
    }

    /* Responsiveness */
    @media (max-width: 480px) {
      .container {
        padding: 32px 16px 48px;
      }

      .photo-wrapper {
        width: 120px;
        height: 120px;
      }

      .photo {
        width: 120px;
        height: 120px;
      }

      .profile-name {
        font-size: 20px;
      }

      .link-card {
        padding: 14px 16px;
      }

      .link-icon {
        width: 40px;
        height: 40px;
      }

      .link-title {
        font-size: 14px;
      }
    }
  </style>
</head>
<body>

  <div class="bg-effects"></div>
  <div class="bg-grid"></div>

  <div class="container">
    <!-- Profile -->
    <div class="profile-section">
      <div class="photo-wrapper">
        <div class="photo-ring-outer"></div>
        <div class="photo-ring"></div>
        <div class="photo">
          <img src="https://i.imgur.com/x7QBquN.png" alt="Felipe Martins">
        </div>
        <div class="verified-badge">
          <svg viewBox="0 0 24 24"><path d="M9 16.17L4.83 12l-1.42 1.41L9 19 21 7l-1.41-1.41z"/></svg>
        </div>
      </div>
      <div class="profile-name">Felipe Martins</div>
      <div class="profile-handle">@felipereallizi</div>
      <div class="profile-tagline">
        💰 Te ajudo a conseguir <strong>crédito de forma simplificada</strong>. Mesmo tendo restrição.
      </div>
    </div>

    <!-- Links -->
    <div class="links-section">

      <!-- Simulador - destaque -->
      <a href="https://simulador.reallizi.com.br" target="_blank" class="link-card highlight">
        <div class="link-card-bg"></div>
        <div class="link-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <rect x="4" y="2" width="16" height="20" rx="2"/>
            <line x1="8" y1="6" x2="16" y2="6"/>
            <line x1="8" y1="10" x2="16" y2="10"/>
            <line x1="8" y1="14" x2="12" y2="14"/>
          </svg>
        </div>
        <div class="link-content">
          <div class="link-title">Simulador de Crédito</div>
          <div class="link-subtitle">Descubra quanto você pode receber</div>
        </div>
        <div class="link-arrow">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <polyline points="9 18 15 12 9 6"/>
          </svg>
        </div>
      </a>

      <!-- Bolsa Família -->
      <a href="https://reallizi.com.br/bolsa-familia/69a74179e5e4fe775969fe95" target="_blank" class="link-card">
        <div class="link-card-bg"></div>
        <div class="link-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"/>
            <circle cx="9" cy="7" r="4"/>
            <path d="M23 21v-2a4 4 0 0 0-3-3.87"/>
            <path d="M16 3.13a4 4 0 0 1 0 7.75"/>
          </svg>
        </div>
        <div class="link-content">
          <div class="link-title">Empréstimo Bolsa Família</div>
          <div class="link-subtitle">Liberação rápida e sem burocracia</div>
        </div>
        <div class="link-arrow">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <polyline points="9 18 15 12 9 6"/>
          </svg>
        </div>
      </a>

      <!-- Consignado CLT -->
      <a href="https://reallizi.com.br/emprestimo-clt/69a741a0e5e4fe77596a0025" target="_blank" class="link-card">
        <div class="link-card-bg"></div>
        <div class="link-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <rect x="2" y="7" width="20" height="14" rx="2" ry="2"/>
            <path d="M16 21V5a2 2 0 0 0-2-2h-4a2 2 0 0 0-2 2v16"/>
          </svg>
        </div>
        <div class="link-content">
          <div class="link-title">Consignado CLT</div>
          <div class="link-subtitle">Desconto direto na folha de pagamento</div>
        </div>
        <div class="link-arrow">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <polyline points="9 18 15 12 9 6"/>
          </svg>
        </div>
      </a>

      <!-- Conta de Luz -->
      <a href="https://reallizi.com.br/emprestimo-conta-de-luz/69a7415e679a163895b13de2" target="_blank" class="link-card">
        <div class="link-card-bg"></div>
        <div class="link-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <polygon points="13 2 3 14 12 14 11 22 21 10 12 10 13 2"/>
          </svg>
        </div>
        <div class="link-content">
          <div class="link-title">Empréstimo pela Conta de Luz</div>
          <div class="link-subtitle">Crédito usando sua conta de energia</div>
        </div>
        <div class="link-arrow">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <polyline points="9 18 15 12 9 6"/>
          </svg>
        </div>
      </a>

      <!-- Garantia de Veículo -->
      <a href="https://reallizi.com.br/emprestimo-carro-garantia/69a741bcbe109a6b615c8935" target="_blank" class="link-card">
        <div class="link-card-bg"></div>
        <div class="link-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <path d="M5 17h14M5 17a2 2 0 0 1-2-2V7a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2v8a2 2 0 0 1-2 2M9 17v2m6-2v2"/>
            <circle cx="7.5" cy="17" r="0"/>
            <path d="M7 10l2 2 4-4"/>
          </svg>
        </div>
        <div class="link-content">
          <div class="link-title">Crédito com Garantia de Veículo</div>
          <div class="link-subtitle">Use seu carro como garantia</div>
        </div>
        <div class="link-arrow">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <polyline points="9 18 15 12 9 6"/>
          </svg>
        </div>
      </a>

    </div>

    <!-- Footer -->
    <div class="footer">
      <div class="social-links">
        <a href="https://www.instagram.com/felipereallizi" target="_blank" class="social-link" aria-label="Instagram">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <rect x="2" y="2" width="20" height="20" rx="5" ry="5"/>
            <path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"/>
            <line x1="17.5" y1="6.5" x2="17.51" y2="6.5"/>
          </svg>
        </a>
        <a href="https://www.reallizi.com.br" target="_blank" class="social-link" aria-label="Website">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <circle cx="12" cy="12" r="10"/>
            <line x1="2" y1="12" x2="22" y2="12"/>
            <path d="M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"/>
          </svg>
        </a>
      </div>
      <div class="footer-brand">
        <svg viewBox="0 0 24 24" fill="currentColor"><path d="M12 2L2 7l10 5 10-5-10-5zM2 17l10 5 10-5M2 12l10 5 10-5"/></svg>
        reallizi.com.br
      </div>
    </div>
  </div>

</body>
</html>
