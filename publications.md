---
layout: page
permalink: /publications/index.html
title: Publications
---

Latest Update: Oct 2025

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Publications</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css"/>
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/jpswalsh/academicons@1.9.4/css/academicons.min.css"/>
  <style>
    :root{
      --bg:#f7f8fa;
      --panel:#fff;
      --text:#1f2937;
      --muted:#6b7280;
      --brand:#2563eb;
      --brand-600:#1d4ed8;
      --accent:#10b981;
      --shadow:0 2px 12px rgba(0,0,0,.06);
      --radius:10px;

      --btn-font:.85rem;
      --icon-size:.95rem;
      --link:#1a73e8;
      --link-hover:#0d62d9;
    }
    *{box-sizing:border-box}
    body{
      margin:0; padding:24px;
      font-family: Inter, "Segoe UI", Roboto, Helvetica, Arial, "Apple Color Emoji","Segoe UI Emoji", system-ui, -apple-system;
      background:var(--bg); color:var(--text);
    }
    .container{ max-width:960px; margin:0 auto; }

    .section-title{
      font-family: Georgia, "Times New Roman", Times, serif;
      display:flex; align-items:center; gap:10px;
      font-weight:700; font-size:1.4rem;
      border-bottom:2px solid var(--brand);
      padding-bottom:8px; margin:8px 0 18px;
      color:#0f172a;
    }
    .panel{ background:var(--panel); border-radius:10px; box-shadow:var(--shadow); padding:20px; }

    /* Preprints list */
    .pub-list{ list-style:none; margin:0; padding:0; }
    .pub-item{
      display:grid; grid-template-columns:1fr auto; gap:10px 16px;
      padding:14px 0; border-bottom:1px solid #e5e7eb;
    }
    .pub-item:last-child{ border-bottom:none; padding-bottom:0; }
    .meta{ display:flex; align-items:center; gap:8px; flex-wrap:wrap; }
    .badge{
      font-size:.72rem; font-weight:700; letter-spacing:.02em;
      padding:2px 8px; border-radius:999px; user-select:none;
      background:#fde68a; color:#92400e; border:1px solid #f59e0b;
    }
    .badge.success{ background:#d1fae5; color:#065f46; border-color:#10b981; }
    .badge.info{ background:#dbeafe; color:#1e40af; border-color:#3b82f6; }
    .title{ font-weight:700; color:#0f172a; line-height:1.4; }
    .title em{ font-style:italic; font-weight:600; color:#1f2937; }
    .authors{ color:var(--muted); }
    .authors strong{ color: inherit; font-weight: 800; } /* 本人仅加粗 */

    .links{ display:flex; gap:6px; flex-wrap:wrap; margin-top:8px; }
    .btn{
      display:inline-flex; align-items:center; gap:6px;
      padding:5px 10px; text-decoration:none; border-radius:7px; font-weight:600;
      font-size: var(--btn-font); border:1px solid transparent; transition:.2s;
    }
    .btn i{ font-size: var(--icon-size); }
    .btn.arxiv{ background:var(--brand); color:#fff; border-color:var(--brand); }
    .btn.arxiv:hover{ background:var(--brand-600); transform:translateY(-1px); }
    .btn.pdf{ background:#f8fafc; color:#b91c1c; border-color:#e5e7eb; }
    .btn.pdf:hover{ background:#f1f5f9; border-color:#ef4444; transform:translateY(-1px); }
    .btn.cite{ background:#ecfeff; color:#0f766e; border-color:#67e8f9; }
    .btn.cite:hover{ background:#cffafe; transform:translateY(-1px); }

    .right{ display:flex; flex-direction:column; align-items:flex-end; gap:6px; white-space:nowrap; }
    .year{ color:#0f172a; font-weight:700; font-size:.95rem; }
    .status{ font-size:.8rem; color:#334155; }

    /* Modal */
    .modal{ position:fixed; inset:0; display:none; align-items:center; justify-content:center; background:rgba(0,0,0,.45); z-index:1000; padding:16px; }
    .modal[aria-hidden="false"]{ display:flex; }
    .dialog{ background:#fff; border-radius:12px; box-shadow:var(--shadow); width:100%; max-width:720px; padding:20px; position:relative; }
    .dialog h3{ margin:0 0 10px; font-size:1.2rem; }
    .close{ position:absolute; top:10px; right:10px; background:none; border:none; font-size:1.1rem; cursor:pointer; color:#6b7280; }
    .format-switch{ display:flex; gap:8px; margin:8px 0 10px; }
    .pill{ padding:4px 10px; border-radius:999px; border:1px solid #e5e7eb; background:#f8fafc; color:#334155; cursor:pointer; font-size:.82rem; }
    .pill.active{ background:#1f2937; color:#fff; border-color:#1f2937; }
    .code{ background:#0b1020; color:#dbeafe; font-family: ui-monospace,SFMono-Regular,Menlo,Consolas,monospace; border-radius:8px; padding:12px; white-space:pre-wrap; line-height:1.6; min-height:120px; border-left:4px solid var(--brand); font-size:.9rem; }
    .actions{ display:flex; gap:8px; margin-top:10px; }
    .copy{ background:var(--brand); color:#fff; border:none; padding:8px 12px; border-radius:8px; cursor:pointer; font-weight:700; }
    .copy.success{ background:var(--accent); }
    .hint{ color:#64748b; font-size:.85rem; margin-top:4px; }

    /* Published papers (静态列表的样式统一) */
    .published{
      margin-top:28px;
    }
    .published h3{
      margin:0 0 12px;
      font-family: Georgia, "Times New Roman", Times, serif;
      font-size:1.25rem; font-weight:700; color:#0f172a;
      border-bottom:1px solid #e5e7eb; padding-bottom:6px;
    }
    .pub-plain{ list-style:none; padding:0; margin:0; }
    .pub-plain li{
      padding:10px 0; border-bottom:1px solid #eef2f7; line-height:1.6;
    }
    .pub-plain li:last-child{ border-bottom:none; }
    .pub-plain i{ font-style:italic; }
    .pub-plain a{
      color: var(--link); text-decoration: none; border-bottom: 1px dotted rgba(26,115,232,.35);
    }
    .pub-plain a:hover{
      color: var(--link-hover); border-bottom-color: rgba(13,98,217,.6);
    }
    .pub-plain strong{ font-weight:800; color: inherit; } /* 本人仅加粗 */

    @media (max-width: 720px){
      body{ padding:16px; }
      .pub-item{ grid-template-columns:1fr; }
      .right{ align-items:flex-start; }
    }
    .btn, .close, .pill, .copy, .cite-btn:focus{ outline:2px solid transparent; outline-offset:2px; }
    .btn:focus-visible, .close:focus-visible, .pill:focus-visible, .copy:focus-visible{ outline-color:#60a5fa; }
  </style>
</head>
<body>
  <main class="container">
    <!-- Preprints -->
    <section class="panel" aria-labelledby="preprints-title">
      <h2 id="preprints-title" class="section-title">
        <i class="fas fa-file-alt" aria-hidden="true"></i>
        Preprints
      </h2>
      <ul id="pubList" class="pub-list" aria-live="polite"></ul>
    </section>

    <!-- Published papers -->
    <section class="published">
      <h3>Published papers</h3>
      <ul class="pub-plain">
        <li>Zhongting Xu, <strong>Zhengjie Sun*</strong> and Shengliang Zhang. A meshless energy-preserving scheme for conservative partial differential equations using kernel-based Galerkin methods, <i>Engineering Analysis with Boundary Elements</i>, 183, 106615, 2026.</li>

        <li><strong>Zhengjie Sun</strong> and Yuyan Gao*. A meshless structure-preserving quasi-interpolation method for the Allen-Cahn equation on spheres, <i>Mathematics and Computers in Simulation</i>, 241, 31-47, 2026.</li>

        <li><strong>Zhengjie Sun</strong>, Wenwu Gao* and Xingping Sun. Scaled zonal kernel quasi-interpolation on spheres, <i>IMA Journal of Numerical Analysis</i>, doi.org/10.1093/imanum/draf104, 2025. (<a href="https://arxiv.org/abs/2408.14803" target="_blank" rel="noopener">arXiv:2408.14803</a>)</li>

        <li><strong>Zhengjie Sun</strong>, Leevan Ling and Ran Zhang*. Learning PDEs from data on closed surfaces with sparse optimization, <i>Communications in Computational Physics</i>, 37:289-314, 2025. (<a href="https://arxiv.org/abs/2405.06199" target="_blank" rel="noopener">arXiv:2405.06199</a>)</li>

        <li>Qinjiao Gao, <strong>Zhengjie Sun*</strong> and Zongmin Wu. Energy-equidistributed moving mesh strategies for simulating Hamiltonian partial differential equations, <i>Applied Mathematics Letters</i>, 163, 109460, 2025.</li>

        <li><strong>Zhengjie Sun*</strong>, Leevan Ling and Meng Chen. Structure-preserving kernel-based methods for solving dissipative PDEs on surfaces, <i>Journal of Scientific Computing</i>, 102(3):70, 2025. (<a href="https://arxiv.org/abs/2312.17478" target="_blank" rel="noopener">arXiv:2312.17478</a>)</li>

        <li>Wenwu Gao, Jiecheng Wang, <strong>Zhengjie Sun*</strong> and Gregory E. Fasshauer. Quasi-interpolation for high-dimensional function approximation, <i>Numerische Mathematik</i>, 156:1855–1885, 2024. (<a href="https://arxiv.org/abs/2409.14278" target="_blank" rel="noopener">arXiv:2409.14278</a>)</li>

        <li><strong>Zhengjie Sun*</strong> and Leevan Ling. A high-order meshless linearly implicit energy-preserving method for nonlinear wave equations on Riemannian manifolds, <i>SIAM Journal on Scientific Computing</i>, 46(6):A3779-3802, 2024.</li>

        <li><strong>Zhengjie Sun</strong> and Qinjiao Gao*. Energy-preserving schemes for conservative PDEs based on periodic quasi-interpolation methods, <i>Communications in Nonlinear Science and Numerical Simulation</i>, 131, 107831, 2024.</li>

        <li><strong>Zhengjie Sun*</strong> and Yuyan Gao. High order multiquadric trigonometric quasi-interpolation method for solving time-dependent partial differential equations, <i>Numerical Algorithms</i>, 93:1719-1739, 2023.</li>

        <li><strong>Zhengjie Sun</strong> and Shengliang Zhang*. A radial basis function approximation method for conservative Allen-Cahn equations on surfaces, <i>Applied Mathematics Letters</i>, 143, 108634, 2023.</li>

        <li>Shengliang Zhang, <strong>Zhengjie Sun*</strong> and Alpesh Kumar. Meshless symplectic and multi-symplectic scheme for the coupled nonlinear Schrödinger system based on local RBF approximation, <i>Computers & Mathematics with Applications</i>, 134:16-32, 2023.</li>

        <li><strong>Zhengjie Sun*</strong> and Yuyan Gao. A meshless quasi-interpolation method for solving hyperbolic conservation laws based on the essentially non-oscillatory reconstruction, <i>International Journal of Computer Mathematics</i>, 100(6):1303-1320, 2023.</li>

        <li><strong>Zhengjie Sun</strong> and Leevan Ling*. A kernel-based meshless conservative Galerkin method for solving Hamiltonian wave equations, <i>SIAM Journal on Scientific Computing</i>, 44(4):A2789-2807, 2022.</li>

        <li><strong>Zhengjie Sun</strong>, Wenwu Gao and Ran Yang*. A convergent iterated quasi-interpolation for periodic domain and its applications to surface PDEs, <i>Journal of Scientific Computing</i>, 93(2):37, 2022.</li>

        <li><strong>Zhengjie Sun*</strong>. A conservative scheme for two-dimensional Schrödinger equation based on multi-quadric trigonometric quasi-interpolation approach, <i>Applied Mathematics and Computation</i>, 423, 2022, 12pp.</li>

        <li>Yuyan Gao and <strong>Zhengjie Sun*</strong>. Multi-symplectic quasi-interpolation method for the KdV equation, <i>Computational and Applied Mathematics</i>, 41(3):112, 17pp, 2022.</li>

        <li><strong>Zhengjie Sun</strong>, Zongmin Wu and Wenwu Gao*. An iterated quasi-interpolation approach for derivative approximation, <i>Numerical Algorithms</i>, 85:255-276, 2020.</li>

        <li><strong>Zhengjie Sun*</strong>. Multi-symplectic quasi-interpolation method for Hamiltonian partial differential equations, <i>Journal of Computational Physics</i>, 395:125-143, 2019.</li>

        <li>Wenwu Gao and <strong>Zhengjie Sun*</strong>. High-order numerical solution of time-dependent differential equations with quasi-interpolation, <i>Applied Numerical Mathematics</i>, 146:276-290, 2019.</li>

        <li><strong>Zhengjie Sun*</strong>. A meshless symplectic method for two-dimensional nonlinear Schrödinger equations based on radial basis function approximation, <i>Engineering Analysis with Boundary Elements</i>, 104:1-7, 2019.</li>

        <li><strong>Zhengjie Sun</strong> and Zongmin Wu*. Meshless conservative schemes for multivariate Hamiltonian partial differential equations, <i>Journal of Scientific Computing</i>, 76:1168-1187, 2018.</li>

        <li><strong>Zhengjie Sun</strong> and Wenwu Gao*. A energy-momentum conserving scheme for Hamiltonian wave equation based on multiquadric trigonometric quasi-interpolation, <i>Applied Mathematical Modelling</i>, 57:179-191, 2018.</li>

        <li><strong>Zhengjie Sun*</strong>. Conservative or dissipative quasi-interpolation method for evolutionary partial differential equations, <i>Engineering Analysis with Boundary Elements</i>, 96:78-83, 2018.</li>
        
        <li><strong>Zhengjie Sun</strong> and Wenwu Gao*. A meshless scheme for Hamiltonian partial differential equations with conservation properties, <i>Applied Numerical Mathematics</i>, 119:115-125, 2017.</li>
      </ul>
    </section>
  </main>

  <!-- Citation Modal -->
  <div id="citeModal" class="modal" role="dialog" aria-modal="true" aria-hidden="true" aria-labelledby="citeTitle">
    <div class="dialog">
      <button id="closeModal" class="close" aria-label="Close citation dialog">
        <i class="fas fa-times"></i>
      </button>
      <h3 id="citeTitle">Citation</h3>
      <div class="format-switch" role="tablist" aria-label="Citation format">
        <button class="pill active" role="tab" aria-selected="true" id="tab-apa">APA</button>
        <button class="pill" role="tab" aria-selected="false" id="tab-bib">BibTeX</button>
      </div>
      <pre id="citeContent" class="code" tabindex="0"></pre>
      <div class="actions">
        <button id="copyBtn" class="copy"><i class="fas fa-copy"></i> Copy</button>
      </div>
      <div class="hint">Tip: Press Ctrl/Cmd+C to copy selected text if the button fails.</div>
    </div>
  </div>

  <script>
    // Preprints data
    const publications = [
      {
        id: 'sun2025monte',
        year: 2025,
        status: 'Submitted',
        statusBadge: 'info',
        authorsHTML: '<strong>Zhengjie Sun*</strong>, Mengyuan Lv, and Xingping Sun',
        titleHTML: 'Monte Carlo quasi-interpolation of spherical data',
        arxivId: '2510.12027',
        arxivAbs: 'https://arxiv.org/abs/2510.12027',
        pdf: 'https://arxiv.org/pdf/2510.12027.pdf',
        apa: 'Sun, Z., Lv, M., & Sun, X. (2025). Monte Carlo quasi-interpolation of spherical data. arXiv preprint arXiv:2510.12027.',
        bibtex:
`@article{sun2025monte,
  title={Monte Carlo quasi-interpolation of spherical data},
  author={Sun, Zhengjie and Lv, Mengyuan and Sun, Xingping},
  journal={arXiv preprint arXiv:2510.12027},
  year={2025}
}`
      },
      {
        id: 'sun2025inverse',
        year: 2025,
        status: 'Submitted',
        statusBadge: 'info',
        authorsHTML: '<strong>Zhengjie Sun*</strong> and Leevan Ling',
        titleHTML: 'Inverse inequalities for kernel-based approximation on bounded domains and Riemannian manifolds',
        arxivId: '2508.05376',
        arxivAbs: 'https://arxiv.org/abs/2508.05376',
        pdf: 'https://arxiv.org/pdf/2508.05376.pdf',
        apa: 'Sun, Z., & Ling, L. (2025). Inverse inequalities for kernel-based approximation on bounded domains and Riemannian manifolds. arXiv preprint arXiv:2508.05376.',
        bibtex:
`@article{sun2025inverse,
  title={Inverse inequalities for kernel-based approximation on bounded domains and Riemannian manifolds},
  author={Sun, Zhengjie and Ling, Leevan},
  journal={arXiv preprint arXiv:2508.05376},
  year={2025}
}`
      },
      {
        id: 'gao2024quasi',
        year: 2024,
        status: 'Submitted',
        statusBadge: 'info',
        authorsHTML: 'Wenwu Gao, Le Hu, <strong>Zhengjie Sun*</strong>, and Changwei Wang',
        titleHTML: 'Quasi-interpolation using generalized Gaussian kernels',
        arxivId: '2407.21283',
        arxivAbs: 'https://arxiv.org/abs/2407.21283',
        pdf: 'https://arxiv.org/pdf/2407.21283.pdf',
        apa: 'Gao, W., Hu, L., Sun, Z., & Wang, C. (2024). Quasi-interpolation using generalized Gaussian kernels. arXiv preprint arXiv:2407.21283.',
        bibtex:
`@article{gao2024quasi,
  title={Quasi-interpolation using generalized Gaussian kernels},
  author={Gao, Wenwu and Hu, Le and Sun, Zhengjie and Wang, Changwei},
  journal={arXiv preprint arXiv:2407.21283},
  year={2024}
}`
      }
    ];

    // Render Preprints
    const listEl = document.getElementById('pubList');
    function renderList(items){
      listEl.innerHTML = '';
      items.sort((a,b)=> b.year - a.year || a.titleHTML.localeCompare(b.titleHTML));
      for(const p of items){
        const li = document.createElement('li'); li.className='pub-item';
        const left = document.createElement('div');
        const meta = document.createElement('div'); meta.className='meta';
        const badge = document.createElement('span'); badge.className='badge '+(p.statusBadge||''); badge.textContent=p.status||''; meta.appendChild(badge);
        const title = document.createElement('div'); title.className='title'; title.innerHTML=`<em>${p.titleHTML}</em>`;
        const authors = document.createElement('div'); authors.className='authors'; authors.innerHTML=p.authorsHTML;
        const links = document.createElement('div'); links.className='links';
        if(p.arxivAbs){ const a=document.createElement('a'); a.className='btn arxiv'; a.href=p.arxivAbs; a.target='_blank'; a.rel='noopener'; a.innerHTML=`<i class="ai ai-arxiv"></i> arXiv:${p.arxivId}`; links.appendChild(a); }
        if(p.pdf){ const a=document.createElement('a'); a.className='btn pdf'; a.href=p.pdf; a.target='_blank'; a.rel='noopener'; a.innerHTML=`<i class="fas fa-file-pdf"></i> PDF`; links.appendChild(a); }
        const cite=document.createElement('button'); cite.className='btn cite cite-btn'; cite.type='button'; cite.dataset.id=p.id; cite.innerHTML=`<i class="fas fa-quote-right"></i> Cite`; links.appendChild(cite);
        left.appendChild(meta); left.appendChild(title); left.appendChild(authors); left.appendChild(links);

        const right=document.createElement('div'); right.className='right';
        right.innerHTML=`<div class="year">${p.year}</div><div class="status">${p.status||''}</div>`;

        li.appendChild(left); li.appendChild(right); listEl.appendChild(li);
      }
    }
    renderList(publications);

    // Modal logic
    const modal=document.getElementById('citeModal');
    const closeBtn=document.getElementById('closeModal');
    const citeContent=document.getElementById('citeContent');
    const copyBtn=document.getElementById('copyBtn');
    const tabAPA=document.getElementById('tab-apa');
    const tabBib=document.getElementById('tab-bib');
    let currentPub=null;

    function openModal(pubId){
      currentPub=publications.find(p=>p.id===pubId);
      if(!currentPub) return;
      setFormat('apa');
      modal.setAttribute('aria-hidden','false');
      document.body.style.overflow='hidden';
      citeContent.focus();
    }
    function closeModal(){
      modal.setAttribute('aria-hidden','true');
      document.body.style.overflow='auto';
    }
    function setFormat(fmt){
      if(!currentPub) return;
      if(fmt==='apa'){
        tabAPA.classList.add('active'); tabAPA.setAttribute('aria-selected','true');
        tabBib.classList.remove('active'); tabBib.setAttribute('aria-selected','false');
        citeContent.textContent=currentPub.apa||'N/A';
      }else{
        tabBib.classList.add('active'); tabBib.setAttribute('aria-selected','true');
        tabAPA.classList.remove('active'); tabAPA.setAttribute('aria-selected','false');
        citeContent.textContent=currentPub.bibtex||'N/A';
      }
    }
    document.addEventListener('click',(e)=>{
      const btn=e.target.closest('.cite-btn');
      if(btn){ e.preventDefault(); openModal(btn.dataset.id); }
    });
    tabAPA.addEventListener('click',()=>setFormat('apa'));
    tabBib.addEventListener('click',()=>setFormat('bib'));
    closeBtn.addEventListener('click',closeModal);
    modal.addEventListener('click',(e)=>{ if(e.target===modal) closeModal(); });
    document.addEventListener('keydown',(e)=>{ if(e.key==='Escape' && modal.getAttribute('aria-hidden')==='false') closeModal(); });

    async function copyTextFallback(text){
      try{
        if(navigator.clipboard && window.isSecureContext){
          await navigator.clipboard.writeText(text); return true;
        }
      }catch{}
      const tmp=document.createElement('textarea'); tmp.value=text; tmp.style.position='fixed'; tmp.style.left='-9999px'; document.body.appendChild(tmp);
      tmp.focus(); tmp.select(); const ok=document.execCommand('copy'); document.body.removeChild(tmp); return ok;
    }
    copyBtn.addEventListener('click', async()=>{
      const ok=await copyTextFallback(citeContent.textContent);
      copyBtn.classList.toggle('success',ok);
      copyBtn.innerHTML= ok ? '<i class="fas fa-check"></i> Copied' : '<i class="fas fa-copy"></i> Copy failed';
      setTimeout(()=>{ copyBtn.classList.remove('success'); copyBtn.innerHTML='<i class="fas fa-copy"></i> Copy'; }, 1800);
    });
  </script>
</body>
</html>
