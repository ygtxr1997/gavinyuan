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
  - name: Ying Shan
    url: "https://scholar.google.com/citations?hl=en&user=4oXBp9UAAAAJ"
    affiliations: '2'
  - name: Huicheng Zheng
    url: "https://cse.sysu.edu.cn/content/2481"
    affiliations: '1'
    corresponding: True

affiliations:
  - name: "Sun Yat-sen University, China"
    idx: '1'
  - name: "Tencent AI Lab, China"
    idx: '2'

links:
  - name: "ArXiv"
    url: "https://arxiv.com"
  - name: "Supp"
    url: "https://github.com"
  - name: "Demo"
    url: "https://huggingface.com"

bibliography: 2023-02-03-superswap.bib

toc:
  - name: Equations
    # if a section has subsections, you can add them as follows:
    # subsections:
    #   - name: Example Child Subsection 1
    #   - name: Example Child Subsection 2
  - name: Citations
  - name: Footnotes
  - name: Code Blocks
  - name: Interactive Plots
  - name: Layouts
  - name: Other Typography?
---

<div class="centered"  style="width:80%">
  {% include figure.html path="assets/img/super_swap/fr_weakness.png" title="example image" class="img-fluid" %}
</div>
<div class="caption">
    (a) Our porposed SuperSwap achieves better identity preservation from sources. (b, c) Besides, we discover that the local details of lower face, such as face shape and mouth, largely affect vidual similarity but tend to be neglected by face recognition networks.
</div>

<h1>Abstract</h1>

Almost all advanced face swapping approaches use reconstruction as the proxy task, i.e., the supervision only exists when the training target and the source belong to the same person. Otherwise, lacking pixel-level supervision, these methods struggle for source identity preservation. This paper proposes to construct reliable supervision, dubbed **cycle triplets**, serving as the image-level guidance when the source identity differs from the target one. Specifically, we first use real face pairs to produce synthetic ones via traditional image blending techniques in computer graphics, aiming at preserving true identity of the source. Then based on the cycle relationship among real and synthetic faces, we reversely take synthetic ones as training inputs while real ones as supervisions to avoid the inheritance of artifacts in blended faces. Moreover, the identity extractors in previous method are face recognition models that cares about distinct facial features globally but tends to ignore some local attributes easy to recognize by human, particularly in nose, mouth, and face shape. To remedy this issue, we propose a **LowerNet** focusing on details of lower face. Our face swapping framework, named **SuperSwap**, does not depend on a specific backbone, where any existing network can be treated as a plug-in component. Extensive experiments demonstrate the efficacy of our SuperSwap, especially in identity preservation.

<h1>Cycle Relationship</h1>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/super_swap/typical_pipeline.png" title="example image" class="img-fluid" zoomable=true %}
    </div>
</div>
<div class="caption">
    Typical face swapping training process.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/super_swap/cycle.png" title="example image" class="img-fluid" zoomable=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/super_swap/table01.png" title="example image" class="img-fluid" zoomable=true %}
    </div>
</div>
<div class="caption">
    (Left) The cycle relationship among the items of cycle triplets. (Right) Training inputs and outputs of face swapping. The rows in gray indicate our cycle triplets joining the training.
</div>

<h1>Synthesizing Naive Triplets </h1>

Given a target face $$C_a$$ and a source one $$C_b$$ from real scenarios, we use a code $$(\sigma_1, \sigma_2, \sigma_3, \sigma_4, \sigma_5)$$ to represent the inherent five attributes of a face image, which are: background; pose and expression; light; eyes, nose, and mouth; face shape, respectively:
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/super_swap/triplet_overall.png" title="example image" class="img-fluid" zoomable=true %}
    </div>
</div>
<div class="caption">
    The pipeline of synthesizing naive triplets.
</div>

<div class="row mt-5 centered" style="max-width:80%">
    <div class="col-sm mt-5 mt-md-0">
        {% include figure.html path="assets/img/super_swap/triplet_shape.png" title="example image" class="img-fluid" zoomable=true %}
    </div>
</div>
<div class="caption">
    Segmentation-based dropping and inpainting in face reshaping step.
</div>

<h1>LowerNet</h1>

<div class="row mt-3 centered" style="max-width:80%">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/super_swap/lowernet.png" title="example image" class="img-fluid" zoomable=true%}
    </div>
</div>
<div class="caption">
    Training stage of LowerNet.
</div>

<h1>Results</h1>

<h2>1. Image Face Swapping</h2>

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

<h2>2. Video Face Swapping</h2>

<div class="centered container">
  <iframe class="video" width="100%" src="https://www.youtube.com/embed/uqe4pD-XpGE"></iframe> 
</div>

<h1>Reference</h1>

Coming soon.

<h1>Acknowledgements</h1>

Coming soon.
