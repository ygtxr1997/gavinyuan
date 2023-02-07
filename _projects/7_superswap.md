---
layout: paper
title: 'SuperSwap: Enhancing General Face Swapping with Reliable Supervision'
description: 'Under reviewed'
img: assets/img/super_swap/fr_weakness.png
importance: 1
category: paper

date: 2023-02-03

authors:
  - name: Ge Yuan
    url: "https://ygtxr1997.github.io"
    affiliations: '1,2'
    equal: True
  - name: Maomao Li
    url: "https://scholar.google.com/citations?hl=en&user=ym_t6QYAAAAJ"
    affiliations: '2'
    equal: True
  - name: Yong Zhang
    url: "https://yzhang2016.github.io/yongnorriszhang.github.io/"
    affiliations: '2'
    corresponding: True
  - name: Ying Shan
    url: "https://scholar.google.com/citations?hl=en&user=4oXBp9UAAAAJ"
    affiliations: '2'
  - name: Huicheng Zheng
    url: "https://cse.sysu.edu.cn/content/2481"
    affiliations: '1'
    corresponding: True

affiliations:
  - name: "Sun Yat-sen University"
    idx: '1'
  - name: "Tencent AI Lab"
    idx: '2'

links:
  - name: "ArXiv"
    url: "https://arxiv.com"
  - name: "Supp"
    url: "https://github.com"
  - name: "Demo"
    url: "https://huggingface.com"

bibliography: 2023-02-03-.bib
---

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.html path="assets/img/super_swap/fr_weakness.png" title="example image" class="img-fluid" zoomable=true %}
  </div>
  <div class="col">
    <div class="col-sm mt-3 mt-md-0 centered">
      {% include figure.html path="assets/img/super_swap/cycle.png" title="example image" class="img-fluid" zoomable=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0 centered">
      {% include figure.html path="assets/img/super_swap/table01.png" title="example image" class="img-fluid" zoomable=true %}
    </div>
  </div>
</div>

<h1>Abstract</h1>

Almost all advanced face swapping approaches use reconstruction as the proxy task, i.e., the supervision only exists when the training target and the source belong to the same person. Otherwise, lacking pixel-level supervision, these methods struggle for source identity preservation. This paper proposes to construct reliable supervision, dubbed **cycle triplets**, serving as the image-level guidance when the source identity differs from the target one. Specifically, we first use real face pairs to produce synthetic ones via traditional image blending techniques in computer graphics, aiming at preserving true identity of the source. Then based on the cycle relationship among real and synthetic faces, we reversely take synthetic ones as training inputs while real ones as supervisions to avoid the inheritance of artifacts in blended faces. Moreover, the identity extractors in previous method are face recognition models that cares about distinct facial features globally but tends to ignore some local attributes easy to recognize by human, particularly in nose, mouth, and face shape. To remedy this issue, we propose a **LowerNet** focusing on details of lower face. Our face swapping framework, named **SuperSwap**, does not depend on a specific backbone, where any existing network can be treated as a plug-in component. Extensive experiments demonstrate the efficacy of our SuperSwap, especially in identity preservation.

<h1>Image Face Swapping</h1>

<div class="col-sm mt-3 mt-md-0 centered">
    {% include figure.html path="assets/img/super_swap/web_results.png" title="example image" class="img-fluid" zoomable=true%}
</div>
<div class="caption">
    Results on images collected from the web.
</div>

<div class="col-sm mt-3 mt-md-0 centered">
    {% include figure.html path="assets/img/super_swap/celebahq.png" title="example image" class="img-fluid" zoomable=true%}
</div>
<div class="caption">
    Results on CelebA-HQ.
</div>

<div class="col-sm mt-3 mt-md-0 centered" style="max-width:80%">
    {% include figure.html path="assets/img/super_swap/ffplus.png" title="example image" class="img-fluid" zoomable=true%}
</div>
<div class="caption">
    Results on FF+.
</div>

<h1>Video Face Swapping</h1>

<div class="centered container">
  <iframe class="video" width="100%" src="https://www.youtube.com/embed/uqe4pD-XpGE"></iframe> 
</div>

<h1>Reference</h1>

Coming soon.

<h1>Acknowledgements</h1>

Coming soon.
