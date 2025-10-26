<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Syed Sardar Valli - Cloud Architect & DevOps Engineer</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet"/>
  <style>
    :root {
      --bg: #0d1117;
      --card: #161b22;
      --text: #f0f6fc;
      --primary: #2e9ef7;
      --accent: #9333ea;
      --success: #28a745;
      --radius: 12px;
      --shadow: 0 8px 24px rgba(0,0,0,0.3);
      --transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
    }
    * { margin:0; padding:0; box-sizing:border-box; }
    body {
      background: var(--bg);
      color: var(--text);
      font-family: 'Inter', sans-serif;
      line-height: 1.7;
      padding: 1rem;
    }
    .container { max-width: 1100px; margin: 0 auto; }
    h1, h2, h3 { font-weight: 700; }
    a { color: inherit; text-decoration: none; transition: var(--transition); }
    a:hover { opacity: 0.8; }

    /* Header */
    .header {
      text-align: center;
      padding: 2rem 0 1.5rem;
      position: relative;
    }
    .header::before {
      content: "";
      position: absolute;
      top: 0; left: 0; right: 0;
      height: 200px;
      background: linear-gradient(135deg, var(--primary), var(--accent));
      border-radius: 0 0 30% 30% / 0 0 100% 100%;
      z-index: -1;
    }
    .name {
      font-size: 3.5rem;
      font-weight: 700;
      color: white;
      text-shadow: 0 4px 12px rgba(0,0,0,0.3);
      animation: fadeInDown 1s ease-out;
    }
    .tagline {
      font-size: 1.25rem;
      color: rgba(255,255,255,0.9);
      margin-top: 0.5rem;
      animation: fadeInUp 1s ease-out 0.2s backwards;
    }

    /* Badges */
    .badges {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 0.75rem;
      margin: 1.5rem 0;
      animation: fadeInUp 1s ease-out 0.4s backwards;
    }
    .badge {
      background: rgba(255,255,255,0.1);
      backdrop-filter: blur(10px);
      padding: 0.5rem 1rem;
      border-radius: 50px;
      font-size: 0.875rem;
      font-weight: 500;
      color: white;
      border: 1px solid rgba(255,255,255,0.15);
    }

    /* Connect */
    .connect {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 0.75rem;
      margin: 2rem 0;
    }
    .connect a {
      display: flex;
      align-items: center;
      gap: 0.5rem;
      background: var(--card);
      padding: 0.75rem 1.25rem;
      border-radius: var(--radius);
      font-weight: 500;
      transition: var(--transition);
      box-shadow: var(--shadow);
    }
    .connect a:hover {
      transform: translateY(-4px);
      box-shadow: 0 12px 32px rgba(0,0,0,0.4);
    }
    .connect img {
      width: 20px; height: 20px;
    }

    /* Section */
    .section {
      margin: 3rem 0;
      padding: 2rem;
      background: var(--card);
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      position: relative;
      overflow: hidden;
    }
    .section::before {
      content: "";
      position: absolute;
      top: 0; left: 0;
      width: 6px;
      height: 100%;
      background: linear-gradient(var(--primary), var(--accent));
    }
    .section-title {
      font-size: 1.75rem;
      margin-bottom: 1.5rem;
      color: var(--primary);
      display: flex;
      align-items: center;
      gap: 0.75rem;
    }
    .section-title::before {
      content: "";
      width: 8px; height: 8px;
      background: var(--accent);
      border-radius: 50%;
    }

    /* Profile YAML */
    .yaml {
      background: #0d1117;
      padding: 1.5rem;
      border-radius: var(--radius);
      font-family: 'JetBrains Mono', monospace;
      font-size: 0.9rem;
      color: #8b949e;
      overflow-x: auto;
      box-shadow: inset 0 2px 8px rgba(0,0,0,0.3);
    }
    .yaml .key { color: #79c0ff; }
    .yaml .string { color: #a5d6ff; }
    .yaml .comment { color: #8b949e; font-style: italic; }

    /* Skills */
    .skills-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
      gap: 1.5rem;
      margin-top: 1.5rem;
    }
    .skill-card {
      background: rgba(255,255,255,0.03);
      padding: 1.25rem;
      border-radius: var(--radius);
      border: 1px solid rgba(255,255,255,0.1);
      transition: var(--transition);
    }
    .skill-card:hover {
      border-color: var(--primary);
      transform: translateY(-4px);
    }
    .skill-title {
      font-weight: 600;
      margin-bottom: 0.75rem;
      color: var(--accent);
    }
    .skill-icons {
      display: flex;
      flex-wrap: wrap;
      gap: 0.75rem;
    }
    .skill-icons img {
      width: 42px; height: 42px;
      transition: var(--transition);
    }
    .skill-icons img:hover {
      transform: scale(1.15);
    }

    /* Projects */
    .projects-table {
      width: 100%;
      border-collapse: collapse;
      margin-top: 1rem;
    }
    .projects-table td {
      padding: 1.25rem;
      vertical-align: top;
      border-bottom: 1px solid rgba(255,255,255,0.08);
    }
    .project {
      background: rgba(255,255,255,0.03);
      padding: 1.25rem;
      border-radius: var(--radius);
      height: 100%;
      transition: var(--transition);
    }
    .project:hover {
      background: rgba(46,158,247,0.1);
      transform: translateY(-4px);
    }
    .project-title {
      font-weight: 600;
      margin-bottom: 0.75rem;
      color: var(--primary);
    }
    .project-badges {
      display: flex;
      flex-wrap: wrap;
      gap: 0.5rem;
      margin: 0.75rem 0;
    }
    .project-badge {
      font-size: 0.75rem;
      padding: 0.25rem 0.6rem;
      border-radius: 50px;
      font-weight: 500;
    }
    .project-desc {
      font-size: 0.95rem;
      color: #c9d1d9;
      margin-bottom: 1rem;
    }
    .project-features {
      list-style: none;
      font-size: 0.875rem;
      color: #8b949e;
    }
    .project-features li {
      position: relative;
      padding-left: 1.5rem;
      margin-bottom: 0.5rem;
    }
    .project-features li::before {
      content: "✓";
      position: absolute;
      left: 0;
      color: var(--success);
      font-weight: bold;
    }
    .project-link {
      display: inline-block;
      margin-top: 1rem;
      color: var(--primary);
      font-weight: 500;
      font-size: 0.875rem;
    }

    /* Certifications */
    .certs-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 1.5rem;
      margin-top: 1rem;
    }
    .cert-card {
      text-align: center;
      padding: 1.5rem;
      background: rgba(255,255,255,0.03);
      border-radius: var(--radius);
      border: 1px solid rgba(255,255,255,0.1);
      transition: var(--transition);
    }
    .cert-card:hover {
      border-color: var(--accent);
      transform: translateY(-4px);
    }
    .cert-badge {
      display: inline-block;
      padding: 0.5rem 1rem;
      background: #f80000;
      color: white;
      border-radius: 50px;
      font-size: 0.875rem;
      font-weight: 600;
      margin-bottom: 1rem;
    }

    /* Stats */
    .stats-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 1.5rem;
      margin: 2rem 0;
    }
    .stat-img {
      width: 100%;
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      transition: var(--transition);
    }
    .stat-img:hover {
      transform: scale(1.02);
    }

    /* Journey */
    .journey-code {
      background: #0d1117;
      padding: 1.5rem;
      border-radius: var(--radius);
      font-family: 'JetBrains Mono', monospace;
      font-size: 0.9rem;
      overflow-x: auto;
      margin: 1.5rem 0;
      box-shadow: inset 0 2px 8px rgba(0,0,0,0.3);
    }

    /* Opportunities */
    .opp-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 1.5rem;
      margin-top: 1rem;
    }
    .opp-card {
      background: rgba(40,167,69,0.1);
      border: 1px solid rgba(40,167,69,0.3);
      padding: 1.5rem;
      border-radius: var(--radius);
    }
    .opp-card h4 {
      color: var(--success);
      margin-bottom: 1rem;
    }
    .opp-card ul {
      list-style: none;
    }
    .opp-card li {
      position: relative;
      padding-left: 1.5rem;
      margin-bottom: 0.75rem;
      font-size: 0.95rem;
    }
    .opp-card li::before {
      content: "→";
      position: absolute;
      left: 0;
      color: var(--success);
      font-weight: bold;
    }

    /* Footer */
    .footer {
      text-align: center;
      padding: 3rem 1rem 2rem;
      position: relative;
    }
    .footer::before {
      content: "";
      position: absolute;
      bottom: 0; left: 0; right: 0;
      height: 120px;
      background: linear-gradient(135deg, var(--accent), var(--primary));
      border-radius: 30% 30% 0 0 / 100% 100% 0 0;
      z-index: -1;
    }
    .footer-quote {
      font-style: italic;
      color: rgba(255,255,255,0.9);
      margin: 1.5rem 0;
      font-size: 1.1rem;
    }
    .footer-sign {
      color: white;
      font-weight: 600;
    }

    /* Animations */
    @keyframes fadeInDown {
      from { opacity:0; transform:translateY(-30px); }
      to { opacity:1; transform:translateY(0); }
    }
    @keyframes fadeInUp {
      from { opacity:0; transform:translateY(30px); }
      to { opacity:1; transform:translateY(0); }
    }

    @media (max-width: 768px) {
      .name { font-size: 2.5rem; }
      .tagline { font-size: 1.1rem; }
      .section { padding: 1.5rem; }
      .projects-table td { display: block; width: 100%; padding: 1rem 0; }
      .project { margin-bottom: 1rem; }
    }
  </style>
</head>
<body>
  <div class="container">

    <!-- Header -->
    <header class="header">
      <h1 class="name">Syed Sardar Valli</h1>
      <p class="tagline">Cloud Architect | DevOps Engineer | Full-Stack Developer</p>

      <div class="badges">
        <span class="badge">Profile Views: <span id="views">-</span></span>
        <span class="badge">GitHub Followers: <span id="followers">-</span></span>
        <span class="badge">Focus: Cloud Native</span>
        <span class="badge" style="background:#28a745;color:white">Open To Work</span>
      </div>

      <div class="connect">
        <a href="mailto:syedsardarvali246@gmail.com">
          <img src="https://img.shields.io/badge/Gmail-D14836?style=flat-square&logo=gmail&logoColor=white" alt="Email"/>
          Email
        </a>
        <a href="https://linkedin.com/in/syed-sardar-valli">
          <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn"/>
          LinkedIn
        </a>
        <a href="https://github.com/sardarvali">
          <img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white" alt="GitHub"/>
          GitHub
        </a>
        <a href="https://syed-sardar-vali.web.app/">
          <img src="https://img.shields.io/badge/Portfolio-FF5722?style=flat-square&logo=google-chrome&logoColor=white" alt="Portfolio"/>
          Portfolio
        </a>
        <a href="tel:+919052579129">
          <img src="https://img.shields.io/badge/WhatsApp-25D366?style=flat-square&logo=whatsapp&logoColor=white" alt="WhatsApp"/>
          WhatsApp
        </a>
      </div>
    </header>

    <!-- About -->
    <section class="section">
      <h2 class="section-title">About Me</h2>
      <div style="display:flex;gap:2rem;align-items:flex-start;flex-wrap:wrap;">
        <div style="flex:1;min-width:300px;">
          <div class="yaml">
            <span class="comment"># 👨‍💻 Profile</span><br>
            <span class="key">name:</span> <span class="string">"Syed Sardar Valli"</span><br>
            <span class="key">title:</span> <span class="string">"Cloud & DevOps Engineer"</span><br>
            <span class="key">education:</span> <span class="string">"B.Tech CSE @ LPU"</span><br>
            <span class="key">location:</span> <span class="string">"Punjab, India 🇮🇳"</span><br><br>

            <span class="comment"># 🎯 Expertise</span><br>
            - Cloud Architecture (OCI, AWS, GCP)<br>
            - DevOps & CI/CD Automation<br>
            - Full-Stack Development<br>
            - Mobile App Development (Android)<br>
            - Infrastructure as Code<br><br>

            <span class="comment"># 🚀 Currently</span><br>
            - Building cloud-native solutions<br>
            - Mastering Kubernetes & Terraform<br>
            - Contributing to open source<br>
            - Pursuing advanced OCI certifications<br><br>

            <span class="comment"># 💡 Philosophy</span><br>
            <span class="string">"Automate everything, scale infinitely,<br> secure by default, deploy fearlessly"</span>
          </div>
        </div>
        <div style="flex:1;min-width:300px;text-align:center;">
          <img src="https://user-images.githubusercontent.com/74038190/229223263-cf2e4b07-2615-4f87-9c38-e37600f8381a.gif" alt="Coding" style="max-width:100%;border-radius:var(--radius);box-shadow:var(--shadow);"/>
        </div>
      </div>
    </section>

    <!-- Tech Stack -->
    <section class="section">
      <h2 class="section-title">Technology Arsenal</h2>
      <div class="skills-grid">
        <div class="skill-card">
          <h3 class="skill-title">☁️ Cloud & Infrastructure</h3>
          <div class="skill-icons">
            <img src="https://skillicons.dev/icons?i=aws" alt="AWS"/>
            <img src="https://skillicons.dev/icons?i=gcp" alt="GCP"/>
            <img src="https://skillicons.dev/icons?i=azure" alt="Azure"/>
            <img src="https://skillicons.dev/icons?i=docker" alt="Docker"/>
            <img src="https://skillicons.dev/icons?i=kubernetes" alt="Kubernetes"/>
            <img src="https://skillicons.dev/icons?i=terraform" alt="Terraform"/>
            <img src="https://skillicons.dev/icons?i=jenkins" alt="Jenkins"/>
            <img src="https://skillicons.dev/icons?i=ansible" alt="Ansible"/>
          </div>
          <div style="margin-top:0.75rem;display:flex;gap:0.5rem;flex-wrap:wrap;">
            <img src="https://img.shields.io/badge/Oracle_Cloud-F80000?style=flat-square&logo=oracle&logoColor=white" alt="OCI"/>
            <img src="https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black" alt="Linux"/>
            <img src="https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white" alt="Nginx"/>
          </div>
        </div>

        <div class="skill-card">
          <h3 class="skill-title">💻 Programming & Development</h3>
          <div class="skill-icons">
            <img src="https://skillicons.dev/icons?i=cpp" alt="C++"/>
            <img src="https://skillicons.dev/icons?i=java" alt="Java"/>
            <img src="https://skillicons.dev/icons?i=js" alt="JavaScript"/>
            <img src="https://skillicons.dev/icons?i=kotlin" alt="Kotlin"/>
            <img src="https://skillicons.dev/icons?i=python" alt="Python"/>
            <img src="https://skillicons.dev/icons?i=nodejs" alt="Node.js"/>
            <img src="https://skillicons.dev/icons?i=html" alt="HTML"/>
            <img src="https://skillicons.dev/icons?i=css" alt="CSS"/>
          </div>
          <div style="margin-top:0.75rem;display:flex;gap:0.5rem;flex-wrap:wrap;">
            <img src="https://img.shields.io/badge/Bootstrap-7952B3?style=flat-square&logo=bootstrap&logoColor=white" alt="Bootstrap"/>
            <img src="https://img.shields.io/badge/Express.js-000000?style=flat-square&logo=express&logoColor=white" alt="Express"/>
            <img src="https://img.shields.io/badge/REST_APIs-FF6C37?style=flat-square&logo=postman&logoColor=white" alt="REST APIs"/>
          </div>
        </div>

        <div class="skill-card">
          <h3 class="skill-title">📱 Mobile & Database</h3>
          <div class="skill-icons">
            <img src="https://skillicons.dev/icons?i=androidstudio" alt="Android Studio"/>
            <img src="https://skillicons.dev/icons?i=firebase" alt="Firebase"/>
            <img src="https://skillicons.dev/icons?i=mysql" alt="MySQL"/>
            <img src="https://skillicons.dev/icons?i=mongodb" alt="MongoDB"/>
            <img src="https://skillicons.dev/icons?i=sqlite" alt="SQLite"/>
          </div>
          <div style="margin-top:0.75rem;display:flex;gap:0.5rem;flex-wrap:wrap;">
            <img src="https://img.shields.io/badge/Firestore-FFCA28?style=flat-square&logo=firebase&logoColor=black" alt="Firestore"/>
            <img src="https://img.shields.io/badge/PostgreSQL-316192?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL"/>
          </div>
        </div>

        <div class="skill-card">
          <h3 class="skill-title">🔧 DevOps & Tools</h3>
          <div class="skill-icons">
            <img src="https://skillicons.dev/icons?i=git" alt="Git"/>
            <img src="https://skillicons.dev/icons?i=github" alt="GitHub"/>
            <img src="https://skillicons.dev/icons?i=gitlab" alt="GitLab"/>
            <img src="https://skillicons.dev/icons?i=vscode" alt="VS Code"/>
            <img src="https://skillicons.dev/icons?i=linux" alt="Linux"/>
            <img src="https://skillicons.dev/icons?i=bash" alt="Bash"/>
          </div>
          <div style="margin-top:0.75rem;display:flex;gap:0.5rem;flex-wrap:wrap;">
            <img src="https://img.shields.io/badge/CI/CD-2088FF?style=flat-square&logo=github-actions&logoColor=white" alt="CI/CD"/>
            <img src="https://img.shields.io/badge/Monitoring-FF6C37?style=flat-square&logo=prometheus&logoColor=white" alt="Monitoring"/>
            <img src="https://img.shields.io/badge/IaC-844FBA?style=flat-square&logo=terraform&logoColor=white" alt="IaC"/>
          </div>
        </div>
      </div>
    </section>

    <!-- Projects -->
    <section class="section">
      <h2 class="section-title">Featured Projects Portfolio</h2>
      <table class="projects-table">
        <tr>
          <td>
            <div class="project">
              <h3 class="project-title">PetCare Adoption Platform</h3>
              <div class="project-badges">
                <span class="project-badge" style="background:#FFCA28;color:black">Firebase</span>
                <span class="project-badge" style="background:#F7DF1E;color:black">JavaScript</span>
                <span class="project-badge" style="background:#E34F26;color:white">HTML5</span>
              </div>
              <p class="project-desc"><strong>Secure web-based pet adoption ecosystem</strong></p>
              <ul class="project-features">
                <li>Firebase Authentication & Authorization</li>
                <li>Real-time Admin Dashboard</li>
                <li>Cloud Firestore Integration</li>
                <li>Responsive Multi-Device Design</li>
                <li>Multi-step Form with Validation</li>
              </ul>
              <a href="#" class="project-link">View Project →</a>
            </div>
          </td>
          <td>
            <div class="project">
              <h3 class="project-title">GAIL Gas Management System</h3>
              <div class="project-badges">
                <span class="project-badge" style="background:#3DDC84;color:black">Android</span>
                <span class="project-badge" style="background:#7F52FF;color:white">Kotlin</span>
                <span class="project-badge" style="background:#003B57;color:white">SQLite</span>
              </div>
              <p class="project-desc"><strong>Enterprise gas distribution monitoring app</strong></p>
              <ul class="project-features">
                <li>Role-Based Access Control</li>
                <li>Real-time API Integration</li>
                <li>Workflow Approval System</li>
                <li>Material Design UI</li>
                <li>10+ Feature Modules</li>
              </ul>
              <a href="#" class="project-link">View Project →</a>
            </div>
          </td>
        </tr>
        <tr>
          <td>
            <div class="project">
              <h3 class="project-title">Personal Portfolio</h3>
              <div class="project-badges">
                <span class="project-badge" style="background:#FFCA28;color:black">Firebase</span>
                <span class="project-badge" style="background:#F7DF1E;color:black">JavaScript</span>
                <span class="project-badge" style="background:#1572B6;color:white">CSS3</span>
              </div>
              <p class="project-desc"><strong>Modern responsive portfolio showcase</strong></p>
              <ul class="project-features">
                <li>Contemporary Design System</li>
                <li>Optimized Performance</li>
                <li>Mobile-First Approach</li>
                <li>Integrated Contact Form</li>
                <li>Firebase Cloud Hosting</li>
              </ul>
              <a href="https://syed-sardar-vali.web.app/" class="project-link">Visit Site →</a>
            </div>
          </td>
          <td>
            <div class="project">
              <h3 class="project-title">Docker WebApp Deployment</h3>
              <div class="project-badges">
                <span class="project-badge" style="background:#2496ED;color:white">Docker</span>
                <span class="project-badge" style="background:#339933;color:white">Node.js</span>
                <span class="project-badge" style="background:#000;color:white">Express</span>
              </div>
              <p class="project-desc"><strong>Containerized microservices architecture</strong></p>
              <ul class="project-features">
                <li>Multi-Container Setup</li>
                <li>Docker Compose Orchestration</li>
                <li>Scalable Deployment</li>
                <li>Isolated Environments</li>
                <li>CI/CD Ready Infrastructure</li>
              </ul>
            </div>
          </td>
        </tr>
        <tr>
          <td>
            <div class="project">
              <h3 class="project-title">Restaurant Management System</h3>
              <div class="project-badges">
                <span class="project-badge" style="background:#ED8B00;color:white">Java</span>
                <span class="project-badge" style="background:#4479A1;color:white">MySQL</span>
                <span class="project-badge" style="background:#007396;color:white">JavaFX</span>
              </div>
              <p class="project-desc"><strong>End-to-end restaurant operations platform</strong></p>
              <ul class="project-features">
                <li>Order Management System</li>
                <li>Inventory Tracking</li>
                <li>Staff Management Module</li>
                <li>Billing & Invoicing</li>
                <li>Analytics Dashboard</li>
              </ul>
            </div>
          </td>
          <td>
            <div class="project">
              <h3 class="project-title">Real-Time ChatApp</h3>
              <div class="project-badges">
                <span class="project-badge" style="background:#3DDC84;color:black">Android</span>
                <span class="project-badge" style="background:#FFCA28;color:black">Firebase</span>
                <span class="project-badge" style="background:#7F52FF;color:white">Kotlin</span>
              </div>
              <p class="project-desc"><strong>Feature-rich messaging application</strong></p>
              <ul class="project-features">
                <li>Real-time Messaging</li>
                <li>User Authentication</li>
                <li>Media Sharing</li>
                <li>Push Notifications</li>
                <li>Message Persistence</li>
              </ul>
            </div>
          </td>
        </tr>
      </table>
    </section>

    <!-- Certifications -->
    <section class="section">
      <h2 class="section-title">Oracle Cloud Infrastructure Certifications</h2>
      <div style="text-align:center;margin-bottom:1.5rem;">
        <span style="display:inline-block;padding:0.5rem 1.25rem;background:#f80000;color:white;border-radius:50px;font-weight:600;font-size:1rem;">Certified Oracle Cloud Professional</span>
      </div>
      <div class="certs-grid">
        <div class="cert-card">
          <div class="cert-badge">AI & ML</div>
          <p><strong>OCI AI Foundations</strong></p>
          <a href="https://catalog-education.oracle.com/pls/certview/sharebadge?id=4ED6C5B5370C2C4643BCAF2269AC3A13F953A3846B982A9339038288D35FB3E0" target="_blank" style="color:var(--primary);">Verify →</a>
          <hr style="margin:1rem 0;border-color:rgba(255,255,255,0.1);"/>
          <p><strong>OCI Generative AI</strong></p>
          <a href="https://catalog-education.oracle.com/pls/certview/sharebadge?id=FFEBCE22E53B5A042F419C9F7AED5B19650F90179411AB78D1491E3CF1B88FEC" target="_blank" style="color:var(--primary);">Verify →</a>
        </div>
        <div class="cert-card">
          <div class="cert-badge">Cloud & Arch</div>
          <p><strong>OCI Foundations</strong></p>
          <a href="https://catalog-education.oracle.com/pls/certview/sharebadge?id=1327A6626097491F45C9022CEFA2A75845A4DC4123F49DBE0C58A5965464FBF3" target="_blank" style="color:var(--primary);">Verify →</a>
          <hr style="margin:1rem 0;border-color:rgba(255,255,255,0.1);"/>
          <p><strong>OCI Multicloud</strong></p>
          <a href="https://catalog-education.oracle.com/pls/certview/sharebadge?id=DEC3AA39FB719A25FA3B2E008ECC29B6AE6751331150011A7C8CD26F74FCEF43" target="_blank" style="color:var(--primary);">Verify →</a>
        </div>
        <div class="cert-card">
          <div class="cert-badge">DevOps & Net</div>
          <p><strong>OCI DevOps</strong></p>
          <a href="https://catalog-education.oracle.com/pls/certview/sharebadge?id=2B6FBFD47BEDE54DCFD41C14AF2120B19B2F4F4B7CBE3259B7131530FA979FC0" target="_blank" style="color:var(--primary);">Verify →</a>
          <hr style="margin:1rem 0;border-color:rgba(255,255,255,0.1);"/>
          <p><strong>OCI Networking</strong></p>
          <a href="https://catalog-education.oracle.com/pls/certview/sharebadge?id=8E3457B8F658EF1CA7C25B51CCD0800F8A819C4310A0817A4FE9DC639A447A07" target="_blank" style="color:var(--primary);">Verify →</a>
        </div>
      </div>
      <p style="text-align:center;margin-top:1.5rem;font-size:0.9rem;color:#8b949e;">Click any badge to verify certification authenticity</p>
    </section>

    <!-- GitHub Stats -->
    <section class="section">
      <h2 class="section-title">GitHub Performance Metrics</h2>
      <div class="stats-grid">
        <img src="https://github-readme-stats.vercel.app/api?username=sardarvali&show_icons=true&theme=radical&hide_border=true&bg_color=0D1117&title_color=2E9EF7&icon_color=9333EA&text_color=FFFFFF" alt="GitHub Stats" class="stat-img"/>
        <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=sardarvali&layout=compact&theme=radical&hide_border=true&bg_color=0D1117&title_color=2E9EF7&text_color=FFFFFF&langs_count=8" alt="Top Languages" class="stat-img"/>
      </div>
      <div style="margin:1.5rem 0;text-align:center;">
        <img src="https://github-readme-streak-stats.herokuapp.com/?user=sardarvali&theme=radical&hide_border=true&background=0D1117&stroke=2E9EF7&ring=9333EA&fire=FF6C37&currStreakLabel=2E9EF7" alt="Streak" class="stat-img" style="max-width:100%;"/>
      </div>
      <div style="text-align:center;margin:1.5rem 0;">
        <img src="https://github-readme-activity-graph.vercel.app/graph?username=sardarvali&theme=react-dark&hide_border=true&bg_color=0D1117&color=2E9EF7&line=9333EA&point=FF6C37" alt="Contribution Graph" class="stat-img"/>
      </div>
      <div style="text-align:center;margin:2rem 0;">
        <img src="https://github-profile-trophy.vercel.app/?username=sardarvali&theme=radical&no-frame=true&no-bg=true&row=1&column=7" alt="Trophies"/>
      </div>
    </section>

    <!-- Current Focus -->
    <section class="section">
      <h2 class="section-title">Current Focus & Learning Path</h2>
      <div class="journey-code">
        <span style="color:#79c0ff">const</span> <span style="color:#ff7b72">developerJourney</span> = {<br>
        &nbsp;&nbsp;<span style="color:#79c0ff">currentMission</span>: <span style="color:#a5d6ff">"Building scalable cloud-native solutions"</span>,<br><br>
        &nbsp;&nbsp;<span style="color:#79c0ff">learning</span>: {<br>
        &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#79c0ff">advanced</span>: [<span style="color:#a5d6ff">"Kubernetes Orchestration"</span>, <span style="color:#a5d6ff">"Terraform IaC"</span>, <span style="color:#a5d6ff">"OCI Advanced Services"</span>],<br>
        &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#79c0ff">exploring</span>: [<span style="color:#a5d6ff">"Service Mesh (Istio)"</span>, <span style="color:#a5d6ff">"GitOps (ArgoCD)"</span>, <span style="color:#a5d6ff">"Observability Stack"</span>],<br>
        &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#79c0ff">mastering</span>: [<span style="color:#a5d6ff">"Microservices Patterns"</span>, <span style="color:#a5d6ff">"Cloud Security"</span>, <span style="color:#a5d6ff">"CI/CD Pipelines"</span>]<br>
        &nbsp;&nbsp;},<br><br>
        &nbsp;&nbsp;<span style="color:#79c0ff">building</span>: {<br>
        &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#79c0ff">personal</span>: [<span style="color:#a5d6ff">"Multi-Cloud Management Dashboard"</span>, <span style="color:#a5d6ff">"DevOps Automation Toolkit"</span>],<br>
        &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#79c0ff">collaborative</span>: [<span style="color:#a5d6ff">"Open Source Contributions"</span>, <span style="color:#a5d6ff">"Community Projects"</span>]<br>
        &nbsp;&nbsp;},<br><br>
        &nbsp;&nbsp;<span style="color:#79c0ff">goals2025</span>: [<br>
        &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#a5d6ff">"Contribute to 10+ open source projects"</span>,<br>
        &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#a5d6ff">"Build production-grade microservices platform"</span>,<br>
        &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#a5d6ff">"Earn advanced cloud & DevOps certifications"</span>,<br>
        &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#a5d6ff">"Mentor aspiring cloud engineers"</span><br>
        &nbsp;&nbsp;],<br><br>
        &nbsp;&nbsp;<span style="color:#79c0ff">mantra</span>: <span style="color:#a5d6ff">"Code with purpose, deploy with confidence, scale with wisdom"</span><br>
        };
      </div>
    </section>

    <!-- Opportunities -->
    <section class="section">
      <h2 class="section-title">Professional Opportunities</h2>
      <div class="opp-grid">
        <div class="opp-card">
          <h4>🎯 Currently Seeking</h4>
          <ul>
            <li>Cloud Engineer / Solutions Architect</li>
            <li>DevOps Engineer / SRE</li>
            <li>Full-Stack Developer</li>
            <li>Android Developer</li>
            <li>Open Source Collaborations</li>
            <li>Internships & Co-op Programs</li>
          </ul>
        </div>
        <div class="opp-card">
          <h4>💪 What I Bring</h4>
          <ul>
            <li>Cloud-Native Architecture Design</li>
            <li>End-to-End DevOps Pipeline</li>
            <li>Cross-Platform Development</li>
            <li>Security-First Mindset</li>
            <li>Collaborative Team Player</li>
            <li>Continuous Learning Attitude</li>
          </ul>
        </div>
      </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
      <h2 style="color:white;margin-bottom:1rem;">Let's Build Something Amazing Together</h2>
      <div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:1rem;max-width:800px;margin:2rem auto;text-align:center;">
        <div>
          <strong>📧 Email</strong><br>
          syedsardarvali246@gmail.com
        </div>
        <div>
          <strong>💼 LinkedIn</strong><br>
          /in/syed-sardar-valli
        </div>
        <div>
          <strong>🌐 Portfolio</strong><br>
          syed-sardar-vali.web.app
        </div>
        <div>
          <strong>📱 WhatsApp</strong><br>
          +91 90525 79129
        </div>
        <div>
          <strong>🐙 GitHub</strong><br>
          @sardarvali
        </div>
        <div>
          <strong>💬 Open to</strong><br>
          Coffee Chats ☕
        </div>
      </div>
      <p class="footer-quote">"The best way to predict the future is to build it"</p>
      <p class="footer-sign">⭐ From sardarvali | Crafting tomorrow's solutions, one commit at a time 🚀</p>
    </footer>

  </div>

  <script>
    // Dynamic badges
    fetch('https://komarev.com/ghpvc/?username=sardarvali')
      .then(r => r.text())
      .then(v => document.getElementById('views').textContent = v)
      .catch(() => document.getElementById('views').textContent = 'N/A');

    fetch('https://api.github.com/users/sardarvali')
      .then(r => r.json())
      .then(d => document.getElementById('followers').textContent = d.followers)
      .catch(() => document.getElementById('followers').textContent = 'N/A');
  </script>
</body>
</html>
