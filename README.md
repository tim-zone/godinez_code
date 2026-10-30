/* Base Resets & Typography */
* { 
    box-sizing: border-box; 
    margin: 0; 
    padding: 0; 
}

/* Smooth scrolling for anchor links */
html { 
    scroll-behavior: smooth; 
}

body { 
    font-family: 'Inter', -apple-system, sans-serif; 
    color: #333; 
    line-height: 1.6; 
    background-color: #fbfbfd; 
}

h1, h2, h3 { 
    font-family: 'Playfair Display', serif; 
}

/* Stop scrolling when landing screen is active */
body.no-scroll { 
    overflow: hidden; 
}

/* Landing / Loading Screen */
.landing-screen {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100vh;
    background-image: url('FB_IMG_1788141626612.jpg'); 
    background-size: cover;
    background-position: center;
    background-color: #0f1d30;
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    align-items: center;
    z-index: 9999;
    transition: opacity 0.6s ease, visibility 0.6s ease;
    padding-bottom: 80px;
}

.landing-screen.hidden {
    opacity: 0;
    visibility: hidden;
}

.landing-content {
    text-align: center;
    animation: fadeIn 1s ease 0.3s both; 
}

@keyframes fadeIn {
    from { opacity: 0; transform: translateY(15px); }
    to { opacity: 1; transform: translateY(0); }
}

.landing-content p {
    color: #ffffff;
    font-family: 'Inter', sans-serif;
    font-size: 1.1rem;
    margin-bottom: 20px;
    text-shadow: 0 2px 6px rgba(0,0,0,0.6); 
}

.explore-btn {
    background-color: #d1a553;
    color: #0f1d30;
    border: 2px solid #0f1d30;
    border-radius: 50px;
    padding: 14px 40px;
    font-family: 'Inter', sans-serif;
    font-size: 1.1rem;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.3s ease;
    box-shadow: 0 4px 15px rgba(0,0,0,0.4);
}

.explore-btn:hover {
    background-color: #dfb25e;
    transform: scale(1.03);
}

/* Core Colors */
.bg-navy { background-color: #0f1d30; color: #ffffff; }
.bg-navy-dark { background-color: #0a1422; color: #ffffff; }
.bg-white { background-color: #ffffff; }

/* Layout */
.container { 
    max-width: 1100px; 
    margin: 0 auto; 
    padding: 0 24px; 
    position: relative;
}
.section-padding { padding: 80px 0; }

/* Navigation */
.header-wrapper {
    background: #ffffff;
    position: relative;
    z-index: 1000;
    box-shadow: 0 2px 10px rgba(0,0,0,0.05);
}
nav { 
    display: flex; justify-content: space-between; align-items: center; 
    padding: 15px 0; 
}
.brand { display: flex; align-items: center; gap: 12px; }

.brand-logo { 
    width: 45px; 
    height: 45px; 
    object-fit: contain; 
    border-radius: 50%; 
    background-color: #0f1d30; 
}

.brand-text h1 { 
    font-size: 1.2rem; 
    margin: 0; 
    font-family: 'Playfair Display', serif; 
    color: #0f1d30; 
    font-weight: 700;
}
.brand-text p { font-size: 0.85rem; color: #6b7280; margin: 0; }
.menu-icon { font-size: 1.8rem; cursor: pointer; color: #0f1d30; user-select: none; }

/* Mobile Dropdown Menu */
.mobile-dropdown {
    position: absolute;
    top: 100%;
    left: 0;
    width: 100%;
    background: #ffffff;
    padding: 10px 24px 30px 24px;
    box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1);
    display: none; 
    flex-direction: column;
    border-top: 1px solid #f3f4f6;
}

.mobile-dropdown.active {
    display: flex; 
    animation: slideDown 0.3s ease forwards;
}

@keyframes slideDown {
    from { opacity: 0; transform: translateY(-10px); }
    to { opacity: 1; transform: translateY(0); }
}

.dropdown-links {
    list-style: none;
    width: 100%;
}

.dropdown-links li {
    border-bottom: 1px solid #e5e7eb;
}

.dropdown-links li a {
    display: block;
    padding: 16px 0;
    text-decoration: none;
    color: #0f1d30;
    font-weight: 500;
    font-size: 1rem;
}

.dropdown-apply-btn {
    background-color: #d1a553;
    color: #0f1d30;
    text-align: left;
    padding: 16px;
    border-radius: 8px;
    text-decoration: none;
    font-weight: 500;
    margin-top: 20px;
    display: block;
}

/* Ad Banner Style */
.ad-banner {	
    width: 100%;
    background-color: #0f1d30;
}
.ad-banner img {
    width: 100%;
    max-height: 350px;
    object-fit: cover;
    display: block;
    border-bottom: 3px solid #d1a553;
}

/* Hero Section */
.hero { padding: 60px 0 120px 0; }

.hero-logo {
    display: block;
    margin: 0 auto 30px auto;
    max-width: 250px;
    width: 100%;
    height: auto;
}

.hero h1 { font-size: 3.5rem; margin-bottom: 24px; line-height: 1.15; max-width: 800px; text-align: left; }
.hero p { font-size: 1.1rem; max-width: 550px; margin-bottom: 40px; color: #cbd5e1; text-align: left; }

/* Buttons */
.btn { 
    padding: 14px 28px; border-radius: 6px; font-weight: 500; 
    text-decoration: none; display: inline-block; cursor: pointer; 
    transition: all 0.2s; font-size: 0.95rem;
}
.btn-gold { background-color: #d1a553; color: #0f1d30; border: none; }
.btn-gold:hover { background-color: #dfb25e; }
.btn-outline { border: 1px solid rgba(255,255,255,0.4); color: #ffffff; background: transparent; margin-left: 12px; }
.btn-outline:hover { background-color: rgba(255,255,255,0.1); border-color: #fff; }
.btn-outline-dark { border: 1px solid #0f1d30; color: #0f1d30; margin-top: 20px;}

/* Quick Stats */
.quick-stats { 
    display: grid; grid-template-columns: 1fr 1fr; 
    background: #ffffff; border-radius: 8px; 
    box-shadow: 0 10px 30px rgba(0,0,0,0.05); 
    margin-top: -60px; position: relative; z-index: 10; 
    border: 1px solid #eaeaea;
}
.stat-item { padding: 32px; border-bottom: 1px solid #eaeaea; border-right: 1px solid #eaeaea; }
.stat-item:nth-child(2n) { border-right: none; }
.stat-item:nth-child(n+3) { border-bottom: none; }
.stat-title { font-weight: 600; color: #0f1d30; display: flex; align-items: center; gap: 10px; margin-bottom: 6px; font-size: 1.05rem; }
.stat-icon { color: #d1a553; }
.stat-desc { font-size: 0.9rem; color: #6b7280; }

/* Quote Banner */
.quote-banner { margin: 80px 0 60px; padding: 40px 50px; border-radius: 8px; position: relative; }
.quote-line { width: 40px; height: 2px; background: #d1a553; margin-bottom: 24px; }
.quote-banner h2 { font-style: italic; font-size: 1.8rem; font-weight: 400; margin-bottom: 24px; color: #fff; line-height: 1.4; }
.quote-code { color: #2dd4bf; font-family: monospace; font-size: 0.9rem; }

/* Section Typography */
.section-title { font-size: 2.4rem; margin-bottom: 16px; color: #0f1d30; }
.section-desc { color: #6b7280; font-size: 1.05rem; max-width: 600px; margin-bottom: 40px; }

/* Built for Builders */
.builders-section { padding-bottom: 80px; scroll-margin-top: 40px; }
.check-list { list-style: none; margin-bottom: 30px; margin-top: 30px; }
.check-list li { margin-bottom: 16px; display: flex; align-items: center; gap: 12px; color: #4b5563; font-size: 0.95rem; }
.check-list li::before { content: "✓"; color: #d1a553; font-weight: bold; }

/* Areas of Study Cards (2x2 Grid) */
.study-cards { display: grid; grid-template-columns: 1fr 1fr; gap: 24px; margin-top: 40px; }
.card { background: #ffffff; padding: 30px; border-radius: 8px; border: 1px solid #eaeaea; border-top: 3px solid #2dd4bf; }
.card-gold { border-top-color: #d1a553; }
.card-navy { border-top-color: #0f1d30; }

.card-icon { width: 45px; height: 45px; background: #f0fdfa; display: flex; align-items: center; justify-content: center; border-radius: 8px; margin-bottom: 20px; color: #2dd4bf; font-weight: bold; font-size: 1.2rem;}
.card-gold .card-icon { background: #fefce8; color: #d1a553; }
.card-navy .card-icon { background: #f1f5f9; color: #0f1d30; }

.course-code { font-size: 0.75rem; background: #f3f4f6; padding: 4px 8px; border-radius: 4px; color: #6b7280; font-family: monospace; display: inline-block; margin-bottom: 12px; }
.card h3 { font-family: 'Inter', sans-serif; font-size: 1.2rem; margin-bottom: 12px; color: #0f1d30; }
.card p { font-size: 0.9rem; color: #6b7280; }

/* Program Photos */
.photos-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 24px; margin-top: 40px; }
.photo-card img { width: 100%; height: 250px; object-fit: cover; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.05); }

/* Deep Stats Grid */
.metrics-grid { display: grid; grid-template-columns: repeat(2, 1fr); gap: 1px; background: rgba(255,255,255,0.1); border-top: 1px solid rgba(255,255,255,0.1); border-bottom: 1px solid rgba(255,255,255,0.1); }
.metric-box { padding: 80px 20px; text-align: center; border-right: 1px solid rgba(255,255,255,0.1); border-bottom: 1px solid rgba(255,255,255,0.1); }
.metric-box:nth-child(2n) { border-right: none; }
.metric-box:nth-child(n+3) { border-bottom: none; }
.metric-number { font-size: 3.5rem; color: #d1a553; font-family: 'Playfair Display', serif; font-weight: 700; margin-bottom: 8px; }
.metric-label { font-size: 1rem; color: #cbd5e1; font-weight: 400; }

/* Pills / Careers */
.pills-wrapper { display: flex; flex-wrap: wrap; gap: 12px; margin-top: 30px; }
.pill { border: 1px solid #e5e7eb; padding: 10px 24px; border-radius: 50px; font-size: 0.9rem; color: #4b5563; background: #ffffff; }

/* Footer */
footer { padding: 80px 0 40px 0; font-size: 0.9rem; scroll-margin-top: 40px; }
.footer-grid { display: grid; grid-template-columns: 2fr 1fr 1fr; gap: 60px; margin-bottom: 60px; }
.footer-logo { margin-bottom: 20px; }
.footer-logo .brand-logo { width: 40px; height: 40px; } 
.footer-logo h2 { font-family: 'Inter', sans-serif; font-size: 1.1rem; color: #ffffff; margin-bottom: 4px; }
.footer-logo p { color: #cbd5e1; font-size: 0.8rem; }
.footer-desc { color: #94a3b8; max-width: 300px; margin-bottom: 20px; line-height: 1.6; }

.footer-links h3 { color: #ffffff; font-family: 'Inter', sans-serif; font-size: 1rem; margin-bottom: 20px; }
.footer-links ul { list-style: none; }
.footer-links li { margin-bottom: 12px; }
.footer-links a { color: #94a3b8; text-decoration: none; transition: color 0.2s; }
.footer-links a:hover { color: #d1a553; }

.contact-info { border-top: 1px solid rgba(255,255,255,0.1); padding-top: 40px; color: #94a3b8; }
.contact-info p { margin-bottom: 12px; }
.contact-info strong { color: #ffffff; font-weight: 500; display: block; margin-bottom: 4px; }

/* Responsive Design */
@media (max-width: 768px) {
    .hero h1 { font-size: 2.5rem; }
    .quick-stats { grid-template-columns: 1fr; }
    .stat-item { border-right: none; }
    .study-cards, .photos-grid { grid-template-columns: 1fr; }
    .metrics-grid { grid-template-columns: 1fr; }
    .metric-box { border-right: none; }
    .footer-grid { grid-template-columns: 1fr; gap: 40px; }
}
