---
layout: page
permalink: /publications/index.html
title: Publications
---

Latest Update: Oct 2025


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
      --danger:#dc2626;
      --shadow:0 2px 12px rgba(0,0,0,.06);
      --radius:10px;
      --btn-font:.85rem;
      --icon-size:.95rem;
    }
    *{box-sizing:border-box}
    body{
      margin:0; padding:24px;
      font-family: Inter, "Segoe UI", Roboto, Helvetica, Arial, "Apple Color Emoji","Segoe UI Emoji", system-ui, -apple-system;
      background:var(--bg); color:var(--text);
    }
    /* 更宽容器 + 响应式分级 */
    .container{ max-width:1200px; margin:0 auto; }
    @media (min-width:1024px){ .container{ max-width:1280px; } }
    @media (min-width:1280px){
      .container{ max-width:1400px; }
      body{ padding-left:32px; padding-right:32px; }
    }
    @media (min-width:1536px){ .container{ max-width:1500px; } }

    .section-title{
      font-family: Georgia, "Times New Roman", Times, serif;
      display:flex; align-items:center; gap:10px;
      font-weight:700; font-size:1.4rem;
      border-bottom:2px solid var(--brand);
      padding-bottom:8px; margin:8px 0 18px;
      color:#0f172a;
    }
    .panel{ background:var(--panel); border-radius:10px; box-shadow:var(--shadow); padding:20px; }

    /* 统一的 publication card 基础样式 */
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
      background:#e5e7eb; color:#374151; border:1px solid #d1d5db;
    }
    .badge.info{ background:#dbeafe; color:#1e40af; border-color:#3b82f6; }
    .badge.success{ background:#d1fae5; color:#065f46; border-color:#10b981; }
    .badge.warn{ background:#fee2e2; color:#991b1b; border-color:#ef4444; }

    .title{ font-weight:700; color:#0f172a; line-height:1.4; }
    .title em{ font-style:italic; font-weight:600; color:#1f2937; }
    .venue{ color:#334155; font-size:.9rem; margin-top:4px; } /* 发表期刊放到左侧标题下 */
    .authors{ color:var(--muted); margin-top:2px; }
    .authors strong{ font-weight:800; }

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
    .btn.doi{ background:#eef2ff; color:#3730a3; border-color:#c7d2fe; }
    .btn.doi:hover{ background:#e0e7ff; transform:translateY(-1px); }
    .btn.cite{ background:#ecfeff; color:#0f766e; border-color:#67e8f9; }
    .btn.cite:hover{ background:#cffafe; transform:translateY(-1px); }

    .right{ display:flex; flex-direction:column; align-items:flex-end; gap:4px; text-align:right; }
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

    @media (max-width: 720px){
      body{ padding:16px; }
      .pub-item{ grid-template-columns:1fr; }
      .right{ align-items:flex-start; text-align:left; }
    }
    .btn, .close, .pill, .copy, .cite-btn:focus{ outline:2px solid transparent; outline-offset:2px; }
    .btn:focus-visible, .close:focus-visible, .pill:focus-visible, .copy:focus-visible{ outline-color:#60a5fa; }
  </style>
</head>
<body>
  <main class="container">
    <!-- Preprints（保持原布局） -->
    <section class="panel" aria-labelledby="preprints-title">
      <h2 id="preprints-title" class="section-title">
        <i class="fas fa-flask" aria-hidden="true"></i>
        Preprints
      </h2>
      <ul id="preprintsList" class="pub-list" aria-live="polite"></ul>
    </section>

    <!-- Published（修改后的布局：右侧仅年份；venue 在标题下方） -->
    <section class="panel" aria-labelledby="published-title" style="margin-top:20px;">
      <h2 id="published-title" class="section-title">
        <i class="fas fa-book-open" aria-hidden="true"></i>
        Published papers
      </h2>
      <ul id="publishedList" class="pub-list" aria-live="polite"></ul>
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
    // 统一数据模型（示例含多条；可继续补充/修改）
    const pubs = [
      // Preprints
      {
        id: 'sun2025monte',
        type: 'preprint',
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
        type: 'preprint',
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
        type: 'preprint',
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
      },



      
      // Published
      {
        id: 'xu2026eabe',
        type: 'published',
        year: 2026,
        status: 'Published',
        statusBadge: 'success',
        authorsHTML: 'Zhongting Xu, <strong>Zhengjie Sun*</strong> and Shengliang Zhang',
        titleHTML: 'A meshless energy-preserving scheme for conservative partial differential equations using kernel-based Galerkin methods',
        venue: 'Engineering Analysis with Boundary Elements, 183, 106615',
        doiLink: 'https://doi.org/10.1016/j.enganabound.2025.106615',
        apa: 'Xu, Z., Sun, Z., & Zhang, S. (2026). A meshless energy-preserving scheme for conservative partial differential equations using kernel-based Galerkin methods. Engineering Analysis with Boundary Elements, 183, 106615.',
        bibtex:
`@article{xu2026meshless,
  title={A meshless energy-preserving scheme for conservative partial differential equations using kernel-based Galerkin methods},
  author={Xu, Zhongting and Sun, Zhengjie and Zhang, Shengliang},
  journal={Engineering Analysis with Boundary Elements},
  volume={183},
  pages={106615},
  year={2026},
  publisher={Elsevier},
  doi={10.1016/j.enganabound.2026.106615}
}`
      },
      {
        id: 'sun2026macs',
        type: 'published',
        year: 2026,
        status: 'Published',
        statusBadge: 'success',
        authorsHTML: '<strong>Zhengjie Sun</strong> and Yuyan Gao*',
        titleHTML: 'A meshless structure-preserving quasi-interpolation method for the Allen-Cahn equation on spheres',
        venue: 'Mathematics and Computers in Simulation, 241, 31–47',
        doiLink: 'https://doi.org/10.1016/j.matcom.2025.09.031',
        apa: 'Sun, Z., & Gao, Y. (2026). A meshless structure-preserving quasi-interpolation method for the Allen-Cahn equation on spheres. Mathematics and Computers in Simulation, 241, 31–47.',
        bibtex:
`@article{sun2026allen,
  title={A meshless structure-preserving quasi-interpolation method for the Allen-Cahn equation on spheres},
  author={Sun, Zhengjie and Gao, Yuyan},
  journal={Mathematics and Computers in Simulation},
  volume={241},
  pages={31--47},
  year={2026}
}`
      },
      {
        id: 'sun2025imanum',
        type: 'published',
        year: 2025,
        status: 'Published',
        statusBadge: 'success',
        authorsHTML: '<strong>Zhengjie Sun</strong>, Wenwu Gao* and Xingping Sun',
        titleHTML: 'Scaled zonal kernel quasi-interpolation on spheres',
        venue: 'IMA Journal of Numerical Analysis, doi.org/10.1093/imanum/draf104',
        doiLink: 'https://doi.org/10.1093/imanum/draf104',
        arxivId: '2408.14803',
        arxivAbs: 'https://arxiv.org/abs/2408.14803',
        pdf: 'https://arxiv.org/pdf/2408.14803v2.pdf',
        apa: 'Sun, Z., Gao, W., & Sun, X. (2025). Scaled zonal kernel quasi-interpolation on spheres. IMA Journal of Numerical Analysis. https://doi.org/10.1093/imanum/draf104',
        bibtex:
`@article{sun2025scaled,
  title={Scaled zonal kernel quasi-interpolation on spheres},
  author={Sun, Zhengjie and Gao, Wenwu and Sun, Xingping},
  journal={IMA Journal of Numerical Analysis},
  year={2025},
  doi={10.1093/imanum/draf104}
}`
      },
      {
        id: 'sun2025ccp',
        type: 'published',
        year: 2025,
        status: 'Published',
        statusBadge: 'success',
        authorsHTML: '<strong>Zhengjie Sun</strong>, Leevan Ling and Ran Zhang*',
        titleHTML: 'Learning PDEs from data on closed surfaces with sparse optimization',
        venue: 'Communications in Computational Physics, 37:289–314',
        doiLink: 'https://doi.org/10.4208/cicp.OA-2024-0112',
        arxivId: '2405.06199',
        arxivAbs: 'https://arxiv.org/abs/2405.06199',
        apa: 'Sun, Z., Ling, L., & Zhang, R. (2025). Learning PDEs from data on closed surfaces with sparse optimization. Communications in Computational Physics, 37, 289–314.',
        bibtex:
`@article{sun2025learning,
  title={Learning PDEs from data on closed surfaces with sparse optimization},
  author={Sun, Zhengjie and Ling, Leevan and Zhang, Ran},
  journal={Communications in Computational Physics},
  volume={37},
  pages={289--314},
  year={2025}
}`
      },
     
      {
        id: 'sun2025jsc',
        type: 'published',
        year: 2025,
        status: 'Published',
        statusBadge: 'success',
        authorsHTML: '<strong>Zhengjie Sun*</strong>, Leevan Ling and Meng Chen',
        titleHTML: 'Structure-preserving kernel-based methods for solving dissipative PDEs on surfaces',
        venue: 'Journal of Scientific Computing, 102(3):70',
        doiLink:  'https://doi.org/10.1007/s10915-024-02774-0',
        arxivId: '2312.17478',
        arxivAbs: 'https://arxiv.org/abs/2312.17478',
        apa: 'Sun, Z., Ling, L., & Chen, M. (2025). Structure-preserving kernel-based methods for solving dissipative PDEs on surfaces. Journal of Scientific Computing, 102(3), 70.',
        bibtex:
`@article{sun2025structure,
  title={Structure-preserving kernel-based methods for solving dissipative PDEs on surfaces},
  author={Sun, Zhengjie and Ling, Leevan and Chen, Meng},
  journal={Journal of Scientific Computing},
  volume={102},
  number={3},
  pages={70},
  year={2025}
}`
      },
      {
        id: 'gao2024num-math',
        type: 'published',
        year: 2024,
        status: 'Published',
        statusBadge: 'success',
        authorsHTML: 'Wenwu Gao, Jiecheng Wang, <strong>Zhengjie Sun*</strong> and Gregory E. Fasshauer',
        titleHTML: 'Quasi-interpolation for high-dimensional function approximation',
        venue: 'Numerische Mathematik, 156:1855–1885',
        doiLink:  'https://doi.org/10.1007/s00211-024-01435-6',
        arxivId: '2409.14278',
        arxivAbs: 'https://arxiv.org/abs/2409.14278',
        pdf: 'https://arxiv.org/abs/2409.14278.pdf',
        apa: 'Gao, W., Wang, J., Sun, Z., & Fasshauer, G. E. (2024). Quasi-interpolation for high-dimensional function approximation. Numerische Mathematik, 156, 1855–1885.',
        bibtex:
`@article{gao2024highdim,
  title={Quasi-interpolation for high-dimensional function approximation},
  author={Gao, Wenwu and Wang, Jiecheng and Sun, Zhengjie and Fasshauer, Gregory E.},
  journal={Numerische Mathematik},
  volume={156},
  pages={1855--1885},
  year={2024}
}`
      },
      {
        id: 'sun2024sjsc',
        type: 'published',
        year: 2024,
        status: 'Published',
        statusBadge: 'success',
        authorsHTML: '<strong>Zhengjie Sun*</strong> and Leevan Ling',
        titleHTML: 'A high-order meshless linearly implicit energy-preserving method for nonlinear wave equations on Riemannian manifolds',
        venue: 'SIAM Journal on Scientific Computing, 46(6):A3779–3802',
        apa: 'Sun, Z., & Ling, L. (2024). A high-order meshless linearly implicit energy-preserving method for nonlinear wave equations on Riemannian manifolds. SIAM Journal on Scientific Computing, 46(6), A3779–A3802.',
        bibtex:
`@article{sun2024highorder,
  title={A high-order meshless linearly implicit energy-preserving method for nonlinear wave equations on Riemannian manifolds},
  author={Sun, Zhengjie and Ling, Leevan},
  journal={SIAM Journal on Scientific Computing},
  volume={46},
  number={6},
  pages={A3779--A3802},
  year={2024}
}`
      },
      {
        id: 'sun2024cnsns',
        type: 'published',
        year: 2024,
        status: 'Published',
        statusBadge: 'success',
        authorsHTML: '<strong>Zhengjie Sun</strong> and Qinjiao Gao*',
        titleHTML: 'Energy-preserving schemes for conservative PDEs based on periodic quasi-interpolation methods',
        venue: 'Communications in Nonlinear Science and Numerical Simulation, 131, 107831',
        apa: 'Sun, Z., & Gao, Q. (2024). Energy-preserving schemes for conservative PDEs based on periodic quasi-interpolation methods. Communications in Nonlinear Science and Numerical Simulation, 131, 107831.',
        bibtex:
`@article{sun2024energy,
  title={Energy-preserving schemes for conservative PDEs based on periodic quasi-interpolation methods},
  author={Sun, Zhengjie and Gao, Qinjiao},
  journal={Communications in Nonlinear Science and Numerical Simulation},
  volume={131},
  pages={107831},
  year={2024}
}`
      },
      {
        id: 'sun2023numalg',
        type: 'published',
        year: 2023,
        status: 'Published',
        statusBadge: 'success',
        authorsHTML: '<strong>Zhengjie Sun*</strong> and Yuyan Gao',
        titleHTML: 'High order multiquadric trigonometric quasi-interpolation method for solving time-dependent partial differential equations',
        venue: 'Numerical Algorithms, 93:1719–1739',
        apa: 'Sun, Z., & Gao, Y. (2023). High order multiquadric trigonometric quasi-interpolation method for solving time-dependent partial differential equations. Numerical Algorithms, 93, 1719–1739.',
        bibtex:
`@article{sun2023mq,
  title={High order multiquadric trigonometric quasi-interpolation method for solving time-dependent partial differential equations},
  author={Sun, Zhengjie and Gao, Yuyan},
  journal={Numerical Algorithms},
  volume={93},
  pages={1719--1739},
  year={2023}
}`
      },
      {
        id: 'sun2023aml',
        type: 'published',
        year: 2023,
        status: 'Published',
        statusBadge: 'success',
        authorsHTML: '<strong>Zhengjie Sun</strong> and Shengliang Zhang*',
        titleHTML: 'A radial basis function approximation method for conservative Allen-Cahn equations on surfaces',
        venue: 'Applied Mathematics Letters, 143, 108634',
        apa: 'Sun, Z., & Zhang, S. (2023). A radial basis function approximation method for conservative Allen-Cahn equations on surfaces. Applied Mathematics Letters, 143, 108634.',
        bibtex:
`@article{sun2023ac,
  title={A radial basis function approximation method for conservative Allen-Cahn equations on surfaces},
  author={Sun, Zhengjie and Zhang, Shengliang},
  journal={Applied Mathematics Letters},
  volume={143},
  pages={108634},
  year={2023}
}`
      },
      {
        id: 'zhang2023cma',
        type: 'published',
        year: 2023,
        status: 'Published',
        statusBadge: 'success',
        authorsHTML: 'Shengliang Zhang, <strong>Zhengjie Sun*</strong> and Alpesh Kumar',
        titleHTML: 'Meshless symplectic and multi-symplectic scheme for the coupled nonlinear Schrödinger system based on local RBF approximation',
        venue: 'Computers & Mathematics with Applications, 134:16–32',
        apa: 'Zhang, S., Sun, Z., & Kumar, A. (2023). Meshless symplectic and multi-symplectic scheme for the coupled nonlinear Schrödinger system based on local RBF approximation. Computers & Mathematics with Applications, 134, 16–32.',
        bibtex:
`@article{zhang2023symplectic,
  title={Meshless symplectic and multi-symplectic scheme for the coupled nonlinear Schr{\"o}dinger system based on local RBF approximation},
  author={Zhang, Shengliang and Sun, Zhengjie and Kumar, Alpesh},
  journal={Computers \& Mathematics with Applications},
  volume={134},
  pages={16--32},
  year={2023}
}`
      },
      {
        id: 'sun2023ijcm',
        type: 'published',
        year: 2023,
        status: 'Published',
        statusBadge: 'success',
        authorsHTML: '<strong>Zhengjie Sun*</strong> and Yuyan Gao',
        titleHTML: 'A meshless quasi-interpolation method for solving hyperbolic conservation laws based on the essentially non-oscillatory reconstruction',
        venue: 'International Journal of Computer Mathematics, 100(6):1303–1320',
        apa: 'Sun, Z., & Gao, Y. (2023). A meshless quasi-interpolation method for solving hyperbolic conservation laws based on the essentially non-oscillatory reconstruction. International Journal of Computer Mathematics, 100(6), 1303–1320.',
        bibtex:
`@article{sun2023eno,
  title={A meshless quasi-interpolation method for solving hyperbolic conservation laws based on the essentially non-oscillatory reconstruction},
  author={Sun, Zhengjie and Gao, Yuyan},
  journal={International Journal of Computer Mathematics},
  volume={100},
  number={6},
  pages={1303--1320},
  year={2023}
}`
      },
      {
        id: 'sun2022sjsc',
        type: 'published',
        year: 2022,
        status: 'Published',
        statusBadge: 'success',
        authorsHTML: '<strong>Zhengjie Sun</strong> and Leevan Ling*',
        titleHTML: 'A kernel-based meshless conservative Galerkin method for solving Hamiltonian wave equations',
        venue: 'SIAM Journal on Scientific Computing, 44(4):A2789–2807',
        apa: 'Sun, Z., & Ling, L. (2022). A kernel-based meshless conservative Galerkin method for solving Hamiltonian wave equations. SIAM Journal on Scientific Computing, 44(4), A2789–A2807.',
        bibtex:
`@article{sun2022galerkin,
  title={A kernel-based meshless conservative Galerkin method for solving Hamiltonian wave equations},
  author={Sun, Zhengjie and Ling, Leevan},
  journal={SIAM Journal on Scientific Computing},
  volume={44},
  number={4},
  pages={A2789--A2807},
  year={2022}
}`
      },
      {
        id: 'sun2022jsc',
        type: 'published',
        year: 2022,
        status: 'Published',
        statusBadge: 'success',
        authorsHTML: '<strong>Zhengjie Sun</strong>, Wenwu Gao and Ran Yang*',
        titleHTML: 'A convergent iterated quasi-interpolation for periodic domain and its applications to surface PDEs',
        venue: 'Journal of Scientific Computing, 93(2):37',
        apa: 'Sun, Z., Gao, W., & Yang, R. (2022). A convergent iterated quasi-interpolation for periodic domain and its applications to surface PDEs. Journal of Scientific Computing, 93(2), 37.',
        bibtex:
`@article{sun2022iterated,
  title={A convergent iterated quasi-interpolation for periodic domain and its applications to surface PDEs},
  author={Sun, Zhengjie and Gao, Wenwu and Yang, Ran},
  journal={Journal of Scientific Computing},
  volume={93},
  number={2},
  pages={37},
  year={2022}
}`
      },
      {
        id: 'sun2022amc',
        type: 'published',
        year: 2022,
        status: 'Published',
        statusBadge: 'success',
        authorsHTML: '<strong>Zhengjie Sun*</strong>',
        titleHTML: 'A conservative scheme for two-dimensional Schrödinger equation based on multi-quadric trigonometric quasi-interpolation approach',
        venue: 'Applied Mathematics and Computation, 423, 12pp',
        apa: 'Sun, Z. (2022). A conservative scheme for two-dimensional Schrödinger equation based on multi-quadric trigonometric quasi-interpolation approach. Applied Mathematics and Computation, 423, 12pp.',
        bibtex:
`@article{sun2022schrodinger,
  title={A conservative scheme for two-dimensional Schr{\"o}dinger equation based on multi-quadric trigonometric quasi-interpolation approach},
  author={Sun, Zhengjie},
  journal={Applied Mathematics and Computation},
  volume={423},
  pages={12pp},
  year={2022}
}`
      },
      {
        id: 'gao2022cam',
        type: 'published',
        year: 2022,
        status: 'Published',
        statusBadge: 'success',
        authorsHTML: 'Yuyan Gao and <strong>Zhengjie Sun*</strong>',
        titleHTML: 'Multi-symplectic quasi-interpolation method for the KdV equation',
        venue: 'Computational and Applied Mathematics, 41(3):112, 17pp',
        apa: 'Gao, Y., & Sun, Z. (2022). Multi-symplectic quasi-interpolation method for the KdV equation. Computational and Applied Mathematics, 41(3), 112 (17pp).',
        bibtex:
`@article{gao2022kdv,
  title={Multi-symplectic quasi-interpolation method for the KdV equation},
  author={Gao, Yuyan and Sun, Zhengjie},
  journal={Computational and Applied Mathematics},
  volume={41},
  number={3},
  pages={112},
  year={2022}
}`
      },
      {
        id: 'sun2020numalg',
        type: 'published',
        year: 2020,
        status: 'Published',
        statusBadge: 'success',
        authorsHTML: '<strong>Zhengjie Sun</strong>, Zongmin Wu and Wenwu Gao*',
        titleHTML: 'An iterated quasi-interpolation approach for derivative approximation',
        venue: 'Numerical Algorithms, 85:255–276',
        apa: 'Sun, Z., Wu, Z., & Gao, W. (2020). An iterated quasi-interpolation approach for derivative approximation. Numerical Algorithms, 85, 255–276.',
        bibtex:
`@article{sun2020deriv,
  title={An iterated quasi-interpolation approach for derivative approximation},
  author={Sun, Zhengjie and Wu, Zongmin and Gao, Wenwu},
  journal={Numerical Algorithms},
  volume={85},
  pages={255--276},
  year={2020}
}`
      },
      {
        id: 'sun2019jcp',
        type: 'published',
        year: 2019,
        status: 'Published',
        statusBadge: 'success',
        authorsHTML: '<strong>Zhengjie Sun*</strong>',
        titleHTML: 'Multi-symplectic quasi-interpolation method for Hamiltonian partial differential equations',
        venue: 'Journal of Computational Physics, 395:125–143',
        apa: 'Sun, Z. (2019). Multi-symplectic quasi-interpolation method for Hamiltonian partial differential equations. Journal of Computational Physics, 395, 125–143.',
        bibtex:
`@article{sun2019msqi,
  title={Multi-symplectic quasi-interpolation method for Hamiltonian partial differential equations},
  author={Sun, Zhengjie},
  journal={Journal of Computational Physics},
  volume={395},
  pages={125--143},
  year={2019}
}`
      },
      {
        id: 'gao2019anm',
        type: 'published',
        year: 2019,
        status: 'Published',
        statusBadge: 'success',
        authorsHTML: 'Wenwu Gao and <strong>Zhengjie Sun*</strong>',
        titleHTML: 'High-order numerical solution of time-dependent differential equations with quasi-interpolation',
        venue: 'Applied Numerical Mathematics, 146:276–290',
        apa: 'Gao, W., & Sun, Z. (2019). High-order numerical solution of time-dependent differential equations with quasi-interpolation. Applied Numerical Mathematics, 146, 276–290.',
        bibtex:
`@article{gao2019highorder,
  title={High-order numerical solution of time-dependent differential equations with quasi-interpolation},
  author={Gao, Wenwu and Sun, Zhengjie},
  journal={Applied Numerical Mathematics},
  volume={146},
  pages={276--290},
  year={2019}
}`
      },
      {
        id: 'sun2019eabe',
        type: 'published',
        year: 2019,
        status: 'Published',
        statusBadge: 'success',
        authorsHTML: '<strong>Zhengjie Sun*</strong>',
        titleHTML: 'A meshless symplectic method for two-dimensional nonlinear Schrödinger equations based on radial basis function approximation',
        venue: 'Engineering Analysis with Boundary Elements, 104:1–7',
        apa: 'Sun, Z. (2019). A meshless symplectic method for two-dimensional nonlinear Schrödinger equations based on radial basis function approximation. Engineering Analysis with Boundary Elements, 104, 1–7.',
        bibtex:
`@article{sun2019symplectic,
  title={A meshless symplectic method for two-dimensional nonlinear Schr{\"o}dinger equations based on radial basis function approximation},
  author={Sun, Zhengjie},
  journal={Engineering Analysis with Boundary Elements},
  volume={104},
  pages={1--7},
  year={2019}
}`
      },
      {
        id: 'sun2018jsc',
        type: 'published',
        year: 2018,
        status: 'Published',
        statusBadge: 'success',
        authorsHTML: '<strong>Zhengjie Sun</strong> and Zongmin Wu*',
        titleHTML: 'Meshless conservative schemes for multivariate Hamiltonian partial differential equations',
        venue: 'Journal of Scientific Computing, 76:1168–1187',
        apa: 'Sun, Z., & Wu, Z. (2018). Meshless conservative schemes for multivariate Hamiltonian partial differential equations. Journal of Scientific Computing, 76, 1168–1187.',
        bibtex:
`@article{sun2018meshless,
  title={Meshless conservative schemes for multivariate Hamiltonian partial differential equations},
  author={Sun, Zhengjie and Wu, Zongmin},
  journal={Journal of Scientific Computing},
  volume={76},
  pages={1168--1187},
  year={2018}
}`
      },
      {
        id: 'sun2018amm',
        type: 'published',
        year: 2018,
        status: 'Published',
        statusBadge: 'success',
        authorsHTML: '<strong>Zhengjie Sun</strong> and Wenwu Gao*',
        titleHTML: 'A energy-momentum conserving scheme for Hamiltonian wave equation based on multiquadric trigonometric quasi-interpolation',
        venue: 'Applied Mathematical Modelling, 57:179–191',
        apa: 'Sun, Z., & Gao, W. (2018). A energy-momentum conserving scheme for Hamiltonian wave equation based on multiquadric trigonometric quasi-interpolation. Applied Mathematical Modelling, 57, 179–191.',
        bibtex:
`@article{sun2018amm,
  title={A energy-momentum conserving scheme for Hamiltonian wave equation based on multiquadric trigonometric quasi-interpolation},
  author={Sun, Zhengjie and Gao, Wenwu},
  journal={Applied Mathematical Modelling},
  volume={57},
  pages={179--191},
  year={2018}
}`
      },
      {
        id: 'sun2018eabe',
        type: 'published',
        year: 2018,
        status: 'Published',
        statusBadge: 'success',
        authorsHTML: '<strong>Zhengjie Sun*</strong>',
        titleHTML: 'Conservative or dissipative quasi-interpolation method for evolutionary partial differential equations',
        venue: 'Engineering Analysis with Boundary Elements, 96:78–83',
        apa: 'Sun, Z. (2018). Conservative or dissipative quasi-interpolation method for evolutionary partial differential equations. Engineering Analysis with Boundary Elements, 96, 78–83.',
        bibtex:
`@article{sun2018qim,
  title={Conservative or dissipative quasi-interpolation method for evolutionary partial differential equations},
  author={Sun, Zhengjie},
  journal={Engineering Analysis with Boundary Elements},
  volume={96},
  pages={78--83},
  year={2018}
}`
      },
      {
        id: 'sun2017anm',
        type: 'published',
        year: 2017,
        status: 'Published',
        statusBadge: 'success',
        authorsHTML: '<strong>Zhengjie Sun</strong> and Wenwu Gao*',
        titleHTML: 'A meshless scheme for Hamiltonian partial differential equations with conservation properties',
        venue: 'Applied Numerical Mathematics, 119:115–125',
        apa: 'Sun, Z., & Gao, W. (2017). A meshless scheme for Hamiltonian partial differential equations with conservation properties. Applied Numerical Mathematics, 119, 115–125.',
        bibtex:
`@article{sun2017anm,
  title={A meshless scheme for Hamiltonian partial differential equations with conservation properties},
  author={Sun, Zhengjie and Gao, Wenwu},
  journal={Applied Numerical Mathematics},
  volume={119},
  pages={115--125},
  year={2017}
}`
      }
    ];

    const preprintsList = document.getElementById('preprintsList');
    const publishedList = document.getElementById('publishedList');

    function createLinkBtn({className, href, iconHTML, label}){
      const a = document.createElement('a');
      a.className = `btn ${className}`;
      a.href = href; a.target = '_blank'; a.rel = 'noopener';
      a.innerHTML = `${iconHTML} ${label}`;
      return a;
    }

    // Preprints：原通用渲染（右侧含年份、venue与状态）
    function renderListDefault(targetEl, items){
      targetEl.innerHTML = '';
      for(const p of items){
        const li = document.createElement('li'); li.className='pub-item';

        const left = document.createElement('div');
        const meta = document.createElement('div'); meta.className='meta';
        if(p.status){ const badge=document.createElement('span'); badge.className='badge '+(p.statusBadge||''); badge.textContent=p.status; meta.appendChild(badge); }
        const title = document.createElement('div'); title.className='title'; title.innerHTML=`<em>${p.titleHTML}</em>`;
        const authors = document.createElement('div'); authors.className='authors'; authors.innerHTML=p.authorsHTML;

        const links = document.createElement('div'); links.className='links';
        if(p.arxivAbs){ links.appendChild(createLinkBtn({className:'arxiv', href:p.arxivAbs, iconHTML:'<i class="ai ai-arxiv"></i>', label:`arXiv${p.arxivId?':'+p.arxivId:''}`})); }
        if(p.pdf){ links.appendChild(createLinkBtn({className:'pdf', href:p.pdf, iconHTML:'<i class="fas fa-file-pdf"></i>', label:'PDF'})); }
        if(p.doiLink){ links.appendChild(createLinkBtn({className:'doi', href:p.doiLink, iconHTML:'<i class="fas fa-link"></i>', label:'DOI'})); }
        const cite=document.createElement('button'); cite.className='btn cite cite-btn'; cite.type='button'; cite.dataset.id=p.id; cite.innerHTML=`<i class="fas fa-quote-right"></i> Cite`; links.appendChild(cite);

        left.appendChild(meta); left.appendChild(title); left.appendChild(authors); left.appendChild(links);

        const right=document.createElement('div'); right.className='right';
        right.innerHTML = `
          <div class="year">${p.year}</div>
          ${p.venue ? `<div class="venue">${p.venue}</div>` : ''}
          ${p.status ? `<div class="status">${p.status}</div>` : ''}
        `;

        li.appendChild(left); li.appendChild(right); targetEl.appendChild(li);
      }
    }

    // Published：右侧仅年份；venue 放在左侧标题下
    function renderListPublished(targetEl, items){
      targetEl.innerHTML = '';
      // 不排序，按添加顺序渲染
      for(const p of items){
        const li = document.createElement('li'); li.className='pub-item';

        const left = document.createElement('div');

        const title = document.createElement('div'); title.className='title'; title.innerHTML=`<em>${p.titleHTML}</em>`;
        left.appendChild(title);

        if(p.venue){
          const venue = document.createElement('div'); venue.className='venue'; venue.textContent = p.venue;
          left.appendChild(venue);
        }

        const authors = document.createElement('div'); authors.className='authors'; authors.innerHTML=p.authorsHTML;
        left.appendChild(authors);

        const links = document.createElement('div'); links.className='links';
        if(p.arxivAbs){ links.appendChild(createLinkBtn({className:'arxiv', href:p.arxivAbs, iconHTML:'<i class="ai ai-arxiv"></i>', label:`arXiv${p.arxivId?':'+p.arxivId:''}`})); }
        if(p.pdf){ links.appendChild(createLinkBtn({className:'pdf', href:p.pdf, iconHTML:'<i class="fas fa-file-pdf"></i>', label:'PDF'})); }
        if(p.doiLink){ links.appendChild(createLinkBtn({className:'doi', href:p.doiLink, iconHTML:'<i class="fas fa-link"></i>', label:'DOI'})); }
        const cite=document.createElement('button'); cite.className='btn cite cite-btn'; cite.type='button'; cite.dataset.id=p.id; cite.innerHTML=`<i class="fas fa-quote-right"></i> Cite`; links.appendChild(cite);
        left.appendChild(links);

        const right=document.createElement('div'); right.className='right';
        right.innerHTML = `<div class="year">${p.year}</div>`; // 仅年份

        li.appendChild(left); li.appendChild(right); targetEl.appendChild(li);
      }
    }

    // 初始渲染
    renderListDefault(preprintsList, pubs.filter(p=>p.type==='preprint'));
    renderListPublished(publishedList, pubs.filter(p=>p.type==='published'));

    // Modal 逻辑
    const modal=document.getElementById('citeModal');
    const closeBtn=document.getElementById('closeModal');
    const citeContent=document.getElementById('citeContent');
    const copyBtn=document.getElementById('copyBtn');
    const tabAPA=document.getElementById('tab-apa');
    const tabBib=document.getElementById('tab-bib');
    let currentPub=null;

    function openModal(pubId){
      currentPub=pubs.find(p=>p.id===pubId);
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
      copyBtn.innerHTML= ok ? '<i class="fas fa-check"></i> Copied' : '<i class="fas fa-copy"></i> Copy';
      setTimeout(()=>{ copyBtn.classList.remove('success'); copyBtn.innerHTML='<i class="fas fa-copy"></i> Copy'; }, 1800);
    });
  </script>
</body>
</html>
