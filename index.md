---
layout: page
---

<!-- Base section spacing to align with Publications style -->
<style>
  /* 如果站点已有全局样式，可删除此段并改用站点 CSS */
  .section {
    margin: 1.5rem 0;
  }
  .section h3 {
    margin: 0 0 0.75rem;
    font-weight: 600;
    font-size: 1.25rem;
  }
  .pub-list {
    margin: 0;
    padding: 0;
    list-style: none;
  }
  .pub-item {
    display: grid;
    grid-template-columns: 1fr auto; /* 左：内容，右：年份 */
    gap: 0.75rem 1rem;
    padding: 0.5rem 0;
    border-top: 1px solid #e5e7eb;
  }
  .pub-item:first-child {
    border-top: none;
  }
  .pub-left {
    line-height: 1.7;
    min-width: 0; /* 防止长链接溢出 */
  }
  .pub-title {
    margin: 0.15rem 0 0;
    font-weight: 500;
  }
  .pub-venue {
    margin: 0.15rem 0 0;
    color: #374151; /* 微弱强调 */
  }
  .pub-year {
    white-space: nowrap;
    color: #6b7280;
    padding-left: 0.5rem;
  }
  .pub-link a {
    word-break: break-all; /* DOI/长链接在移动端换行 */
  }

  /* 小屏优化：年份换到下一行右对齐 */
  @media (max-width: 480px) {
    .pub-item {
      grid-template-columns: 1fr;
    }
    .pub-year {
      justify-self: end;
    }
  }
</style>

<!-- Profile / About Section -->
<section class="content section" aria-labelledby="about-title">
  <h3 id="about-title">
    About
  </h3>

  <p style="line-height: 1.7; margin: 0;">
    <strong>Sun, Zhengjie (孙正杰)</strong> is an Associate Professor at the School of Mathematics and Statistics,
    Nanjing University of Science and Technology. He received his Ph.D. from Fudan University in 2018.
    His research focuses on scattered data approximation, numerical analysis, and meshless methods for
    partial differential equations (PDEs).
  </p>

  <div style="height: 1rem;"></div>

  <p style="line-height: 1.7; margin: 0;">
    If you are interested in my work and would like to chat or collaborate, please email me at
    <a href="mailto:zhengjiesun@njust.edu.cn" rel="noopener noreferrer">
      <i>zhengjiesun@njust.edu.cn</i>
    </a>.
  </p>
</section>

<hr style="margin: 1.5rem 0; border: 0; border-top: 1px solid #e5e7eb;" />

<!-- Research Interests Section -->
<section class="content section" aria-labelledby="interests-title">
  <h3 id="interests-title">
    Research Interests
  </h3>

  <ul style="line-height: 1.7; margin: 0 0 0.5rem 1.25rem;">
    <li>Scattered data approximation</li>
    <li>Radial basis functions</li>
    <li>Meshless methods</li>
    <li>Structure-preserving schemes</li>
  </ul>

  <p style="line-height: 1.7; margin: 0.75rem 0 0;">
    We focus on the theory and applications of kernel-based meshless methods.
    In particular, we study interpolation and quasi-interpolation schemes of radial basis functions,
    and develop meshless structure-preserving algorithms for time-dependent PDEs.
    Recently, our interests include
    <strong>high-dimensional function approximation</strong> and
    <strong>numerical solutions for PDEs on manifolds</strong>.
  </p>
</section>

<hr style="margin: 1.5rem 0; border: 0; border-top: 1px solid #e5e7eb;" />

<!-- Selected Publications (代表作) - Unified with Publications style -->
<section class="content section" aria-labelledby="selected-pubs-title">
  <h3 id="selected-pubs-title">
    Selected Publications
  </h3>

  <ul class="pub-list">
    <!-- 1 -->
    <li class="pub-item">
      <div class="pub-left">
        <div class="pub-authors">
          <strong>Sun, Z.</strong>, Gao, W., &amp; Sun, X.
        </div>
        <div class="pub-title">
          Scaled zonal kernel quasi-interpolation on spheres.
        </div>
        <div class="pub-venue">
          <i>IMA Journal of Numerical Analysis</i>.
          <span class="pub-link">
            <a href="https://doi.org/10.1093/imanum/draf104" target="_blank" rel="noopener noreferrer">
              https://doi.org/10.1093/imanum/draf104
            </a>
          </span>
        </div>
      </div>
      <div class="pub-year">2025</div>
    </li>

    <!-- 2 -->
    <li class="pub-item">
      <div class="pub-left">
        <div class="pub-authors">
          <strong>Sun, Z.</strong>, &amp; Ling, L.
        </div>
        <div class="pub-title">
          A high-order meshless linearly implicit energy-preserving method for nonlinear wave equations on Riemannian manifolds.
        </div>
        <div class="pub-venue">
          <i>SIAM Journal on Scientific Computing</i>, 46(6), A3779–A3802.
        </div>
      </div>
      <div class="pub-year">2024</div>
    </li>

    <!-- 3 -->
    <li class="pub-item">
      <div class="pub-left">
        <div class="pub-authors">
          Gao, W., Wang, J., <strong>Sun, Z.</strong>, &amp; Fasshauer, G. E.
        </div>
        <div class="pub-title">
          Quasi-interpolation for high-dimensional function approximation.
        </div>
        <div class="pub-venue">
          <i>Numerische Mathematik</i>, 156, 1855–1885.
        </div>
      </div>
      <div class="pub-year">2024</div>
    </li>

    <!-- 4 -->
    <li class="pub-item">
      <div class="pub-left">
        <div class="pub-authors">
          <strong>Sun, Z.</strong>, &amp; Ling, L.
        </div>
        <div class="pub-title">
          A kernel-based meshless conservative Galerkin method for solving Hamiltonian wave equations.
        </div>
        <div class="pub-venue">
          <i>SIAM Journal on Scientific Computing</i>, 44(4), A2789–A2807.
        </div>
      </div>
      <div class="pub-year">2022</div>
    </li>

    <!-- 5 -->
    <li class="pub-item">
      <div class="pub-left">
        <div class="pub-authors">
          <strong>Sun, Z.</strong>, Ling, L., &amp; Chen, M.
        </div>
        <div class="pub-title">
          Structure-preserving kernel-based methods for solving dissipative PDEs on surfaces.
        </div>
        <div class="pub-venue">
          <i>Journal of Scientific Computing</i>, 102(3), 70.
        </div>
      </div>
      <div class="pub-year">2025</div>
    </li>
  </ul>
</section>
