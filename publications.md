---
layout: page
permalink: /publications/index.html

title: Publications
---

Latest Update: Oct 2025


<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Academic Publications</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/jpswalsh/academicons@1.9.4/css/academicons.min.css">
    <style>
        /* 基础样式重置 */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', 'Helvetica Neue', Arial, sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #f9f9f9;
            max-width: 1000px;
            margin: 0 auto;
            padding: 40px;
        }
        
        /* 标题样式 */
        .section-title {
            font-family: 'Georgia', 'Times New Roman', serif;
            font-weight: 600;
            color: #2c3e50;
            border-bottom: 2px solid #3498db;
            padding-bottom: 8px;
            margin: 40px 0 20px 0;
            font-size: 1.5rem;
        }
        
        /* 预印本列表容器 */
        .preprints-container {
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
            padding: 25px;
            margin-bottom: 40px;
        }
        
        /* 紧凑列表样式 */
        .compact-list {
            list-style-type: none;
        }
        
        .compact-list li {
            margin-bottom: 25px;
            padding-bottom: 20px;
            border-bottom: 1px solid #eaeaea;
            position: relative;
        }
        
        .compact-list li:last-child {
            border-bottom: none;
            margin-bottom: 0;
            padding-bottom: 0;
        }
        
        /* 论文标题样式 */
        .compact-list em {
            font-style: italic;
            color: #2c3e50;
            display: inline-block;
            margin: 5px 0;
        }
        
        /* 作者姓名样式 */
        .compact-list strong {
            color: #e74c3c;
            font-weight: 700;
        }
        
        /* 论文状态 */
        .compact-list li::after {
            content: attr(data-status);
            position: absolute;
            top: 0;
            right: 0;
            background-color: #f1c40f;
            color: #34495e;
            padding: 3px 10px;
            border-radius: 12px;
            font-size: 0.8rem;
            font-weight: 600;
        }
        
        /* 链接容器 */
        .paper-links {
            margin-top: 12px;
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
        }
        
        /* 链接通用样式 */
        .paper-links a {
            display: inline-flex;
            align-items: center;
            padding: 6px 12px;
            border-radius: 4px;
            text-decoration: none;
            font-size: 0.9rem;
            transition: all 0.3s ease;
            font-weight: 500;
        }
        
        /* arXiv链接样式 */
        .arxiv-id {
            background-color: #1a73e8;
            color: white !important;
            border: 1px solid #1a73e8;
        }
        
        .arxiv-id:hover {
            background-color: #0d62d9;
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(26, 115, 232, 0.3);
        }
        
        /* PDF链接样式 */
        .pdf-download {
            background-color: #f8f9fa;
            color: #d32f2f !important;
            border: 1px solid #ddd;
        }
        
        .pdf-download:hover {
            background-color: #e9ecef;
            border-color: #d32f2f;
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(211, 47, 47, 0.2);
        }
        
        /* 引用链接样式 */
        .cite-btn {
            background-color: #2ecc71;
            color: white !important;
            border: 1px solid #2ecc71;
            cursor: pointer;
        }
        
        .cite-btn:hover {
            background-color: #27ae60;
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(46, 204, 113, 0.3);
        }
        
        /* 图标间距 */
        .paper-links i, .paper-links .ai {
            margin-right: 6px;
            font-size: 1rem;
        }
        
        /* 引用弹窗 */
        .citation-modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.5);
            z-index: 1000;
            justify-content: center;
            align-items: center;
        }
        
        .citation-content {
            background-color: white;
            padding: 25px;
            border-radius: 8px;
            max-width: 600px;
            width: 90%;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.2);
            position: relative;
        }
        
        .citation-close {
            position: absolute;
            top: 15px;
            right: 15px;
            background: none;
            border: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: #7f8c8d;
        }
        
        .citation-text {
            background-color: #f8f9fa;
            padding: 15px;
            border-radius: 4px;
            margin: 15px 0;
            font-family: 'Courier New', monospace;
            font-size: 0.9rem;
            line-height: 1.5;
            white-space: pre-wrap;
            border-left: 4px solid #3498db;
        }
        
        .copy-btn {
            background-color: #3498db;
            color: white;
            border: none;
            padding: 8px 16px;
            border-radius: 4px;
            cursor: pointer;
            font-size: 0.9rem;
            margin-top: 10px;
        }
        
        .copy-btn:hover {
            background-color: #2980b9;
        }
        
        /* 响应式设计 */
        @media (max-width: 768px) {
            body {
                padding: 15px;
            }
            
            .preprints-container {
                padding: 15px;
            }
            
            .compact-list li {
                padding: 15px;
                background-color: #fcfcfc;
                border-radius: 6px;
                margin-bottom: 15px;
            }
            
            .compact-list li::after {
                position: relative;
                display: inline-block;
                margin-left: 10px;
                top: -2px;
            }
            
            .paper-links {
                flex-direction: column;
                gap: 6px;
            }
            
            .paper-links a {
                width: 100%;
                justify-content: center;
                padding: 8px 12px;
            }
        }
        
        /* 打印样式 */
        @media print {
            .paper-links a {
                color: #000 !important;
                text-decoration: underline;
                background: none !important;
                border: none !important;
                padding: 0 !important;
            }
            
            .cite-btn {
                display: none;
            }
            
            .preprints-container {
                box-shadow: none;
                padding: 0;
            }
        }
    </style>
</head>
<body>
    <div class="preprints-container">
        <h3 class="section-title">
            <i class="fas fa-file-alt"></i> Preprints
        </h3>
        
        <ul class="compact-list">
            <li data-status="Submitted, 2025">
                <strong>Zhengjie Sun*</strong>, Mengyuan Lv and Xingping Sun. 
                <em>Monte Carlo quasi-interpolation of spherical data</em>. 
                Submitted, 2025.
                <div class="paper-links">
                    <a href="https://arxiv.org/abs/2510.12027" class="arxiv-id" target="_blank" rel="noopener noreferrer">
                        <i class="ai ai-arxiv"></i> arXiv:2510.12027
                    </a>
                    <a href="https://arxiv.org/pdf/2510.12027.pdf" class="pdf-download" target="_blank" rel="noopener noreferrer">
                        <i class="fas fa-file-pdf"></i> PDF
                    </a>
                    <a href="#" class="cite-btn" data-id="sun2025monte">
                        <i class="fas fa-quote-right"></i> Cite
                    </a>
                </div>
            </li>
            
            <li data-status="Submitted, 2025">
                <strong>Zhengjie Sun*</strong> and Leevan Ling. 
                <em>Inverse inequalities for kernel-based approximation on bounded domains and Riemannian manifolds</em>. 
                Submitted, 2025.
                <div class="paper-links">
                    <a href="https://arxiv.org/abs/2508.05376" class="arxiv-id" target="_blank" rel="noopener noreferrer">
                        <i class="ai ai-arxiv"></i> arXiv:2508.05376
                    </a>
                    <a href="https://arxiv.org/pdf/2508.05376.pdf" class="pdf-download" target="_blank" rel="noopener noreferrer">
                        <i class="fas fa-file-pdf"></i> PDF
                    </a>
                    <a href="#" class="cite-btn" data-id="sun2025inverse">
                        <i class="fas fa-quote-right"></i> Cite
                    </a>
                </div>
            </li>
            
            <li data-status="Submitted, 2025">
                Wenwu Gao, Le Hu, <strong>Zhengjie Sun*</strong> and Changwei Wang. 
                <em>Quasi-interpolation using generalized Gaussian kernels</em>. 
                Submitted, 2025.
                <div class="paper-links">
                    <a href="https://arxiv.org/abs/2407.21283" class="arxiv-id" target="_blank" rel="noopener noreferrer">
                        <i class="ai ai-arxiv"></i> arXiv:2407.21283
                    </a>
                    <a href="https://arxiv.org/pdf/2407.21283.pdf" class="pdf-download" target="_blank" rel="noopener noreferrer">
                        <i class="fas fa-file-pdf"></i> PDF
                    </a>
                    <a href="#" class="cite-btn" data-id="gao2024quasi">
                        <i class="fas fa-quote-right"></i> Cite
                    </a>
                </div>
            </li>
        </ul>
    </div>
    
    <!-- 引用弹窗 -->
    <div class="citation-modal" id="citationModal">
        <div class="citation-content">
            <button class="citation-close" id="closeModal">&times;</button>
            <h3>Citation</h3>
            <div class="citation-text" id="citationText"></div>
            <button class="copy-btn" id="copyCitation">
                <i class="fas fa-copy"></i> Copy to Clipboard
            </button>
        </div>
    </div>

    <script>
        // 引用数据
        const citations = {
            'sun2025monte': `Sun, Z., Lv, M., & Sun, X. (2025). Monte Carlo quasi-interpolation of spherical data. arXiv preprint arXiv:2510.12027.

@article{sun2025monte,
  title={Monte Carlo quasi-interpolation of spherical data},
  author={Sun, Zhengjie and Lv, Mengyuan and Sun, Xingping},
  journal={arXiv preprint arXiv:2510.12027},
  year={2025}
}`,
            
            'sun2025inverse': `Sun, Z., & Ling, L. (2025). Inverse inequalities for kernel-based approximation on bounded domains and Riemannian manifolds. arXiv preprint arXiv:2508.05376.

@article{sun2025inverse,
  title={Inverse inequalities for kernel-based approximation on bounded domains and Riemannian manifolds},
  author={Sun, Zhengjie and Ling, Leevan},
  journal={arXiv preprint arXiv:2508.05376},
  year={2025}
}`,
            
            'gao2024quasi': `Gao, W., Hu, L., Sun, Z., & Wang, C. (2024). Quasi-interpolation using generalized Gaussian kernels. arXiv preprint arXiv:2407.21283.

@article{gao2024quasi,
  title={Quasi-interpolation using generalized Gaussian kernels},
  author={Gao, Wenwu and Hu, Le and Sun, Zhengjie and Wang, Changwei},
  journal={arXiv preprint arXiv:2407.21283},
  year={2024}
}`
        };

        // DOM元素
        const modal = document.getElementById('citationModal');
        const citationText = document.getElementById('citationText');
        const closeModal = document.getElementById('closeModal');
        const copyBtn = document.getElementById('copyCitation');

        // 为所有引用按钮添加事件监听器
        document.querySelectorAll('.cite-btn').forEach(btn => {
            btn.addEventListener('click', function(e) {
                e.preventDefault();
                const paperId = this.dataset.id;
                
                if (citations[paperId]) {
                    citationText.textContent = citations[paperId];
                    modal.style.display = 'flex';
                    
                    // 设置页面不可滚动
                    document.body.style.overflow = 'hidden';
                }
            });
        });

        // 关闭弹窗
        closeModal.addEventListener('click', function() {
            modal.style.display = 'none';
            document.body.style.overflow = 'auto';
        });

        // 点击弹窗外部关闭
        modal.addEventListener('click', function(e) {
            if (e.target === modal) {
                modal.style.display = 'none';
                document.body.style.overflow = 'auto';
            }
        });

        // 复制引用到剪贴板
        copyBtn.addEventListener('click', function() {
            const textToCopy = citationText.textContent;
            
            navigator.clipboard.writeText(textToCopy).then(() => {
                // 显示复制成功反馈
                const originalText = copyBtn.innerHTML;
                copyBtn.innerHTML = '<i class="fas fa-check"></i> Copied!';
                copyBtn.style.backgroundColor = '#2ecc71';
                
                setTimeout(() => {
                    copyBtn.innerHTML = originalText;
                    copyBtn.style.backgroundColor = '';
                }, 2000);
            }).catch(err => {
                console.error('复制失败: ', err);
                alert('复制失败，请手动选择文本复制。');
            });
        });

        // 链接点击统计（可选）
        document.querySelectorAll('.paper-links a[href]').forEach(link => {
            link.addEventListener('click', function() {
                const linkType = this.classList.contains('arxiv-id') ? 'arXiv' : 
                               this.classList.contains('pdf-download') ? 'PDF' : 'Cite';
                console.log(`点击了 ${linkType} 链接: ${this.href}`);
                
                // 这里可以添加Google Analytics或其他统计代码
                // ga('send', 'event', 'Preprint Link', 'click', linkType);
            });
        });
    </script>
</body>
</html>
    


<h3 style="margin-bottom: 15px; font-family: inherit;">Published papers</h3>

<ul class="compact-list">

<li>&nbsp;Zhongting Xu, <strong>Zhengjie Sun*</strong> and Shengliang Zhang. A meshless energy-preserving scheme for conservative partial differential equations using kernel-based Galerkin methods, <i>Engineering Analysis with Boundary Elements</i>, 183, 106615, 2026. </li>

<li>&nbsp;<strong>Zhengjie Sun</strong> and Yuyan Gao*. A meshless structure-preserving quasi-interpolation method for the Allen-Cahn equation on spheres,  <i>Mathematics and Computers in Simulation</i>, 241, 31-47, 2026. </li>
    
<li>&nbsp;<strong>Zhengjie Sun</strong>, Wenwu Gao* and Xingping Sun. Scaled zonal kernel quasi-interpolation on spheres, <i>IMA Journal of Numerical Analysis</i>, doi.org/10.1093/imanum/draf104, 2025. (<a href="https://arxiv.org/abs/2408.14803" style="color: #0066cc; text-decoration: none;">arXiv:2408.14803</a>)</li>
    
<li>&nbsp;<strong>Zhengjie Sun</strong>, Leevan Ling and Ran Zhang*. Learning PDEs from data on closed surfaces with sparse optimization, <i>Communications in Computational Physics</i>, 37:289-314, 2025. 
(<a href="https://arxiv.org/abs/2405.06199" style="color: #0066cc; text-decoration: none;">arXiv:2405.06199</a>)</li>
    
<li>&nbsp;Qinjiao Gao, <strong>Zhengjie Sun*</strong> and Zongmin Wu. Energy-equidistributed moving mesh strategies for simulating Hamiltonian partial differential equations, <i>Applied Mathematics Letters</i>, 163, 109460, 2025. </li>
    
<li>&nbsp;<strong>Zhengjie Sun*</strong>, Leevan Ling and Meng Chen. Structure-preserving kernel-based methods for solving dissipative PDEs on surfaces, <i>Journal of Scientific Computing</i>, 102(3):70, 2025.
(<a href="https://arxiv.org/abs/2312.17478" style="color: #0066cc; text-decoration: none;">arXiv:2312.17478</a>)</li>

<li>&nbsp;Wenwu Gao, Jiecheng Wang, <strong>Zhengjie Sun*</strong> and Gregory E. Fasshauer. Quasi-interpolation for high-dimensional function approximation, <i>Numerische Mathematik</i>, 156:1855–1885, 2024.
 (<a href="https://arxiv.org/abs/2409.14278" style="color: #0066cc; text-decoration: none;">arXiv:2409.14278</a>)</li>

<li>&nbsp;<strong>Zhengjie Sun*</strong> and Leevan Ling. A high-order meshless linearly implicit energy-preserving method for nonlinear wave equations on Riemannian manifolds, <i>SIAM Journal on Scientific Computing</i>, 46(6):A3779-3802, 2024. </li>

<li>&nbsp;<strong>Zhengjie Sun</strong> and Qinjiao Gao*. Energy-preserving schemes for conservative PDEs based on periodic quasi-interpolation methods, <i>Communications in Nonlinear Science and Numerical Simulation</i>, 131, 107831, 2024. </li>

<li>&nbsp;<strong>Zhengjie Sun*</strong> and Yuyan Gao. High order multiquadric trigonometric quasi-interpolation method for solving time-dependent partial differential equations, <i>Numerical Algorithms</i>, 93:1719-1739, 2023. </li>

<li>&nbsp;<strong>Zhengjie Sun</strong> and Shengliang Zhang*. A radial basis function approximation method for conservative Allen-Cahn equations on surfaces, <i>Applied Mathematics Letters</i>, 143, 108634, 2023. </li>

<li>&nbsp;Shengliang Zhang, <strong>Zhengjie Sun*</strong> and Alpesh Kumar. Meshless symplectic and multi-symplectic scheme for the coupled nonlinear Schrödinger system based on local RBF approximation, <i>Computers & Mathematics with Applications</i>, 134:16-32, 2023. </li>

<li>&nbsp;<strong>Zhengjie Sun*</strong> and Yuyan Gao. A meshless quasi-interpolation method for solving hyperbolic conservation laws based on the essentially non-oscillatory reconstruction, <i>International Journal of Computer Mathematics</i>, 100(6):1303-1320, 2023. </li>

<li>&nbsp;<strong>Zhengjie Sun</strong> and Leevan Ling*. A kernel-based meshless conservative Galerkin method for solving Hamiltonian wave equations, <i>SIAM Journal on Scientific Computing</i>, 44(4):A2789-2807, 2022. </li>

<li>&nbsp;<strong>Zhengjie Sun</strong>, Wenwu Gao and Ran Yang*. A convergent iterated quasi-interpolation for periodic domain and its applications to surface PDEs, <i>Journal of Scientific Computing</i>, 93(2):37, 2022. </li>

<li>&nbsp;<strong>Zhengjie Sun*</strong>. A conservative scheme for two-dimensional Schrödinger equation based on multi-quadric trigonometric quasi-interpolation approach, <i>Applied Mathematics and Computation</i>, 423, 2022, 12pp. </li>

<li>&nbsp;Yuyan Gao and <strong>Zhengjie Sun*</strong>. Multi-symplectic quasi-interpolation method for the KdV equation, <i>Computational and Applied Mathematics</i>, 41(3):112, 17pp, 2022. </li>

<li>&nbsp;<strong>Zhengjie Sun</strong>, Zongmin Wu and Wenwu Gao*. An iterated quasi-interpolation approach for derivative approximation, <i>Numerical Algorithms</i>, 85:255-276, 2020. </li>

<li>&nbsp;<strong>Zhengjie Sun*</strong>. Multi-symplectic quasi-interpolation method for Hamiltonian partial differential equations, <i>Journal of Computational Physics</i>, 395:125-143, 2019. </li>

<li>&nbsp;Wenwu Gao and <strong>Zhengjie Sun*</strong>. High-order numerical solution of time-dependent differential equations with quasi-interpolation, <i>Applied Numerical Mathematics</i>, 146:276-290, 2019. </li>

<li>&nbsp;<strong>Zhengjie Sun*</strong>. A meshless symplectic method for two-dimensional nonlinear Schrödinger equations based on radial basis function approximation, <i>Engineering Analysis with Boundary Elements</i>, 104:1-7, 2019. </li>

<li>&nbsp;<strong>Zhengjie Sun</strong> and Zongmin Wu*. Meshless conservative schemes for multivariate Hamiltonian partial differential equations, <i>Journal of Scientific Computing</i>, 76:1168-1187, 2018. </li>

<li>&nbsp;<strong>Zhengjie Sun</strong> and Wenwu Gao*. A energy-momentum conserving scheme for Hamiltonian wave equation based on multiquadric trigonometric quasi-interpolation, <i>Applied Mathematical Modelling</i>, 57:179-191, 2018. </li>

<li>&nbsp;<strong>Zhengjie Sun*</strong>. Conservative or dissipative quasi-interpolation method for evolutionary partial differential equations, <i>Engineering Analysis with Boundary Elements</i>, 96:78-83, 2018. </li>
     
<li>&nbsp;<strong>Zhengjie Sun</strong> and Wenwu Gao*. A meshless scheme for Hamiltonian partial differential equations with conservation properties, <i>Applied Numerical Mathematics</i>, 119:115-125, 2017. </li>


</ul>

---


