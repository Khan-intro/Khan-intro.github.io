<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<meta name="description" content="Muhammad Bilal Khan, PhD — researcher in magnetic materials, additive manufacturing, and soft robotics at TU Darmstadt." />
<title>Muhammad Bilal Khan, PhD</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Source+Serif+4:ital,opsz,wght@0,8..60,400;0,8..60,600;0,8..60,700;1,8..60,400&family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
<style>
  :root{
    --ink:#1b2430; --sub:#5b6472; --line:#e6e3da; --paper:#fdfcf9; --panel:#f6f4ee;
    --accent:#7a4a2b; --accent2:#2e5a4e; --ring:#e9e4d8; --maxw:1080px;
  }
  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{margin:0;background:var(--paper);color:var(--ink);
    font-family:Inter,system-ui,-apple-system,Segoe UI,sans-serif;
    font-size:16px;line-height:1.7;-webkit-font-smoothing:antialiased;}
  .serif{font-family:"Source Serif 4",Georgia,serif;}
  a{color:var(--accent);text-decoration:none;}
  a:hover{text-decoration:underline;}
  .wrap{max-width:var(--maxw);margin:0 auto;padding:0 28px;}

  /* top bar */
  .topbar{position:sticky;top:0;z-index:30;background:rgba(253,252,249,.9);backdrop-filter:blur(8px);border-bottom:1px solid var(--line);}
  .topbar-inner{display:flex;align-items:center;justify-content:space-between;height:58px;}
  .topbar .name{font-weight:700;font-size:.92rem;letter-spacing:.01em;color:var(--ink);}
  .topbar nav{display:flex;gap:26px;font-size:.85rem;}
  .topbar nav a{color:var(--sub);font-weight:600;}
  .topbar nav a:hover{color:var(--accent);text-decoration:none;}
  .lang{font-size:.78rem;color:var(--sub);border:1px solid var(--line);border-radius:20px;padding:4px 12px;}

  /* hero / bio */
  .hero{padding:64px 0 20px;}
  .hero-grid{display:grid;grid-template-columns:190px 1fr;gap:42px;align-items:start;}
  .avatar{width:190px;height:230px;border-radius:6px;background:var(--panel);border:1px solid var(--ring);
    display:flex;align-items:center;justify-content:center;text-align:center;color:var(--sub);font-size:.78rem;padding:14px;}
  .hero h1{font-size:2.15rem;margin:0 0 3px;letter-spacing:-.01em;}
  .hero .role{color:var(--sub);font-size:.98rem;margin-bottom:16px;}
  .hero .role a{color:var(--accent2);}
  .hero p{margin:0 0 14px;color:#2b3542;font-size:.99rem;}
  .contact-line{font-size:.85rem;color:var(--sub);margin-top:14px;}
  .contact-line a{color:var(--accent);}
  .badges{display:flex;flex-wrap:wrap;gap:8px;margin-top:16px;}
  .badge{font-size:.74rem;font-weight:600;color:var(--accent2);background:#eef4f1;border:1px solid #dbe8e2;padding:4px 10px;border-radius:20px;}

  section{padding:34px 0;border-top:1px solid var(--line);}
  section:first-of-type{border-top:none;}
  .sec-title{display:flex;align-items:baseline;gap:10px;margin-bottom:18px;}
  .sec-title h2{font-size:1.28rem;margin:0;letter-spacing:-.01em;}
  .sec-title .rule{flex:1;height:1px;background:var(--line);}
  .sec-note{color:var(--sub);font-size:.85rem;margin:-8px 0 18px;}

  /* research interests */
  .interests{display:grid;gap:12px;}
  .interest{display:grid;grid-template-columns:190px 1fr;gap:18px;padding:10px 0;}
  .interest dt{font-weight:700;color:var(--ink);font-size:.92rem;}
  .interest dd{margin:0;color:var(--sub);font-size:.92rem;}

  /* news / timeline */
  .news{display:grid;gap:2px;}
  .news-item{display:grid;grid-template-columns:88px 1fr;gap:18px;padding:11px 0;border-bottom:1px dashed var(--line);}
  .news-item:last-child{border-bottom:none;}
  .news-date{font-size:.78rem;color:var(--accent2);font-weight:700;letter-spacing:.02em;padding-top:2px;}
  .news-text{font-size:.92rem;color:#2b3542;}
  .news-text a{font-weight:600;}

  /* services */
  .svc-grid{display:grid;grid-template-columns:1fr 1fr;gap:32px;}
  .svc-col h3{font-size:.86rem;text-transform:uppercase;letter-spacing:.06em;color:var(--accent2);margin:0 0 10px;}
  .svc-col ul{margin:0 0 20px;padding-left:18px;color:#2b3542;font-size:.9rem;}
  .svc-col li{margin-bottom:6px;}

  /* publications */
  .pub-note{color:var(--sub);font-size:.83rem;margin-bottom:20px;}
  .pub-note a{font-weight:600;}
  .pub{padding:22px 0;border-bottom:1px solid var(--line);}
  .pub:last-child{border-bottom:none;}
  .pub-head{display:flex;justify-content:space-between;gap:16px;align-items:baseline;flex-wrap:wrap;}
  .pub-title{font-weight:700;font-size:1.01rem;color:var(--ink);}
  .pub-venue{font-size:.78rem;color:var(--accent2);font-weight:700;background:#eef4f1;padding:3px 9px;border-radius:14px;white-space:nowrap;}
  .pub-authors{font-size:.87rem;color:var(--sub);margin:5px 0 9px;}
  .pub-authors strong{color:var(--ink);}
  .pub-abstract{font-size:.89rem;color:#3a4351;margin:0;}
  .pub-links{margin-top:9px;font-size:.83rem;}
  .pub-links a{margin-right:14px;font-weight:600;}

  /* footer */
  footer{padding:34px 0 60px;color:var(--sub);font-size:.8rem;text-align:center;}
  footer a{color:var(--sub);}

  .toggle-abs{background:none;border:none;color:var(--accent);font-size:.83rem;font-weight:600;cursor:pointer;padding:0;margin-top:8px;}
  .abs-body{display:none;margin-top:8px;}
  .abs-body.open{display:block;}

  @media (max-width:720px){
    .hero-grid{grid-template-columns:1fr;}
    .avatar{width:140px;height:170px;}
    .interest{grid-template-columns:1fr;gap:4px;}
    .svc-grid{grid-template-columns:1fr;gap:8px;}
    .news-item{grid-template-columns:70px 1fr;}
    .topbar nav{gap:14px;font-size:.78rem;}
  }
</style>
</head>
<body>

<div class="topbar">
  <div class="wrap topbar-inner">
    <div class="name">Muhammad Bilal Khan, PhD</div>
    <nav>
      <a href="#about">About</a>
      <a href="#interests">Research</a>
      <a href="#news">News</a>
      <a href="#service">Service</a>
      <a href="#publications">Publications</a>
      <a href="#contact">Contact</a>
    </nav>
    <span class="lang">EN</span>
  </div>
</div>

<div class="wrap">

  <section class="hero" id="about">
    <div class="hero-grid">
      <div class="avatar">Portrait<br>placeholder<br><span style="font-size:.7rem">replace with a 3:4 photo</span></div>
      <div>
        <h1 class="serif">Muhammad Bilal Khan, PhD, PhD</h1>
        <div class="role">Darmstadt, Germany &nbsp;·&nbsp; Email: mbilalkhannu [at] gmail [dot] com</div>

        <p>I am currently a <strong>Research Associate</strong> at the <a href="#">Institute of Materials Science, Technische Universität Darmstadt</a>, working within the Research Training Group <em>RTG Lokoassist</em>, where I lead research on laser powder bed fusion of magnetic composites for smart actuators, sensors and soft robotics. My research spans functional magnetic materials, additive manufacturing, bioinspired robotics, and data-driven engineering, with applications in assistive technology, sustainable manufacturing, and intelligent automation.</p>

        <p>Previously, I was a <strong>Marie Skłodowska-Curie Research Fellow</strong> at Tecnalia Research and Innovation, Spain, working on digital manufacturing and industrial robotics under the EU Horizon 2020 programme. I hold a joint academic background across two PhDs — in <strong>Materials Science</strong> (Technische Universität Darmstadt) and <strong>Information Science and Technology</strong> (Vidyasirimedhi Institute of Science and Technology, Thailand) — supported by research periods in Denmark, the United States, and Pakistan.</p>

        <p>I am passionate about connecting fundamental materials research with practical, sustainable engineering — developing recyclable magnetic composites, digitally manufactured robotic systems, and data-driven tools that bridge academic research and real-world impact.</p>

        <p>I am always open to collaboration with motivated students and researchers. Feel free to reach out if our interests align — please write to <a href="mailto:mbilalkhannu@gmail.com">mbilalkhannu@gmail.com</a>.</p>

        <div class="badges">
          <span class="badge">Magnetic Materials</span>
          <span class="badge">Additive Manufacturing</span>
          <span class="badge">Soft Robotics</span>
          <span class="badge">Sustainable Engineering</span>
          <span class="badge">Applied AI</span>
        </div>
      </div>
    </div>
  </section>

  <section id="interests">
    <div class="sec-title"><h2 class="serif">Research Interests</h2><div class="rule"></div></div>
    <dl class="interests">
      <div class="interest"><dt>Magnetic & Functional Materials</dt><dd>Nd–Fe–B composites, magnetic actuation, locally tailored stiffness, rare-earth recycling and circular material design.</dd></div>
      <div class="interest"><dt>Additive Manufacturing</dt><dd>Laser powder bed fusion, process–structure–property relationships, and design for advanced manufacturing of smart devices.</dd></div>
      <div class="interest"><dt>Soft & Bioinspired Robotics</dt><dd>Magnetically actuated soft robots, inchworm- and ray-inspired locomotion, compliant actuators and sensing.</dd></div>
      <div class="interest"><dt>Robotics & Automation</dt><dd>Industrial robot trajectory optimisation, collision avoidance, CAD-based automated inspection, and Industry 4.0 systems.</dd></div>
      <div class="interest"><dt>Data-Driven Engineering</dt><dd>Python/MATLAB-based analysis, machine learning, and simulation for materials processing and robotic system design.</dd></div>
      <div class="interest"><dt>Sustainable Smart Devices</dt><dd>Degradable and recyclable magnetic composites for soft actuation, wearable sensing, and assistive technologies.</dd></div>
    </dl>
  </section>

  <section id="news">
    <div class="sec-title"><h2 class="serif">News</h2><div class="rule"></div></div>
    <div class="news">
      <div class="news-item"><div class="news-date">2026/08</div><div class="news-text">Paper <a href="https://doi.org/10.1088/1361-665X/ae8cc7">“Muscle-Inspired Magnetic Actuators That Push, Pull, Crawl, and Grasp”</a> published in <em>Smart Materials and Structures</em>.</div></div>
      <div class="news-item"><div class="news-date">2025/09</div><div class="news-text">Paper <a href="https://doi.org/10.1002/adrr.202500114">“Degradable Magnetic Composites from Recycled Nd-Fe-B Magnets for Soft Actuation and Sensing”</a> published in <em>Advanced Robotics Research</em>. Muhammad Bilal Khan and Lin Guo contributed equally.</div></div>
      <div class="news-item"><div class="news-date">2024–25</div><div class="news-text">Paper <a href="https://doi.org/10.1002/aisy.202400620">“Bioinspired Design, Fabrication, and Wing Morphing of 3D-Printed Magnetic Butterflies”</a> published in <em>Advanced Intelligent Systems</em>.</div></div>
      <div class="news-item"><div class="news-date">2024</div><div class="news-text">Paper <a href="https://www.sciencedirect.com/science/article/abs/pii/S2214860423005183">“Magneto-Active Composites with Locally Tailored Stiffness Produced by Laser Powder Bed Fusion”</a> published in <em>Additive Manufacturing</em>.</div></div>
      <div class="news-item"><div class="news-date">2022–Present</div><div class="news-text">Leading research on laser powder bed fusion of magnetic composites at TU Darmstadt; supervising 2 MSc theses and 5 BSc projects.</div></div>
      <div class="news-item"><div class="news-date">2022</div><div class="news-text">Paper <a href="https://doi.org/10.3389/fbioe.2022.842816">“Electromagnetic Feet With Soft Toes for Adaptive, Versatile, and Stable Locomotion”</a> published in <em>Frontiers in Bioengineering and Biotechnology</em>.</div></div>
      <div class="news-item"><div class="news-date">2020</div><div class="news-text">Started as Marie Skłodowska-Curie Research Fellow at Tecnalia Research and Innovation, Spain, working on digital manufacturing and industrial robotics.</div></div>
    </div>
  </section>

  <section id="service">
    <div class="sec-title"><h2 class="serif">Service</h2><div class="rule"></div></div>
    <div class="svc-grid">
      <div class="svc-col">
        <h3>Academic Service</h3>
        <ul>
          <li>Thesis and student-project supervision, TU Darmstadt (2 MSc, 5 BSc)</li>
          <li>Regional Judge, CNM Science and Research Challenge, University of New Mexico (2015)</li>
          <li>Volunteer Referee, VEX Robotics Competition, University of New Mexico (2015)</li>
          <li>Member, Marie Curie Alumni Association</li>
        </ul>
        <h3>Teaching</h3>
        <ul>
          <li>Advanced Research Lab: Magnetic Material Qualification, TU Darmstadt</li>
          <li>Teaching Assistant, Mechatronics Engineering Laboratories I–IV, Prince of Songkla University</li>
          <li>Teaching Assistant, Robotics I & II, Namal College</li>
        </ul>
      </div>
      <div class="svc-col">
        <h3>Outreach & Mentoring</h3>
        <ul>
          <li>Volunteer Mathematics Teacher, Boonlert School, Thailand (2017–2018)</li>
          <li>Peer-Assisted Learning Leader, Namal College (2015)</li>
          <li>External Events Manager, Namal Society for Social Impact (2013–2015)</li>
        </ul>
        <h3>Community</h3>
        <ul>
          <li>Best Student Cultural Ambassador, IREX, Washington D.C. (2015)</li>
          <li>Flood-Relief Volunteer, Imran Khan Foundation (2015)</li>
        </ul>
      </div>
    </div>
  </section>

  <section id="publications">
    <div class="sec-title"><h2 class="serif">Selected Publications</h2><div class="rule"></div></div>
    <p class="pub-note"><a href="#">See all publications on Google Scholar ↗</a> &nbsp;·&nbsp; *: equal contribution &nbsp;·&nbsp; ✉: corresponding author</p>

    <article class="pub">
      <div class="pub-head"><div class="pub-title serif">Muscle-Inspired Magnetic Actuators That Push, Pull, Crawl, and Grasp</div><div class="pub-venue">Smart Mater. Struct., 2026</div></div>
      <div class="pub-authors"><strong>M. B. Khan</strong>✉, F. Hofmann, K. Schäfer, M. Lutzi, and O. Gutfleisch, <em>Smart Materials and Structures</em>, 2026.</div>
      <p class="pub-abstract">Functional TPU/Nd–Fe–B magnetic composites fabricated by laser powder bed fusion are designed to mimic muscle-like actuation. The resulting devices demonstrate field-driven pushing, pulling, crawling and grasping behaviours, with load-bearing performance far exceeding their own weight, establishing a versatile actuator platform for soft robotics.</p>
      <div class="pub-links"><a href="https://doi.org/10.1088/1361-665X/ae8cc7">DOI ↗</a></div>
    </article>

    <article class="pub">
      <div class="pub-head"><div class="pub-title serif">Degradable Magnetic Composites from Recycled Nd-Fe-B Magnets for Soft Actuation and Sensing</div><div class="pub-venue">Adv. Robotics Res., 2025</div></div>
      <div class="pub-authors"><strong>M. B. Khan</strong>*, L. Guo*, K. Schäfer, E. S. Oliveros-Mata, X. Wang, F. Hofmann, M. Lutzi, M. Suppelt, P. T. Das, J. Schmidtpeter, et al., <em>Advanced Robotics Research</em>, 2025.</div>
      <p class="pub-abstract">A fully degradable, recyclable magnetic-composite platform is developed from recycled Nd–Fe–B microparticles embedded in a gelatin-based organogel. The material enables soft magnetic actuation, jumping soft robots, and magnetoelastic sensing for touch, gait and contactless-motion detection, offering a sustainable alternative to conventional rigid magnetic composites.</p>
      <div class="pub-links"><a href="https://doi.org/10.1002/adrr.202500114">DOI ↗</a></div>
    </article>

    <article class="pub">
      <div class="pub-head"><div class="pub-title serif">Bioinspired Design, Fabrication, and Wing Morphing of 3D-Printed Magnetic Butterflies</div><div class="pub-venue">Adv. Intell. Syst., 2024/25</div></div>
      <div class="pub-authors"><strong>M. B. Khan</strong>, K. Schäfer, F. Hofmann, M. Lutzi, E. S. Oliveros-Mata, et al., <em>Advanced Intelligent Systems</em>, 2024/2025.</div>
      <p class="pub-abstract">Inspired by monarch butterflies, this work presents 3D-printed magnetic composite wings capable of programmable, field-driven morphing. Local control of stiffness and magnetisation direction enables tunable flapping and folding behaviours, demonstrating a design pathway for lightweight, bioinspired magnetic actuators.</p>
      <div class="pub-links"><a href="https://doi.org/10.1002/aisy.202400620">DOI ↗</a></div>
    </article>

    <article class="pub">
      <div class="pub-head"><div class="pub-title serif">Magneto-Active Composites with Locally Tailored Stiffness Produced by Laser Powder Bed Fusion</div><div class="pub-venue">Additive Manuf., 2024</div></div>
      <div class="pub-authors">K. Schäfer, M. Lutzi, <strong>M. B. Khan</strong>, L. Schäfer, I. Dirba, S. Bruns, I. Valizadeh, et al., <em>Additive Manufacturing</em>, 79, 103905, 2024.</div>
      <p class="pub-abstract">A single-step laser powder bed fusion process is proposed that enables precise, spatially resolved control of mechanical stiffness within magneto-active composites, opening new possibilities for functionally graded actuators and medical devices such as magnetically controlled stents.</p>
      <div class="pub-links"><a href="https://www.sciencedirect.com/science/article/abs/pii/S2214860423005183">Publisher ↗</a><a href="https://arxiv.org/abs/2305.02643">Preprint ↗</a></div>
    </article>

    <article class="pub">
      <div class="pub-head"><div class="pub-title serif">Electromagnetic Feet With Soft Toes for Adaptive, Versatile, and Stable Locomotion of an Inchworm-Inspired Pipe Crawling Robot</div><div class="pub-venue">Front. Bioeng. Biotechnol., 2022</div></div>
      <div class="pub-authors"><strong>M. B. Khan</strong>, T. Chuthong, J. Homchanthanakul, and P. Manoonpong, <em>Frontiers in Bioengineering and Biotechnology</em>, 10, 842816, 2022.</div>
      <p class="pub-abstract">A hybrid rigid–soft electromagnetic foot design is introduced for the iCrawl pipe-inspection robot, combining magnetic adhesion with compliant toe structures to achieve adaptive, stable and versatile locomotion across varied metal pipe geometries.</p>
      <div class="pub-links"><a href="https://doi.org/10.3389/fbioe.2022.842816">DOI ↗</a></div>
    </article>

    <article class="pub">
      <div class="pub-head"><div class="pub-title serif">iCrawl: An Inchworm-Inspired Crawling Robot</div><div class="pub-venue">IEEE Access, 2020</div></div>
      <div class="pub-authors"><strong>M. B. Khan</strong>, T. Chuthong, C. D. Do, M. Thor, P. Billeschou, J. C. Larsen, and P. Manoonpong, <em>IEEE Access</em>, 8, 200655–200668, 2020.</div>
      <p class="pub-abstract">This paper introduces iCrawl, a 5-DOF inchworm-inspired robot for outer pipe inspection, using electromagnetic feet with passive foot-caps to achieve robust, versatile crawling on ferromagnetic pipe surfaces without complex control schemes.</p>
      <div class="pub-links"><a href="https://doi.org/10.1109/ACCESS.2020.3035871">DOI ↗</a></div>
    </article>

    <article class="pub">
      <div class="pub-head"><div class="pub-title serif">A Comparative Study of RTV-225 Silicone Elastomer and Natural Rubber Based Thermo-Elastomer for Soft Robotic Applications</div><div class="pub-venue">JAMT, 2019</div></div>
      <div class="pub-authors"><strong>M. B. Khan</strong>, P. Smithmaitrie, and E. Kalkornsurapranee, <em>Journal of Advanced Manufacturing Technology</em>, 13(2/1), 2019.</div>
      <p class="pub-abstract">This study compares the mechanical performance of RTV-225 silicone elastomer against a natural-rubber-based thermoplastic elastomer, providing practical material-selection guidance for soft robotic actuator and structure design.</p>
    </article>

    <article class="pub">
      <div class="pub-head"><div class="pub-title serif">Design and Fabrication of a 3-Fin Symmetric Ray-Inspired Soft Robot for Underwater Exploration</div><div class="pub-venue">IJMAM, 2018</div></div>
      <div class="pub-authors"><strong>M. B. Khan</strong> and P. Smithmaitrie, <em>International Journal of Mechatronics and Applied Mechanics</em>, 4, 2018.</div>
      <p class="pub-abstract">A three-fin, elastomer-based soft robot inspired by manta rays and stingrays is designed and fabricated for underwater locomotion, with two fins generating thrust and a third enabling steering control.</p>
      <div class="pub-links"><a href="https://ijomam.com/wp-content/uploads/2018/11/pag.-7-16_DESIGN-AND-FABRICATION-OF-A-3-FIN-SYMMETRIC-RAY.pdf">PDF ↗</a></div>
    </article>

  </section>

  <section id="contact">
    <div class="sec-title"><h2 class="serif">Contact</h2><div class="rule"></div></div>
    <p class="contact-line">Email: <a href="mailto:mbilalkhannu@gmail.com">mbilalkhannu [at] gmail [dot] com</a> &nbsp;·&nbsp; <a href="mailto:Muhammad.khan3@tu-darmstadt.com">Muhammad.khan3 [at] tu-darmstadt [dot] com</a></p>
    <p class="contact-line">Institute of Materials Science, Technische Universität Darmstadt, Darmstadt, Germany</p>
    <p class="contact-line"><a href="#">Google Scholar</a> &nbsp;·&nbsp; <a href="#">ORCID</a> &nbsp;·&nbsp; <a href="#">LinkedIn</a> &nbsp;·&nbsp; <a href="#">GitHub</a></p>
  </section>

</div>

<footer>© Copyright 2022–<span id="y"></span> Muhammad Bilal Khan. Built with GitHub Pages.</footer>
<script>document.getElementById('y').textContent = new Date().getFullYear();</script>
</body>
</html>
