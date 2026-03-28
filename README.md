<div>
  <style>
@import url('https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;600;700;800&family=Fira+Code:wght@400;500&display=swap');
@keyframes fadeUp{from{opacity:0;transform:translateY(16px)}to{opacity:1;transform:translateY(0)}}
@keyframes spinRing{from{transform:rotate(0deg)}to{transform:rotate(360deg)}}
@keyframes pulseGlow{0%,100%{box-shadow:0 0 0 0 rgba(139,92,246,.25)}50%{box-shadow:0 0 0 10px rgba(139,92,246,0)}}
@keyframes tagFloat{0%,100%{transform:translateY(0)}50%{transform:translateY(-4px)}}
@keyframes bgMove{0%{background-position:0% 50%}50%{background-position:100% 50%}100%{background-position:0% 50%}}
@keyframes shimmer{0%{background-position:-200% center}100%{background-position:200% center}}
@keyframes blink{0%,100%{opacity:1}50%{opacity:0}}
@keyframes orb1{0%,100%{transform:translate(0,0)}50%{transform:translate(30px,-20px)}}
@keyframes orb2{0%,100%{transform:translate(0,0)}50%{transform:translate(-20px,25px)}}
@keyframes orb3{0%,100%{transform:translate(0,0)}50%{transform:translate(15px,20px)}}
.b3f{font-family:'Plus Jakarta Sans',sans-serif;border-radius:16px;overflow:hidden;position:relative;padding:36px 40px;background:linear-gradient(-45deg,#0f0c29,#302b63,#1a1040,#0d1b3e);background-size:400% 400%;animation:bgMove 10s ease infinite;}
.orb{position:absolute;border-radius:50%;filter:blur(70px);pointer-events:none;}
.orb1{width:240px;height:240px;background:#7c3aed44;top:-70px;left:-50px;animation:orb1 8s ease-in-out infinite;}
.orb2{width:200px;height:200px;background:#0891b244;bottom:-60px;right:80px;animation:orb2 9s ease-in-out infinite;}
.orb3{width:160px;height:160px;background:#db277744;bottom:-40px;left:200px;animation:orb3 11s ease-in-out infinite;}
.b3f-topbar{position:absolute;top:0;left:0;right:0;height:2px;background:linear-gradient(90deg,transparent,#8b5cf6,#06b6d4,#f472b6,#8b5cf6,transparent);}
.b3f-grid{position:absolute;inset:0;background-image:linear-gradient(rgba(255,255,255,.022) 1px,transparent 1px),linear-gradient(90deg,rgba(255,255,255,.022) 1px,transparent 1px);background-size:40px 40px;}
.b3f-bottombar{position:absolute;bottom:0;left:0;right:0;height:1px;background:linear-gradient(90deg,transparent,#4f46e5,#06b6d4,#4f46e5,transparent);}
.b3f-inner{position:relative;z-index:5;display:flex;align-items:center;gap:32px;}
.b3f-av-wrap{flex-shrink:0;position:relative;}
.b3f-ring{position:absolute;inset:-8px;border-radius:50%;border:1.5px solid transparent;background:linear-gradient(#1a1040,#1a1040) padding-box,linear-gradient(135deg,#8b5cf6,#06b6d4,#f472b6,#8b5cf6) border-box;animation:spinRing 5s linear infinite;}
.b3f-ring2{position:absolute;inset:-3px;border-radius:50%;border:1px solid rgba(139,92,246,.2);}
.b3f-avatar{width:86px;height:86px;border-radius:50%;overflow:hidden;position:relative;z-index:2;animation:pulseGlow 3s ease-in-out infinite;}
.b3f-avatar img{width:100%;height:100%;object-fit:cover;}
.b3f-info{flex:1;animation:fadeUp .7s ease .1s both;}
.b3f-name{font-size:26px;font-weight:800;background:linear-gradient(90deg,#fff 0%,#c4b5fd 40%,#67e8f9 80%,#fff 100%);background-size:200%;-webkit-background-clip:text;-webkit-text-fill-color:transparent;animation:shimmer 5s linear infinite;margin-bottom:3px;letter-spacing:-.3px;}
.b3f-role{font-family:'Fira Code',monospace;font-size:12px;color:#a78bfa;letter-spacing:1.5px;margin-bottom:5px;}
.b3f-role::before{content:'// ';color:#64748b;}
.b3f-sub{font-size:11px;color:#64748b;margin-bottom:16px;font-family:'Fira Code',monospace;}
.b3f-sub span{color:#38bdf8;}
.b3f-tags{display:flex;flex-direction:column;gap:7px;}
.b3f-row{display:flex;flex-wrap:wrap;gap:6px;align-items:center;}
.b3f-row-label{font-family:'Fira Code',monospace;font-size:9px;color:#475569;letter-spacing:2px;width:48px;flex-shrink:0;}
.b3f-tag{font-family:'Fira Code',monospace;font-size:10px;padding:4px 11px;border-radius:20px;letter-spacing:.4px;}
.tMongo{background:#052e16;color:#86efac;border:1px solid #166534;animation:tagFloat 3.2s ease-in-out infinite 0s}
.tExpress{background:#1c1c1c;color:#d1d5db;border:1px solid #374151;animation:tagFloat 3.2s ease-in-out infinite .15s}
.tReact{background:#0c2340;color:#7dd3fc;border:1px solid #0369a1;animation:tagFloat 3.2s ease-in-out infinite .3s}
.tNode{background:#052e16;color:#6ee7b7;border:1px solid #065f46;animation:tagFloat 3.2s ease-in-out infinite .45s}
.tNext{background:#18181b;color:#e4e4e7;border:1px solid #3f3f46;animation:tagFloat 3.2s ease-in-out infinite .6s}
.tPG{background:#0c1a3a;color:#93c5fd;border:1px solid #1e40af;animation:tagFloat 3.2s ease-in-out infinite .75s}
.tPrisma{background:#1a0f2e;color:#c4b5fd;border:1px solid #5b21b6;animation:tagFloat 3.2s ease-in-out infinite .9s}
.tTS{background:#0f2847;color:#bfdbfe;border:1px solid #1d4ed8;animation:tagFloat 3.2s ease-in-out infinite 1.05s}
.b3f-right{flex-shrink:0;animation:fadeUp .7s ease .3s both;}
.b3f-card{background:rgba(255,255,255,.04);border:1px solid rgba(255,255,255,.08);border-radius:14px;padding:20px 22px;display:flex;flex-direction:column;gap:11px;backdrop-filter:blur(8px);min-width:192px;}
.b3f-card-title{font-family:'Fira Code',monospace;font-size:9px;color:#475569;letter-spacing:2.5px;margin-bottom:2px;}
.b3f-stat{font-family:'Fira Code',monospace;font-size:11px;color:#94a3b8;display:flex;align-items:center;gap:9px;white-space:nowrap;}
.b3f-stat .val{color:#e2e8f0;}
.b3f-dot{width:6px;height:6px;border-radius:50%;flex-shrink:0;}
.dg{background:#22c55e;box-shadow:0 0 7px #22c55e;animation:blink 2s ease-in-out infinite;}
.dp{background:#a78bfa;box-shadow:0 0 7px #a78bfa;animation:blink 2.5s ease-in-out infinite .5s;}
.dc{background:#06b6d4;box-shadow:0 0 7px #06b6d4;animation:blink 3s ease-in-out infinite 1s;}
.b3f-divider{height:1px;background:rgba(255,255,255,.07);}
.b3f-email{font-family:'Fira Code',monospace;font-size:10px;color:#4b5563;}
</style>
<div class="b3f">
  <div class="orb orb1"></div><div class="orb orb2"></div><div class="orb orb3"></div>
  <div class="b3f-grid"></div><div class="b3f-topbar"></div><div class="b3f-bottombar"></div>
  <div class="b3f-inner">
    <div class="b3f-av-wrap">
      <div class="b3f-ring"></div><div class="b3f-ring2"></div>
      <div class="b3f-avatar">
        <img src="data:image/jpeg;base64,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" alt="Selim"/>
      </div>
    </div>
    <div class="b3f-info">
      <div class="b3f-name">MD Selim Islam</div>
      <div class="b3f-role">Full-Stack Web Developer</div>
      <div class="b3f-sub">Crafting scalable apps · <span>MERN</span> · <span>Next.js</span> · <span>PostgreSQL</span></div>
      <div class="b3f-tags">
        <div class="b3f-row"><span class="b3f-row-label">FRONT</span><span class="b3f-tag tReact">React.js</span><span class="b3f-tag tNext">Next.js</span><span class="b3f-tag tTS">TypeScript</span></div>
        <div class="b3f-row"><span class="b3f-row-label">BACK</span><span class="b3f-tag tNode">Node.js</span><span class="b3f-tag tExpress">Express.js</span></div>
        <div class="b3f-row"><span class="b3f-row-label">DB/ORM</span><span class="b3f-tag tMongo">MongoDB</span><span class="b3f-tag tPG">PostgreSQL</span><span class="b3f-tag tPrisma">Prisma</span></div>
      </div>
    </div>
    <div class="b3f-right">
      <div class="b3f-card">
        <div class="b3f-card-title">// STATUS</div>
        <div class="b3f-stat"><span class="b3f-dot dg"></span><span>status</span><span class="val">open to work</span></div>
        <div class="b3f-stat"><span class="b3f-dot dp"></span><span>focus</span><span class="val">full-stack</span></div>
        <div class="b3f-stat"><span class="b3f-dot dc"></span><span>from</span><span class="val">Bangladesh 🇧🇩</span></div>
        <div class="b3f-divider"></div>
        <div class="b3f-email">✉ salimislam0036@gmail.com</div>
      </div>
    </div>
  </div>
</div>
</div>

<br/>

<p align="center">
  <a href="https://github.com/salim-khan-3">
    <img src="https://komarev.com/ghpvc/?username=salim-khan-3&label=Profile+Views&color=0e75b6&style=flat" alt="profile views"/>
  </a>
  <a href="https://github.com/salim-khan-3?tab=followers">
    <img src="https://img.shields.io/github/followers/salim-khan-3?label=Followers&style=social" alt="followers"/>
  </a>
</p>

---

## 🧑‍💻 About Me

```typescript
const selim = {
  name:     "MD Selim Islam",
  role:     "Full-Stack Web Developer",
  location: "Bangladesh 🇧🇩",
  stack:    ["React.js", "Node.js", "TypeScript", "PostgreSQL", "Prisma", "MongoDB"],
  currently: "Building scalable MERN stack applications",
  learning:  "Advanced TypeScript & System Design",
  email:    "salimislam0036@gmail.com",
  openTo:   "Freelance projects & Full-time opportunities",
};
```

---

## 🛠️ Tech Stack

**Frontend**

![React](https://img.shields.io/badge/React-%2361DAFB.svg?style=for-the-badge&logo=react&logoColor=black)
![Next.js](https://img.shields.io/badge/Next.js-%23000000.svg?style=for-the-badge&logo=nextdotjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-%233178C6.svg?style=for-the-badge&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-%23F7DF1E.svg?style=for-the-badge&logo=javascript&logoColor=black)
![TailwindCSS](https://img.shields.io/badge/Tailwind-%2306B6D4.svg?style=for-the-badge&logo=tailwindcss&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white)

**Backend**

![Node.js](https://img.shields.io/badge/Node.js-%23339933.svg?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Express.js](https://img.shields.io/badge/Express.js-%23000000.svg?style=for-the-badge&logo=express&logoColor=white)
![REST API](https://img.shields.io/badge/REST%20API-%23FF6C37.svg?style=for-the-badge&logo=postman&logoColor=white)

**Database & ORM**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-%234169E1.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-%2347A248.svg?style=for-the-badge&logo=mongodb&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-%232D3748.svg?style=for-the-badge&logo=prisma&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-%23FFCA28.svg?style=for-the-badge&logo=firebase&logoColor=black)

**Tools & Platforms**

![Git](https://img.shields.io/badge/Git-%23F05032.svg?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-%23181717.svg?style=for-the-badge&logo=github&logoColor=white)
![VS Code](https://img.shields.io/badge/VS%20Code-%230078D4.svg?style=for-the-badge&logo=visualstudiocode&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-%23000000.svg?style=for-the-badge&logo=vercel&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-%23FF6C37.svg?style=for-the-badge&logo=postman&logoColor=white)
![Figma](https://img.shields.io/badge/Figma-%23F24E1E.svg?style=for-the-badge&logo=figma&logoColor=white)

---

## 📊 GitHub Stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=salim-khan-3&show_icons=true&theme=tokyonight&hide_border=true&bg_color=070b14&title_color=06b6d4&icon_color=06b6d4&text_color=e2e8f0&rank_icon=github" width="49%"/>
  <img src="https://github-readme-streak-stats.herokuapp.com?user=salim-khan-3&theme=tokyonight&hide_border=true&background=070b14&ring=06b6d4&fire=10b981&currStreakLabel=06b6d4&sideLabels=e2e8f0&dates=64748b&sideNums=e2e8f0&currStreakNum=06b6d4" width="49%"/>
</p>

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=salim-khan-3&layout=compact&theme=tokyonight&hide_border=true&bg_color=070b14&title_color=06b6d4&text_color=e2e8f0&langs_count=8" width="40%"/>
</p>

---

## 🏆 GitHub Achievements

<p align="center">
  <img src="https://github-profile-trophy.vercel.app/?username=salim-khan-3&theme=tokyonight&no-frame=true&no-bg=true&margin-w=6&column=6"/>
</p>

---

## 📈 Contribution Graph

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=salim-khan-3&bg_color=070b14&color=06b6d4&line=10b981&point=06b6d4&area=true&hide_border=true" width="100%"/>
</p>

---

## 📌 Featured Projects

<p align="center">
  <a href="https://github.com/salim-khan-3/fullstack-ecommerce-react-side">
    <img src="https://github-readme-stats.vercel.app/api/pin/?username=salim-khan-3&repo=fullstack-ecommerce-react-side&theme=tokyonight&hide_border=true&bg_color=070b14&title_color=06b6d4&icon_color=10b981&text_color=e2e8f0" width="48%"/>
  </a>
  <a href="https://github.com/salim-khan-3/fullstack-ecommerce-mern-ser">
    <img src="https://github-readme-stats.vercel.app/api/pin/?username=salim-khan-3&repo=fullstack-ecommerce-mern-ser&theme=tokyonight&hide_border=true&bg_color=070b14&title_color=06b6d4&icon_color=10b981&text_color=e2e8f0" width="48%"/>
  </a>
</p>

---

## 🤝 Connect With Me

<p align="center">
  <a href="mailto:salimislam0036@gmail.com">
    <img src="https://img.shields.io/badge/Gmail-salimislam0036%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white"/>
  </a>
  &nbsp;
  <a href="https://github.com/salim-khan-3">
    <img src="https://img.shields.io/badge/GitHub-salim--khan--3-181717?style=for-the-badge&logo=github&logoColor=white"/>
  </a>
</p>

<br/>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,12,20&height=80&section=footer"/>
</p>

