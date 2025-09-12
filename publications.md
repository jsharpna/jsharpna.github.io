---
layout: page
title: Publications
permalink: /publications/
---

<style>
.search-box {
  width: 100%;
  padding: 12px 20px;
  margin: 20px 0;
  border: 2px solid #3498db;
  border-radius: 25px;
  font-size: 16px;
  outline: none;
}

.filter-buttons {
  text-align: center;
  margin: 20px 0;
  flex-wrap: wrap;
  display: flex;
  gap: 10px;
  justify-content: center;
}

.filter-btn {
  padding: 8px 16px;
  border: 2px solid #3498db;
  background: white;
  color: #3498db;
  border-radius: 20px;
  cursor: pointer;
  transition: all 0.3s ease;
}

.filter-btn:hover, .filter-btn.active {
  background: #3498db;
  color: white;
}

.publication-section {
  margin: 2rem 0;
  border: 1px solid #e1e8ed;
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 0 4px 6px rgba(0,0,0,0.1);
}

.section-header {
  padding: 1.5rem;
  margin: 0;
  color: white;
  display: flex;
  align-items: center;
  font-size: 1.4rem;
  font-weight: bold;
}

.section-header.education { background: linear-gradient(135deg, #e74c3c, #c0392b); }
.section-header.health { background: linear-gradient(135deg, #e67e22, #d35400); }
.section-header.astronomy { background: linear-gradient(135deg, #9b59b6, #8e44ad); }
.section-header.industry { background: linear-gradient(135deg, #3498db, #2980b9); }
.section-header.theory { background: linear-gradient(135deg, #27ae60, #229954); }

.publication-list {
  padding: 1.5rem;
  background: white;
}

.publication-item {
  margin: 1.5rem 0;
  padding: 1.5rem;
  background: #f8f9fa;
  border-left: 4px solid #3498db;
  border-radius: 0 8px 8px 0;
  transition: all 0.3s ease;
}

.publication-item:hover {
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
  transform: translateX(5px);
}

.pub-title {
  font-size: 1.1rem;
  font-weight: bold;
  margin: 0 0 0.5rem 0;
}

.pub-title a {
  color: #2c3e50;
  text-decoration: none;
}

.pub-title a:hover {
  color: #3498db;
  text-decoration: underline;
}

.pub-authors {
  color: #666;
  margin: 0.5rem 0;
  line-height: 1.4;
}

.pub-venue {
  color: #3498db;
  font-weight: 500;
  margin: 0.5rem 0;
}

.pub-year {
  display: inline-block;
  background: #3498db;
  color: white;
  padding: 2px 8px;
  border-radius: 12px;
  font-size: 0.85rem;
  font-weight: bold;
  margin-left: 10px;
}

.venue-badge {
  display: inline-block;
  padding: 2px 6px;
  border-radius: 8px;
  font-size: 0.75rem;
  font-weight: bold;
  margin-left: 5px;
}

.venue-top { background: #e74c3c; color: white; } /* NeurIPS, ICML, PNAS */
.venue-good { background: #f39c12; color: white; } /* AISTATS, KDD */
.venue-journal { background: #9b59b6; color: white; } /* JMLR, etc */

.stats-summary {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 1rem;
  margin: 2rem 0;
  text-align: center;
}

.stat-card {
  padding: 1rem;
  background: white;
  border: 1px solid #e1e8ed;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0,0,0,0.05);
}

.stat-number {
  font-size: 2rem;
  font-weight: bold;
  color: #3498db;
}

.stat-label {
  color: #666;
  font-size: 0.9rem;
}
</style>

<div style="text-align: center; margin: 2rem 0;">
  <h1 style="color: #2c3e50; margin-bottom: 0.5rem;">Research Publications</h1>
  <p style="font-size: 1.1rem; color: #666;">43+ publications spanning machine learning, statistics, and interdisciplinary applications</p>
</div>

<div class="stats-summary">
  <div class="stat-card">
    <div class="stat-number">43+</div>
    <div class="stat-label">Publications</div>
  </div>
  <div class="stat-card">
    <div class="stat-number">18+</div>
    <div class="stat-label">Journal Papers</div>
  </div>
  <div class="stat-card">
    <div class="stat-number">15+</div>
    <div class="stat-label">NeurIPS/ICML</div>
  </div>
</div>

<input type="text" class="search-box" id="searchBox" placeholder="🔍 Search publications by title, author, or venue...">

<div class="filter-buttons">
  <button class="filter-btn active" onclick="filterPublications('all')">All Publications</button>
  <button class="filter-btn" onclick="filterPublications('education')">🎓 Educational AI</button>
  <button class="filter-btn" onclick="filterPublications('health')">🦠 Public Health</button>
  <button class="filter-btn" onclick="filterPublications('astronomy')">🌌 Astronomy</button>
  <button class="filter-btn" onclick="filterPublications('industry')">🏢 Industry ML</button>
  <button class="filter-btn" onclick="filterPublications('theory')">📊 Statistical Theory</button>
</div>
<!-- Educational AI & Assessment -->
<div class="publication-section" data-category="education">
  <h2 class="section-header education">🎓 Educational AI & Assessment</h2>
  <div class="publication-list">
    
    <div class="publication-item">
      <div class="pub-title"><a href="https://scholar.google.com/citations?view_op=view_citation&hl=en&user=cXhAfX0AAAAJ&citation_for_view=cXhAfX0AAAAJ:Se3iqnhoufwC" target="_blank">BanditCAT and AutoIRT: Machine Learning Approaches to Computerized Adaptive Testing and Item Calibration</a></div>
      <div class="pub-authors"><strong>James Sharpnack</strong>, Kevin Hao, Phoebe Mulcaire, Klinton Bicknell, Geoff LaFlair, Kevin Yancey, Alina A von Davier</div>
      <div class="pub-venue">Large Foundation Models for Educational Assessment (PMLR) <span class="venue-badge venue-good">Workshop</span><span class="pub-year">2025</span></div>
    </div>

    <div class="publication-item">
      <div class="pub-title">Detecting LLM-assisted cheating on open-ended writing tasks on language proficiency tests</div>
      <div class="pub-authors">Chenhao Niu, Kevin Yancey, Ruidong Liu, Mirza Baig, André Horie, <strong>James Sharpnack</strong></div>
      <div class="pub-venue">EMNLP Industry Track <span class="venue-badge venue-good">Industry</span><span class="pub-year">2024</span></div>
    </div>

    <div class="publication-item">
      <div class="pub-title">AI for Education at AAAI 2024: Bridging Innovation and Responsibility</div>
      <div class="pub-authors">Muktha Ananda, Debshila Basu Malick, Jill Burstein, Lydia T Liu, Zitao Liu, <strong>James Sharpnack</strong>, Zichao Wang, Serena Wang</div>
      <div class="pub-venue">AAAI AI for Education Workshop (PMLR) <span class="venue-badge venue-good">Workshop</span><span class="pub-year">2024</span></div>
    </div>

    <div class="publication-item">
      <div class="pub-title">Preface: Innovation and Responsibility in AI-Supported Education</div>
      <div class="pub-authors">Debshila Basu Mallick, Jill Burstein, Simon Woodhead, <strong>James Sharpnack</strong>, Zichao Wang</div>
      <div class="pub-venue">Innovation and Responsibility in AI-Supported Education (PMLR) <span class="venue-badge venue-journal">Editorial</span><span class="pub-year">2025</span></div>
    </div>

  </div>
</div>

<!-- Industry-Scale Machine Learning -->
<div class="publication-section" data-category="industry">
  <h2 class="section-header industry">🏢 Industry-Scale Machine Learning</h2>
  <div class="publication-list">

    <div class="publication-item">
      <div class="pub-title"><a href="https://scholar.google.com/citations?view_op=view_citation&hl=en&user=cXhAfX0AAAAJ&citation_for_view=cXhAfX0AAAAJ:LkGwnXOMwfcC" target="_blank" style="color: #2c3e50; text-decoration: none;">Syndicated Bandits: A Framework for Auto Tuning Hyper-parameters in Contextual Bandit Algorithms</a></div>
      <div class="pub-authors">Qin Ding, Yi-Wei Liu, Cho-Jui Hsieh, <strong>James Sharpnack</strong></div>
      <div class="pub-venue">Advances in Neural Information Processing Systems (NeurIPS) <span class="venue-badge venue-top">NeurIPS</span><span class="pub-year">2022</span></div>
    </div>

    <div class="publication-item">
      <div class="pub-title"><a href="https://scholar.google.com/citations?view_op=view_citation&hl=en&user=cXhAfX0AAAAJ&citation_for_view=cXhAfX0AAAAJ:oNZyr7d5Mn4C" target="_blank">Robust stochastic linear contextual bandits under adversarial attacks</a></div>
      <div class="pub-authors">Qin Ding, Cho-Jui Hsieh, <strong>James Sharpnack</strong></div>
      <div class="pub-venue">International Conference on Artificial Intelligence and Statistics (AISTATS) <span class="venue-badge venue-good">AISTATS</span><span class="pub-year">2022</span></div>
    </div>

    <div class="publication-item">
      <div class="pub-title"><a href="https://scholar.google.com/citations?view_op=view_citation&hl=en&user=cXhAfX0AAAAJ&citation_for_view=cXhAfX0AAAAJ:k8Z6L05lTy4C" target="_blank">SSE-PT: Sequential recommendation via personalized transformer</a></div>
      <div class="pub-authors">Liwei Wu, Shuqing Li, Cho-Jui Hsieh, <strong>James Sharpnack</strong></div>
      <div class="pub-venue">ACM Conference on Recommender Systems <span class="venue-badge venue-good">RecSys</span><span class="pub-year">2020</span></div>
    </div>

    <div class="publication-item">
      <div class="pub-title"><a href="https://scholar.google.com/citations?view_op=view_citation&hl=en&user=cXhAfX0AAAAJ&citation_for_view=cXhAfX0AAAAJ:WF5omc3nYNoC" target="_blank">Graph DNA: Deep neighborhood aware graph encoding for collaborative filtering</a></div>
      <div class="pub-authors">Liwei Wu, Hsiang-Fu Yu, Nikhil Rao, <strong>James Sharpnack</strong>, Cho-Jui Hsieh</div>
      <div class="pub-venue">International Conference on Artificial Intelligence and Statistics (AISTATS) <span class="venue-badge venue-good">AISTATS</span><span class="pub-year">2020</span></div>
    </div>

    <div class="publication-item">
      <div class="pub-title"><a href="https://scholar.google.com/citations?view_op=view_citation&hl=en&user=cXhAfX0AAAAJ&citation_for_view=cXhAfX0AAAAJ:5qfkUJPXOUwC" target="_blank">RLSBench: Domain adaptation under relaxed label shift</a></div>
      <div class="pub-authors">Saurabh Garg, Nick Erickson, <strong>James Sharpnack</strong>, Alex Smola, Sivaraman Balakrishnan, Zachary Chase Lipton</div>
      <div class="pub-venue">International Conference on Machine Learning (ICML) <span class="venue-badge venue-top">ICML</span><span class="pub-year">2023</span></div>
    </div>

    <div class="publication-item">
      <div class="pub-title">Multimodal AutoML for Image, Text and Tabular Data</div>
      <div class="pub-authors">Nick Erickson, Xingjian Shi, <strong>James Sharpnack</strong>, Alexander Smola</div>
      <div class="pub-venue">ACM SIGKDD International Conference on Knowledge Discovery and Data Mining <span class="venue-badge venue-good">KDD</span><span class="pub-year">2022</span></div>
    </div>

    <div class="publication-item">
      <div class="pub-title"><a href="https://scholar.google.com/citations?view_op=view_citation&hl=en&user=cXhAfX0AAAAJ&citation_for_view=cXhAfX0AAAAJ:kz9GbA2Ns4gC" target="_blank">An efficient algorithm for generalized linear bandit: Online stochastic gradient descent and thompson sampling</a></div>
      <div class="pub-authors">Qin Ding, Cho-Jui Hsieh, <strong>James Sharpnack</strong></div>
      <div class="pub-venue">International Conference on Artificial Intelligence and Statistics (AISTATS) <span class="venue-badge venue-good">AISTATS</span><span class="pub-year">2021</span></div>
    </div>

    <div class="publication-item">
      <div class="pub-title"><a href="https://scholar.google.com/citations?view_op=view_citation&hl=en&user=cXhAfX0AAAAJ&citation_for_view=cXhAfX0AAAAJ:KUbvn5osdkgC" target="_blank">Stochastic Shared Embeddings: Data-driven Regularization of Embedding Layers</a></div>
      <div class="pub-authors">Liwei Wu, Shuqing Li, Cho-Jui Hsieh, <strong>James L Sharpnack</strong></div>
      <div class="pub-venue">Advances in Neural Information Processing Systems (NeurIPS) <span class="venue-badge venue-top">NeurIPS</span><span class="pub-year">2019</span></div>
    </div>

    <div class="publication-item">
      <div class="pub-title"><a href="https://scholar.google.com/citations?view_op=view_citation&hl=en&user=cXhAfX0AAAAJ&citation_for_view=cXhAfX0AAAAJ:BwyfMAYsbu0C" target="_blank">SQL-Rank: A Listwise Approach to Collaborative Ranking</a></div>
      <div class="pub-authors">Liwei Wu, Cho-Jui Hsieh, <strong>James Sharpnack</strong></div>
      <div class="pub-venue">International Conference on Machine Learning (ICML) <span class="venue-badge venue-top">ICML</span><span class="pub-year">2018</span></div>
    </div>

    <div class="publication-item">
      <div class="pub-title"><a href="https://scholar.google.com/citations?view_op=view_citation&hl=en&user=cXhAfX0AAAAJ&citation_for_view=cXhAfX0AAAAJ:YOwf2qJgpHMC" target="_blank">Large-scale Collaborative Ranking in Near-Linear Time</a></div>
      <div class="pub-authors">Liwei Wu, Cho-Jui Hsieh, <strong>James Sharpnack</strong></div>
      <div class="pub-venue">ACM SIGKDD International Conference on Knowledge Discovery and Data Mining <span class="venue-badge venue-good">KDD</span><span class="pub-year">2017</span></div>
    </div>

  </div>
</div>

<!-- Public Health & Epidemiology -->
<div class="publication-section" data-category="health">
  <h2 class="section-header health">🦠 Public Health & Epidemiology</h2>
  <div class="publication-list">

    <div class="publication-item">
      <div class="pub-title">Wastewater-based epidemiology for COVID-19: Handling qPCR nondetects and comparing spatially granular wastewater and clinical data trends</div>
      <div class="pub-authors">Hannah Safford, Rogelio E Zuniga-Montanez, Minji Kim, Xiaoliu Wu, Lifeng Wei, <strong>James Sharpnack</strong>, Karen Shapiro, Heather N Bischel</div>
      <div class="pub-venue">ACS ES&T Water <span class="venue-badge venue-journal">Journal</span><span class="pub-year">2022</span></div>
    </div>

    <div class="publication-item">
      <div class="pub-title"><a href="https://scholar.google.com/citations?view_op=view_citation&hl=en&user=cXhAfX0AAAAJ&citation_for_view=cXhAfX0AAAAJ:SpbeaW3--B0C" target="_blank">Beyond Cases and Deaths: The Benefits of Auxiliary Data Streams in Tracking the COVID-19 Pandemic</a></div>
      <div class="pub-authors">Daniel J McDonald, Jacob Bien, Alden Green, Addison J Hu, Nat DeFries, Sangwon Hyun, Natalia L Oliveira, <strong>James Sharpnack</strong>, Jingjing Tang, Robert Tibshirani, et al.</div>
      <div class="pub-venue">Proceedings of the National Academy of Sciences <span class="venue-badge venue-top">PNAS</span><span class="pub-year">2021</span></div>
    </div>

    <div class="publication-item">
      <div class="pub-title">An open repository of real-time COVID-19 indicators</div>
      <div class="pub-authors">Alex Reinhart, Logan Brooks, Maria Jahja, Aaron Rumack, Jingjing Tang, Sumit Agrawal, Wael Al Saeed, Taylor Arnold, Amartya Basu, Jacob Bien, et al.</div>
      <div class="pub-venue">Proceedings of the National Academy of Sciences <span class="venue-badge venue-top">PNAS</span><span class="pub-year">2021</span></div>
    </div>

    <div class="publication-item">
      <div class="pub-title">The impact of COVID-19 vaccination on California's return to normalcy</div>
      <div class="pub-authors">Maria L Daza-Torres, Yury E García, Alec J Schmidt, Brad H Pollock, <strong>James Sharpnack</strong>, Miriam Nuño</div>
      <div class="pub-venue">PLoS One <span class="venue-badge venue-journal">Journal</span><span class="pub-year">2022</span></div>
    </div>

    <div class="publication-item">
      <div class="pub-title">Impact of sensor data pre-processing strategies and selection of machine learning algorithm on the prediction of metritis events in dairy cattle</div>
      <div class="pub-authors">Gema Vidal, <strong>James Sharpnack</strong>, Pablo Pinedo, I Ching Tsai, Amanda Renee Lee, Beatriz Martínez-López</div>
      <div class="pub-venue">Preventive Veterinary Medicine <span class="venue-badge venue-journal">Journal</span><span class="pub-year">2023</span></div>
    </div>

    <div class="publication-item">
      <div class="pub-title">Comparative performance analysis of three machine learning algorithms applied to sensor data registered by a leg-attached accelerometer to predict metritis events in dairy cattle</div>
      <div class="pub-authors">Gema Vidal, <strong>James Sharpnack</strong>, Pablo Pinedo, I Ching Tsai, Amanda Renee Lee, Beatriz Martínez-López</div>
      <div class="pub-venue">Frontiers in Animal Science <span class="venue-badge venue-journal">Journal</span><span class="pub-year">2023</span></div>
    </div>

  </div>
</div>

<!-- Astronomical Discovery -->
<div class="publication-section" data-category="astronomy">
  <h2 class="section-header astronomy">🌌 Astronomical Discovery</h2>
  <div class="publication-list">

    <div class="publication-item">
      <div class="pub-title"><a href="https://scholar.google.com/citations?view_op=view_citation&hl=en&user=cXhAfX0AAAAJ&citation_for_view=cXhAfX0AAAAJ:_FxGoFyzp5QC" target="_blank">An Unsupervised Hunt for Gravitational Lenses</a></div>
      <div class="pub-authors">Stephen Sheng, Keerthi Vasan GC, Chi Po P Choi, <strong>James Sharpnack</strong>, Tucker Jones</div>
      <div class="pub-venue">International Conference on Artificial Intelligence and Statistics (AISTATS) <span class="venue-badge venue-good">AISTATS</span><span class="pub-year">2022</span></div>
    </div>

    <div class="publication-item">
      <div class="pub-title">Optimizing machine learning methods to discover strong gravitational lenses in the deep lens survey</div>
      <div class="pub-authors">Vasan GC Keerthi, Stephen Sheng, Tucker Jones, Chi Po Choi, <strong>James Sharpnack</strong></div>
      <div class="pub-venue">Monthly Notices of the Royal Astronomical Society <span class="venue-badge venue-journal">Journal</span><span class="pub-year">2023</span></div>
    </div>

  </div>
</div>

<!-- Statistical Theory & Methods -->
<div class="publication-section" data-category="theory">
  <h2 class="section-header theory">📊 Statistical Theory & Methods</h2>
  <div class="publication-list">

    <div class="publication-item">
      <div class="pub-title"><a href="https://scholar.google.com/citations?view_op=view_citation&hl=en&user=cXhAfX0AAAAJ&citation_for_view=cXhAfX0AAAAJ:Z5m8FVwuT1cC" target="_blank">Trend filtering on graphs</a></div>
      <div class="pub-authors">Yu-Xiang Wang, <strong>James Sharpnack</strong>, Alexander J Smola, Ryan J Tibshirani</div>
      <div class="pub-venue">Journal of Machine Learning Research (JMLR) <span class="venue-badge venue-journal">JMLR</span><span class="pub-year">2016</span></div>
    </div>

    <div class="publication-item">
      <div class="pub-title"><a href="https://scholar.google.com/citations?view_op=view_citation&hl=en&user=cXhAfX0AAAAJ&citation_for_view=cXhAfX0AAAAJ:RHpTSmoSYBkC" target="_blank">Near-optimal anomaly detection in graphs using Lovász extended scan statistic</a></div>
      <div class="pub-authors"><strong>James L Sharpnack</strong>, Akshay Krishnamurthy, Aarti Singh</div>
      <div class="pub-venue">Advances in Neural Information Processing Systems (NeurIPS) <span class="venue-badge venue-top">NeurIPS</span><span class="pub-year">2013</span></div>
    </div>

    <div class="publication-item">
      <div class="pub-title">Exponential family trend filtering on lattices</div>
      <div class="pub-authors">Veeranjaneyulu Sadhanala, Robert Bassett, <strong>James Sharpnack</strong>, Daniel J McDonald</div>
      <div class="pub-venue">Electronic Journal of Statistics <span class="venue-badge venue-journal">Journal</span><span class="pub-year">2024</span></div>
    </div>

    <div class="publication-item">
      <div class="pub-title">On L2-consistency of Nearest Neighbor Matching</div>
      <div class="pub-authors"><strong>James Sharpnack</strong></div>
      <div class="pub-venue">IEEE Transactions on Information Theory <span class="venue-badge venue-journal">Journal</span><span class="pub-year">2022</span></div>
    </div>

    <div class="publication-item">
      <div class="pub-title"><a href="https://scholar.google.com/citations?view_op=view_citation&hl=en&user=cXhAfX0AAAAJ&citation_for_view=cXhAfX0AAAAJ:ufrVoPGSRksC" target="_blank">Fused Density Estimation: Theory and Methods</a></div>
      <div class="pub-authors">Robert Bassett, <strong>James Sharpnack</strong></div>
      <div class="pub-venue">Journal of the Royal Statistical Society Series B <span class="venue-badge venue-journal">JRSS-B</span><span class="pub-year">2019</span></div>
    </div>

    <div class="publication-item">
      <div class="pub-title"><a href="https://scholar.google.com/citations?view_op=view_citation&hl=en&user=cXhAfX0AAAAJ&citation_for_view=cXhAfX0AAAAJ:lmc2jWPfTJgC" target="_blank">Adaptive nonparametric regression with the K-nearest neighbour fused lasso</a></div>
      <div class="pub-authors">Oscar Hernan Madrid Padilla, <strong>James Sharpnack</strong>, Yanzhen Chen, Daniela M Witten</div>
      <div class="pub-venue">Biometrika <span class="venue-badge venue-journal">Journal</span><span class="pub-year">2020</span></div>
    </div>

    <div class="publication-item">
      <div class="pub-title"><a href="https://scholar.google.com/citations?view_op=view_citation&hl=en&user=cXhAfX0AAAAJ&citation_for_view=cXhAfX0AAAAJ:UeHWp8X0CEIC" target="_blank">Learning Patterns for Detection with Multiscale Scan Statistics</a></div>
      <div class="pub-authors"><strong>James Sharpnack</strong></div>
      <div class="pub-venue">Conference on Learning Theory (COLT) <span class="venue-badge venue-good">COLT</span><span class="pub-year">2018</span></div>
    </div>

    <div class="publication-item">
      <div class="pub-title"><a href="https://scholar.google.com/citations?view_op=view_citation&hl=en&user=cXhAfX0AAAAJ&citation_for_view=cXhAfX0AAAAJ:URolC5Kub84C" target="_blank">A Sharp Error Analysis for the Fused Lasso, with Application to Approximate Changepoint Screening</a></div>
      <div class="pub-authors">Kevin Lin, <strong>James L Sharpnack</strong>, Alessandro Rinaldo, Ryan J Tibshirani</div>
      <div class="pub-venue">Advances in Neural Information Processing Systems (NeurIPS) <span class="venue-badge venue-top">NeurIPS</span><span class="pub-year">2017</span></div>
    </div>

    <div class="publication-item">
      <div class="pub-title"><a href="https://scholar.google.com/citations?view_op=view_citation&hl=en&user=cXhAfX0AAAAJ&citation_for_view=cXhAfX0AAAAJ:vDijr-p_gm4C" target="_blank">Higher-Order Total Variation Classes on Grids: Minimax Theory and Trend Filtering Methods</a></div>
      <div class="pub-authors">Veeranjaneyulu Sadhanala, Yu-Xiang Wang, <strong>James L Sharpnack</strong>, Ryan J Tibshirani</div>
      <div class="pub-venue">Advances in Neural Information Processing Systems (NeurIPS) <span class="venue-badge venue-top">NeurIPS</span><span class="pub-year">2017</span></div>
    </div>

    <div class="publication-item">
      <div class="pub-title"><a href="https://scholar.google.com/citations?view_op=view_citation&hl=en&user=cXhAfX0AAAAJ&citation_for_view=cXhAfX0AAAAJ:EkHepimYqZsC" target="_blank">The DFS fused lasso: Linear-time denoising over general graphs</a></div>
      <div class="pub-authors">Oscar Hernan Madrid Padilla, James G Scott, <strong>James Sharpnack</strong>, Ryan J Tibshirani</div>
      <div class="pub-venue">Journal of Machine Learning Research (JMLR) <span class="venue-badge venue-journal">JMLR</span><span class="pub-year">2017</span></div>
    </div>

    <div class="publication-item">
      <div class="pub-title"><a href="https://scholar.google.com/citations?view_op=view_citation&hl=en&user=cXhAfX0AAAAJ&citation_for_view=cXhAfX0AAAAJ:Ri6SYOTghG4C" target="_blank">Exact asymptotics for the scan statistic and fast alternatives</a></div>
      <div class="pub-authors"><strong>James Sharpnack</strong>, Ery Arias-Castro, et al.</div>
      <div class="pub-venue">Electronic Journal of Statistics <span class="venue-badge venue-journal">Journal</span><span class="pub-year">2016</span></div>
    </div>

    <div class="publication-item">
      <div class="pub-title"><a href="https://scholar.google.com/citations?view_op=view_citation&hl=en&user=cXhAfX0AAAAJ&citation_for_view=cXhAfX0AAAAJ:eQOLeE2rZwMC" target="_blank">Detecting anomalous activity on networks with the graph Fourier scan statistic</a></div>
      <div class="pub-authors"><strong>James Sharpnack</strong>, Alessandro Rinaldo, Aarti Singh</div>
      <div class="pub-venue">IEEE Transactions on Signal Processing <span class="venue-badge venue-journal">Journal</span><span class="pub-year">2016</span></div>
    </div>

    <div class="publication-item">
      <div class="pub-title"><a href="https://scholar.google.com/citations?view_op=view_citation&hl=en&user=cXhAfX0AAAAJ&citation_for_view=cXhAfX0AAAAJ:u-x6o8ySG0sC" target="_blank">Sparsistency of the edge lasso over graphs</a></div>
      <div class="pub-authors"><strong>James Sharpnack</strong>, Alessandro Rinaldo, Aarti Singh</div>
      <div class="pub-venue">International Conference on Artificial Intelligence and Statistics (AISTATS) <span class="venue-badge venue-good">AISTATS</span><span class="pub-year">2012</span></div>
    </div>

    <div class="publication-item">
      <div class="pub-title"><a href="https://scholar.google.com/citations?view_op=view_citation&hl=en&user=cXhAfX0AAAAJ&citation_for_view=cXhAfX0AAAAJ:Y0pCki6q_DkC" target="_blank">Changepoint detection over graphs with the spectral scan statistic</a></div>
      <div class="pub-authors"><strong>James Sharpnack</strong>, Alessandro Rinaldo, Aarti Singh</div>
      <div class="pub-venue">International Conference on Artificial Intelligence and Statistics (AISTATS) <span class="venue-badge venue-good">AISTATS</span><span class="pub-year">2012</span></div>
    </div>

    <div class="publication-item">
      <div class="pub-title"><a href="https://scholar.google.com/citations?view_op=view_citation&hl=en&user=cXhAfX0AAAAJ&citation_for_view=cXhAfX0AAAAJ:d1gkVwhDpl0C" target="_blank">Detecting activations over graphs using spanning tree wavelet bases</a></div>
      <div class="pub-authors"><strong>James Sharpnack</strong>, Akshay Krishnamurthy, Aarti Singh</div>
      <div class="pub-venue">International Conference on Artificial Intelligence and Statistics (AISTATS) <span class="venue-badge venue-good">AISTATS</span><span class="pub-year">2013</span></div>
    </div>

    <div class="publication-item">
      <div class="pub-title"><a href="https://scholar.google.com/citations?view_op=view_citation&hl=en&user=cXhAfX0AAAAJ&citation_for_view=cXhAfX0AAAAJ:IjCSPb-OGe4C" target="_blank">Estimating Graphlet Statistics via Lifting</a></div>
      <div class="pub-authors">Kirill Paramonov, Dmitry Shemetov, <strong>James Sharpnack</strong></div>
      <div class="pub-venue">ACM SIGKDD International Conference on Knowledge Discovery and Data Mining <span class="venue-badge venue-good">KDD</span><span class="pub-year">2019</span></div>
    </div>

    <div class="publication-item">
      <div class="pub-title"><a href="https://scholar.google.com/citations?view_op=view_citation&hl=en&user=cXhAfX0AAAAJ&citation_for_view=cXhAfX0AAAAJ:zYLM7Y9cAGgC" target="_blank">Variance function estimation in high-dimensions</a></div>
      <div class="pub-authors">Mladen Kolar, <strong>James Sharpnack</strong></div>
      <div class="pub-venue">International Conference on Machine Learning (ICML) <span class="venue-badge venue-top">ICML</span><span class="pub-year">2012</span></div>
    </div>

    <div class="publication-item">
      <div class="pub-title"><a href="https://scholar.google.com/citations?view_op=view_citation&hl=en&user=cXhAfX0AAAAJ&citation_for_view=cXhAfX0AAAAJ:u5HHmVD_uO8C" target="_blank">Identifying graph-structured activation patterns in networks</a></div>
      <div class="pub-authors"><strong>James Sharpnack</strong>, Aarti Singh</div>
      <div class="pub-venue">Advances in Neural Information Processing Systems (NeurIPS) <span class="venue-badge venue-top">NeurIPS</span><span class="pub-year">2010</span></div>
    </div>

  </div>
</div>

<!-- Cross-cutting & Other Applications -->
<div class="publication-section" data-category="other">
  <h2 class="section-header" style="background: linear-gradient(135deg, #34495e, #2c3e50); color: white;">🔬 Cross-cutting & Other Applications</h2>
  <div class="publication-list">

    <div class="publication-item">
      <div class="pub-title">Improving lung cancer diagnosis and survival prediction with deep learning and CT imaging</div>
      <div class="pub-authors">Xiawei Wang, <strong>James Sharpnack</strong>, Thomas CM Lee</div>
      <div class="pub-venue">PLoS One <span class="venue-badge venue-journal">Journal</span><span class="pub-year">2025</span></div>
    </div>

    <div class="publication-item">
      <div class="pub-title">Proteogenomic Analysis of Surgically Resected Lung Adenocarcinoma</div>
      <div class="pub-authors">Michael F Sharpnack, Nilini Ranbaduge, Arunima Srivastava, Ferdinando Cerciello, Simona G Codreanu, Daniel C Liebler, Celine Mascaux, Wayne O Miles, Robert Morris, Jason E McDermott, <strong>James Sharpnack</strong>, et al.</div>
      <div class="pub-venue">Journal of Thoracic Oncology <span class="venue-badge venue-journal">Journal</span><span class="pub-year">2018</span></div>
    </div>

    <div class="publication-item">
      <div class="pub-title"><a href="https://scholar.google.com/citations?view_op=view_citation&hl=en&user=cXhAfX0AAAAJ&citation_for_view=cXhAfX0AAAAJ:VaXvl8Fpj5cC" target="_blank">Psychological stress of bicycling with traffic: examining heart rate variability of bicyclists in natural urban environments</a></div>
      <div class="pub-authors">Dillon T Fitch, <strong>James Sharpnack</strong>, Susan L Handy</div>
      <div class="pub-venue">Transportation Research Part F: Traffic Psychology and Behaviour <span class="venue-badge venue-journal">Journal</span><span class="pub-year">2020</span></div>
    </div>

  </div>
</div>

<script>
// Search functionality
document.getElementById('searchBox').addEventListener('input', function(e) {
  const searchTerm = e.target.value.toLowerCase();
  const publications = document.querySelectorAll('.publication-item');
  
  publications.forEach(pub => {
    const text = pub.textContent.toLowerCase();
    if (text.includes(searchTerm)) {
      pub.style.display = 'block';
    } else {
      pub.style.display = 'none';
    }
  });
});

// Filter functionality
function filterPublications(category) {
  const sections = document.querySelectorAll('.publication-section');
  const buttons = document.querySelectorAll('.filter-btn');
  
  // Update button states
  buttons.forEach(btn => btn.classList.remove('active'));
  event.target.classList.add('active');
  
  // Show/hide sections
  sections.forEach(section => {
    if (category === 'all') {
      section.style.display = 'block';
    } else if (section.dataset.category === category) {
      section.style.display = 'block';
    } else {
      section.style.display = 'none';
    }
  });
}

// Handle hash-based filtering when page loads
document.addEventListener('DOMContentLoaded', function() {
  const hash = window.location.hash.replace('#', '');
  if (hash && ['education', 'health', 'astronomy', 'industry', 'theory'].includes(hash)) {
    // Simulate button click to trigger filtering
    const sections = document.querySelectorAll('.publication-section');
    const buttons = document.querySelectorAll('.filter-btn');
    
    // Update button states
    buttons.forEach(btn => btn.classList.remove('active'));
    document.querySelector(`button[onclick="filterPublications('${hash}')"]`)?.classList.add('active');
    
    // Show/hide sections
    sections.forEach(section => {
      if (section.dataset.category === hash) {
        section.style.display = 'block';
      } else {
        section.style.display = 'none';
      }
    });

    // Scroll to publications if coming from homepage
    if (document.referrer.includes(window.location.origin)) {
      document.querySelector('.publication-section').scrollIntoView({ behavior: 'smooth' });
    }
  }
});
</script>

