<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Shakeela Shaik — Data Analyst Portfolio</title>
<link rel="preconnect" href="https://fonts.googleapis.com"/>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;500;700&family=Outfit:wght@300;400;500&display=swap" rel="stylesheet"/>
<style>
  *{box-sizing:border-box;margin:0;padding:0}
  :root{
    --teal-50:#E1F5EE;--teal-100:#9FE1CB;--teal-400:#1D9E75;--teal-600:#0F6E56;--teal-800:#085041;
    --blue-50:#E6F1FB;--blue-100:#B5D4F4;--blue-400:#378ADD;--blue-600:#185FA5;--blue-800:#0C447C;
    --purple-50:#EEEDFE;--purple-100:#CECBF6;--purple-400:#7F77DD;--purple-600:#534AB7;--purple-800:#3C3489;
    --coral-50:#FAECE7;--coral-100:#F5C4B3;--coral-400:#D85A30;--coral-600:#993C1D;--coral-800:#712B13;
    --amber-50:#FAEEDA;--amber-100:#FAC775;--amber-600:#854F0B;--amber-800:#633806;
    --green-50:#EAF3DE;--green-400:#639922;--green-600:#3B6D11;--green-800:#27500A;
    --gray-50:#F8F8F6;--gray-100:#EFEFEB;--gray-200:#D3D1C7;--gray-400:#888780;--gray-600:#5F5E5A;
    --bg:#F5F5F2;--card:#FFFFFF;--text:#1a1a1a;--text-2:#5a5a5a;--text-3:#9a9a9a;
    --border:#E0DFD9;--border-2:#C8C7C0;--radius:12px;--radius-sm:8px;--radius-xl:18px;
  }
  body{font-family:'Outfit',sans-serif;background:var(--bg);color:var(--text);padding:2rem;line-height:1.6;min-height:100vh}
  .page{max-width:820px;margin:0 auto}

  /* HERO */
  .hero{background:var(--card);border:1px solid var(--border);border-radius:var(--radius-xl);padding:2rem;margin-bottom:1.5rem;display:flex;gap:1.5rem;align-items:flex-start}
  .avatar{width:72px;height:72px;border-radius:50%;background:var(--teal-400);display:flex;align-items:center;justify-content:center;font-family:'Syne',sans-serif;font-size:24px;font-weight:700;color:#fff;flex-shrink:0;border:3px solid var(--teal-100)}
  .hero-info{flex:1;min-width:0}
  .hero-name{font-family:'Syne',sans-serif;font-size:28px;font-weight:700;margin-bottom:2px;color:var(--text)}
  .hero-role{font-size:12px;color:var(--text-3);letter-spacing:0.07em;text-transform:uppercase;margin-bottom:12px}
  .hero-bio{font-size:14px;color:var(--text-2);line-height:1.65;margin-bottom:16px;max-width:440px}
  .pill-row{display:flex;gap:8px;flex-wrap:wrap}
  .pill{display:inline-flex;align-items:center;gap:6px;font-size:12px;padding:6px 14px;border-radius:20px;border:1px solid;font-weight:400;text-decoration:none;transition:opacity 0.15s}
  .pill:hover{opacity:0.8}
  .pill.green{background:var(--teal-50);color:var(--teal-600);border-color:var(--teal-100)}
  .pill.blue{background:var(--blue-50);color:var(--blue-600);border-color:var(--blue-100)}

  /* STATS */
  .stat-row{display:grid;grid-template-columns:repeat(4,1fr);gap:10px;margin-bottom:1.5rem}
  .stat{background:var(--card);border-radius:var(--radius-sm);padding:16px;border:1px solid var(--border);text-align:center}
  .stat-n{font-family:'Syne',sans-serif;font-size:30px;font-weight:700;color:var(--teal-400);line-height:1}
  .stat-l{font-size:11px;color:var(--text-3);margin-top:5px;letter-spacing:0.02em}

  /* SECTION HEADER */
  .sec-head{font-size:11px;font-weight:500;letter-spacing:0.09em;text-transform:uppercase;color:var(--text-3);margin:0 0 12px;padding-bottom:8px;border-bottom:1px solid var(--border)}

  /* SKILL CARDS */
  .skill-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(148px,1fr));gap:10px;margin-bottom:1.5rem}
  .skill-card{background:var(--card);border:1px solid var(--border);border-radius:var(--radius);padding:16px;transition:border-color 0.2s,transform 0.15s}
  .skill-card:hover{border-color:var(--teal-100);transform:translateY(-2px)}
  .skill-card-icon{width:34px;height:34px;border-radius:9px;display:flex;align-items:center;justify-content:center;font-size:17px;margin-bottom:10px}
  .skill-card-title{font-size:13px;font-weight:500;margin-bottom:9px;color:var(--text)}
  .tag-wrap{display:flex;flex-wrap:wrap;gap:4px}
  .tag{font-size:11px;padding:3px 8px;border-radius:20px;background:var(--gray-50);color:var(--text-2);border:1px solid var(--border)}

  /* FLASHCARDS */
  .fc-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:10px;margin-bottom:1.5rem}
  .fc{border:1px solid var(--border);border-radius:var(--radius);min-height:140px;cursor:pointer;perspective:700px;user-select:none}
  .fc-inner{width:100%;min-height:140px;position:relative;transform-style:preserve-3d;transition:transform 0.5s cubic-bezier(.4,0,.2,1)}
  .fc.flipped .fc-inner{transform:rotateY(180deg)}
  .fc-front,.fc-back{position:absolute;inset:0;backface-visibility:hidden;border-radius:var(--radius);padding:20px;display:flex;flex-direction:column;justify-content:center;align-items:center;text-align:center}
  .fc-back{transform:rotateY(180deg);background:var(--card)}
  .fc-q{font-size:13px;font-weight:500;line-height:1.4;margin-top:8px}
  .fc-a{font-size:12px;color:var(--text-2);line-height:1.55}
  .fc-hint{font-size:10px;color:rgba(0,0,0,0.3);margin-top:8px;letter-spacing:0.04em}
  .fc-back .fc-hint{color:var(--text-3)}

  /* PROJECTS */
  .proj-list{display:flex;flex-direction:column;gap:10px;margin-bottom:1.5rem}
  .proj{background:var(--card);border:1px solid var(--border);border-radius:var(--radius);padding:18px;display:flex;gap:14px;align-items:flex-start;transition:border-color 0.2s,transform 0.15s}
  .proj:hover{border-color:var(--border-2);transform:translateY(-1px)}
  .proj-ico{width:42px;height:42px;border-radius:11px;display:flex;align-items:center;justify-content:center;font-size:19px;flex-shrink:0}
  .proj-body{flex:1;min-width:0}
  .proj-title{font-size:14px;font-weight:500;margin-bottom:5px;color:var(--text)}
  .proj-desc{font-size:12px;color:var(--text-2);line-height:1.6;margin-bottom:11px}
  .proj-stack{display:flex;flex-wrap:wrap;gap:5px}
  .stag{font-size:11px;padding:3px 9px;border-radius:20px;border:1px solid;font-weight:400}

  /* CERTS */
  .cert-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(150px,1fr));gap:10px;margin-bottom:1.5rem}
  .cert{background:var(--card);border-radius:var(--radius-sm);padding:16px;border:1px solid var(--border)}
  .cert-org{font-size:10px;font-weight:500;text-transform:uppercase;letter-spacing:0.07em;color:var(--teal-400);margin-bottom:6px}
  .cert-name{font-size:13px;color:var(--text);line-height:1.4}
  .cert-badge{display:inline-block;margin-top:10px;font-size:10px;padding:3px 9px;border-radius:20px;background:var(--teal-50);color:var(--teal-600);border:1px solid var(--teal-100)}

  /* CONTACT */
  .contact-card{background:var(--card);border:1px solid var(--border);border-radius:var(--radius-xl);padding:1.5rem 2rem;display:flex;align-items:center;justify-content:space-between;flex-wrap:wrap;gap:1rem}
  .contact-q{font-family:'Syne',sans-serif;font-size:17px;color:var(--text)}
  .contact-sub{font-size:13px;color:var(--text-2);margin-top:4px}
  .contact-btns{display:flex;gap:8px;flex-wrap:wrap}
  .cbtn{display:inline-flex;align-items:center;gap:7px;padding:10px 18px;border-radius:var(--radius-sm);font-size:13px;font-weight:500;text-decoration:none;border:1px solid;transition:opacity 0.15s,transform 0.12s;font-family:'Outfit',sans-serif}
  .cbtn:hover{opacity:0.85;transform:translateY(-1px)}
  .cbtn.primary{background:var(--teal-400);color:#fff;border-color:var(--teal-400)}
  .cbtn.ghost{background:transparent;color:var(--text);border-color:var(--border-2)}

  /* SVG icons inline */
  .ico{width:18px;height:18px;stroke:currentColor;fill:none;stroke-width:1.75;stroke-linecap:round;stroke-linejoin:round;vertical-align:-3px}

  @media(max-width:600px){
    body{padding:1rem}
    .hero{flex-direction:column}
    .stat-row{grid-template-columns:repeat(2,1fr)}
    .contact-card{flex-direction:column;align-items:flex-start}
  }
</style>
</head>
<body>
<div class="page">

  <!-- HERO -->
  <div class="hero">
    <div class="avatar">SS</div>
    <div class="hero-info">
      <div class="hero-name">Shakeela Shaik</div>
      <div class="hero-role">Data Analyst &nbsp;·&nbsp; ML Engineer &nbsp;·&nbsp; BI Developer</div>
      <div class="hero-bio">Turning raw, messy data into clean, actionable intelligence. 1+ year of experience across Python, SQL, Power BI, and machine learning — from pipeline to insight.</div>
      <div class="pill-row">
        <a class="pill green" href="https://www.linkedin.com/in/shakeela-shaik-b75b06326/" target="_blank">
          <svg class="ico"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"/><rect x="2" y="9" width="4" height="12"/><circle cx="4" cy="4" r="2"/></svg>
          LinkedIn
        </a>
        <a class="pill blue" href="mailto:shaikshakeela004@gmail.com">
          <svg class="ico"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
          shaikshakeela004@gmail.com
        </a>
        <span class="pill green">
          <svg class="ico"><polyline points="20 6 9 17 4 12"/></svg>
          Open to work
        </span>
      </div>
    </div>
  </div>

  <!-- STATS -->
  <div class="stat-row">
    <div class="stat"><div class="stat-n">1+</div><div class="stat-l">Years experience</div></div>
    <div class="stat"><div class="stat-n">3</div><div class="stat-l">Projects shipped</div></div>
    <div class="stat"><div class="stat-n">4</div><div class="stat-l">Certifications</div></div>
    <div class="stat"><div class="stat-n">8+</div><div class="stat-l">Tools mastered</div></div>
  </div>

  <!-- SKILL CARDS -->
  <div class="sec-head">Skill cards</div>
  <div class="skill-grid">
    <div class="skill-card">
      <div class="skill-card-icon" style="background:var(--teal-50);color:var(--teal-600)">
        <svg class="ico"><polyline points="16 18 22 12 16 6"/><polyline points="8 6 2 12 8 18"/></svg>
      </div>
      <div class="skill-card-title">Languages</div>
      <div class="tag-wrap"><span class="tag">Python</span><span class="tag">SQL</span></div>
    </div>
    <div class="skill-card">
      <div class="skill-card-icon" style="background:var(--blue-50);color:var(--blue-600)">
        <svg class="ico"><rect x="3" y="3" width="18" height="18" rx="2"/><path d="M3 9h18M9 21V9"/></svg>
      </div>
      <div class="skill-card-title">Analysis</div>
      <div class="tag-wrap"><span class="tag">Pandas</span><span class="tag">NumPy</span><span class="tag">EDA</span></div>
    </div>
    <div class="skill-card">
      <div class="skill-card-icon" style="background:var(--amber-50);color:var(--amber-600)">
        <svg class="ico"><line x1="18" y1="20" x2="18" y2="10"/><line x1="12" y1="20" x2="12" y2="4"/><line x1="6" y1="20" x2="6" y2="14"/></svg>
      </div>
      <div class="skill-card-title">Visualization</div>
      <div class="tag-wrap"><span class="tag">Power BI</span><span class="tag">Plotly</span><span class="tag">Seaborn</span></div>
    </div>
    <div class="skill-card">
      <div class="skill-card-icon" style="background:var(--purple-50);color:var(--purple-600)">
        <svg class="ico"><path d="M12 2a10 10 0 1 0 0 20A10 10 0 0 0 12 2z"/><path d="M12 8v4l3 3"/></svg>
      </div>
      <div class="skill-card-title">Machine learning</div>
      <div class="tag-wrap"><span class="tag">Scikit-learn</span><span class="tag">SMOTE</span><span class="tag">Random Forest</span></div>
    </div>
    <div class="skill-card">
      <div class="skill-card-icon" style="background:var(--coral-50);color:var(--coral-600)">
        <svg class="ico"><circle cx="12" cy="12" r="3"/><path d="M19.07 4.93a10 10 0 0 1 0 14.14M4.93 4.93a10 10 0 0 0 0 14.14"/></svg>
      </div>
      <div class="skill-card-title">Tools</div>
      <div class="tag-wrap"><span class="tag">Streamlit</span><span class="tag">FastAPI</span><span class="tag">Git</span></div>
    </div>
    <div class="skill-card">
      <div class="skill-card-icon" style="background:var(--green-50);color:var(--green-600)">
        <svg class="ico"><path d="M22 12h-4l-3 9L9 3l-3 9H2"/></svg>
      </div>
      <div class="skill-card-title">BI &amp; reporting</div>
      <div class="tag-wrap"><span class="tag">Excel</span><span class="tag">DAX</span><span class="tag">MIS</span><span class="tag">KPIs</span></div>
    </div>
  </div>

  <!-- FLASHCARDS -->
  <div class="sec-head">Skill flashcards — click any card to flip</div>
  <div class="fc-grid">
    <div class="fc" onclick="this.classList.toggle('flipped')">
      <div class="fc-inner">
        <div class="fc-front" style="background:var(--teal-50);border:1px solid var(--teal-100)">
          <svg class="ico" style="width:26px;height:26px;color:var(--teal-600)"><ellipse cx="12" cy="12" rx="10" ry="10"/><path d="M12 6v6l4 2"/></svg>
          <div class="fc-q" style="color:var(--teal-800)">What SQL concepts do I use?</div>
          <div class="fc-hint">Click to reveal</div>
        </div>
        <div class="fc-back">
          <div class="fc-a">Joins · CTEs · Window Functions · Subqueries · Aggregations · Indexing</div>
          <div class="fc-hint">Click to flip back</div>
        </div>
      </div>
    </div>
    <div class="fc" onclick="this.classList.toggle('flipped')">
      <div class="fc-inner">
        <div class="fc-front" style="background:var(--blue-50);border:1px solid var(--blue-100)">
          <svg class="ico" style="width:26px;height:26px;color:var(--blue-600)"><line x1="18" y1="20" x2="18" y2="10"/><line x1="12" y1="20" x2="12" y2="4"/><line x1="6" y1="20" x2="6" y2="14"/></svg>
          <div class="fc-q" style="color:var(--blue-800)">What do I build in Power BI?</div>
          <div class="fc-hint">Click to reveal</div>
        </div>
        <div class="fc-back">
          <div class="fc-a">KPI dashboards · DAX measures · YoY reports · Regional breakdowns · MIS tracking</div>
          <div class="fc-hint">Click to flip back</div>
        </div>
      </div>
    </div>
    <div class="fc" onclick="this.classList.toggle('flipped')">
      <div class="fc-inner">
        <div class="fc-front" style="background:var(--purple-50);border:1px solid var(--purple-100)">
          <svg class="ico" style="width:26px;height:26px;color:var(--purple-600)"><rect x="2" y="3" width="20" height="14" rx="2"/><line x1="8" y1="21" x2="16" y2="21"/><line x1="12" y1="17" x2="12" y2="21"/></svg>
          <div class="fc-q" style="color:var(--purple-800)">Which ML models have I used?</div>
          <div class="fc-hint">Click to reveal</div>
        </div>
        <div class="fc-back">
          <div class="fc-a">Logistic Regression · Random Forest · Linear Regression · SMOTE for imbalanced data</div>
          <div class="fc-hint">Click to flip back</div>
        </div>
      </div>
    </div>
    <div class="fc" onclick="this.classList.toggle('flipped')">
      <div class="fc-inner">
        <div class="fc-front" style="background:var(--amber-50);border:1px solid var(--amber-100)">
          <svg class="ico" style="width:26px;height:26px;color:var(--amber-600)"><polyline points="16 18 22 12 16 6"/><polyline points="8 6 2 12 8 18"/></svg>
          <div class="fc-q" style="color:var(--amber-800)">Python libraries for analysis?</div>
          <div class="fc-hint">Click to reveal</div>
        </div>
        <div class="fc-back">
          <div class="fc-a">Pandas · NumPy · Matplotlib · Seaborn · Plotly · Scikit-learn · Streamlit</div>
          <div class="fc-hint">Click to flip back</div>
        </div>
      </div>
    </div>
    <div class="fc" onclick="this.classList.toggle('flipped')">
      <div class="fc-inner">
        <div class="fc-front" style="background:var(--coral-50);border:1px solid var(--coral-100)">
          <svg class="ico" style="width:26px;height:26px;color:var(--coral-600)"><path d="M22 16.92v3a2 2 0 0 1-2.18 2A19.79 19.79 0 0 1 11.64 18a19.79 19.79 0 0 1-4.9-4.9 19.79 19.79 0 0 1-3.93-8.19A2 2 0 0 1 4.81 3h3a2 2 0 0 1 2 1.72c.127.96.361 1.903.7 2.81a2 2 0 0 1-.45 2.11L8.09 10.91a16 16 0 0 0 5 5l1.97-1.97a2 2 0 0 1 2.11-.45c.907.339 1.85.573 2.81.7A2 2 0 0 1 22 16.92z"/></svg>
          <div class="fc-q" style="color:var(--coral-800)">What deployment tools do I use?</div>
          <div class="fc-hint">Click to reveal</div>
        </div>
        <div class="fc-back">
          <div class="fc-a">Streamlit · FastAPI · Flask · Git/GitHub · Jupyter · Google Colab · VS Code</div>
          <div class="fc-hint">Click to flip back</div>
        </div>
      </div>
    </div>
    <div class="fc" onclick="this.classList.toggle('flipped')">
      <div class="fc-inner">
        <div class="fc-front" style="background:var(--green-50);border:1px solid #C0DD97">
          <svg class="ico" style="width:26px;height:26px;color:var(--green-600)"><polyline points="23 6 13.5 15.5 8.5 10.5 1 18"/><polyline points="17 6 23 6 23 12"/></svg>
          <div class="fc-q" style="color:var(--green-800)">What is my core strength?</div>
          <div class="fc-hint">Click to reveal</div>
        </div>
        <div class="fc-back">
          <div class="fc-a">End-to-end analysis: data collection → cleaning → modeling → reporting → stakeholder insight</div>
          <div class="fc-hint">Click to flip back</div>
        </div>
      </div>
    </div>
  </div>

  <!-- PROJECTS -->
  <div class="sec-head">Featured projects</div>
  <div class="proj-list">
    <div class="proj">
      <div class="proj-ico" style="background:var(--teal-50);color:var(--teal-600)">
        <svg class="ico" style="width:20px;height:20px"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/></svg>
      </div>
      <div class="proj-body">
        <div class="proj-title">Credit Card Fraud Detection System</div>
        <div class="proj-desc">End-to-end ML pipeline on a highly imbalanced dataset. Applied SMOTE oversampling and deployed a live Streamlit app for real-time fraud classification with Precision, Recall, and ROC-AUC evaluation.</div>
        <div class="proj-stack">
          <span class="stag" style="background:var(--teal-50);color:var(--teal-800);border-color:var(--teal-100)">Scikit-learn</span>
          <span class="stag" style="background:var(--teal-50);color:var(--teal-800);border-color:var(--teal-100)">SMOTE</span>
          <span class="stag" style="background:var(--blue-50);color:var(--blue-800);border-color:var(--blue-100)">Streamlit</span>
          <span class="stag" style="background:#F5F5F2;color:#5F5E5A;border-color:#D3D1C7">Pandas</span>
        </div>
      </div>
    </div>
    <div class="proj">
      <div class="proj-ico" style="background:var(--blue-50);color:var(--blue-600)">
        <svg class="ico" style="width:20px;height:20px"><line x1="18" y1="20" x2="18" y2="10"/><line x1="12" y1="20" x2="12" y2="4"/><line x1="6" y1="20" x2="6" y2="14"/></svg>
      </div>
      <div class="proj-body">
        <div class="proj-title">Sales Performance Dashboard</div>
        <div class="proj-desc">Multi-page Power BI dashboard with DAX measures for YoY comparison, regional breakdowns, and KPI tracking. Used Power Query for multi-source data transformation and automation.</div>
        <div class="proj-stack">
          <span class="stag" style="background:var(--blue-50);color:var(--blue-800);border-color:var(--blue-100)">Power BI</span>
          <span class="stag" style="background:var(--blue-50);color:var(--blue-800);border-color:var(--blue-100)">DAX</span>
          <span class="stag" style="background:#F5F5F2;color:#5F5E5A;border-color:#D3D1C7">Power Query</span>
          <span class="stag" style="background:#F5F5F2;color:#5F5E5A;border-color:#D3D1C7">Excel</span>
        </div>
      </div>
    </div>
    <div class="proj">
      <div class="proj-ico" style="background:var(--coral-50);color:var(--coral-600)">
        <svg class="ico" style="width:20px;height:20px"><path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"/><circle cx="9" cy="7" r="4"/><path d="M23 21v-2a4 4 0 0 0-3-3.87"/><path d="M16 3.13a4 4 0 0 1 0 7.75"/></svg>
      </div>
      <div class="proj-body">
        <div class="proj-title">Customer Segmentation Analysis</div>
        <div class="proj-desc">Behavioral clustering to identify high-value and at-risk customers from transaction and demographic data. Delivered visual segment reports with actionable business recommendations.</div>
        <div class="proj-stack">
          <span class="stag" style="background:var(--coral-50);color:var(--coral-800);border-color:var(--coral-100)">Pandas</span>
          <span class="stag" style="background:var(--coral-50);color:var(--coral-800);border-color:var(--coral-100)">Plotly</span>
          <span class="stag" style="background:#F5F5F2;color:#5F5E5A;border-color:#D3D1C7">Scikit-learn</span>
          <span class="stag" style="background:#F5F5F2;color:#5F5E5A;border-color:#D3D1C7">Seaborn</span>
        </div>
      </div>
    </div>
  </div>

  <!-- CERTIFICATIONS -->
  <div class="sec-head">Certifications</div>
  <div class="cert-grid">
    <div class="cert">
      <div class="cert-org">NPTEL</div>
      <div class="cert-name">Machine Learning Using Python</div>
      <span class="cert-badge">Verified</span>
    </div>
    <div class="cert">
      <div class="cert-org">TATA · Forage</div>
      <div class="cert-name">Data Visualization</div>
      <span class="cert-badge">Verified</span>
    </div>
    <div class="cert">
      <div class="cert-org">UpGrad</div>
      <div class="cert-name">AI and Data Science</div>
      <span class="cert-badge">Verified</span>
    </div>
    <div class="cert">
      <div class="cert-org">Microsoft · IBM</div>
      <div class="cert-name">Generative AI</div>
      <span class="cert-badge">Verified</span>
    </div>
  </div>

  <!-- CONTACT -->
  <div class="contact-card">
    <div>
      <div class="contact-q">Open to new opportunities</div>
      <div class="contact-sub">Data Analytics · Machine Learning · Business Intelligence</div>
    </div>
    <div class="contact-btns">
      <a class="cbtn primary" href="https://www.linkedin.com/in/shakeela-shaik-b75b06326/" target="_blank">
        <svg class="ico" style="color:#fff"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"/><rect x="2" y="9" width="4" height="12"/><circle cx="4" cy="4" r="2"/></svg>
        Connect on LinkedIn
      </a>
      <a class="cbtn ghost" href="mailto:shaikshakeela004@gmail.com">
        <svg class="ico"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
        Send an email
      </a>
    </div>
  </div>

</div>
</body>
</html>
