---
layout: paper
title: 'SuperSwap: Enhancing General Face Swapping with Reliable Supervision'
description: Under reviewed
img: assets/img/12.jpg
importance: 1
category: work

date: 2023-02-03

authors:
  - name: Ge Yuan
    url: "https://en.wikipedia.org/wiki/Albert_Einstein"
    affiliations: '1,2'
    equal: True
  - name: Maomao Li
    url: "https://en.wikipedia.org/wiki/Boris_Podolsky"
    affiliations: '2'
    equal: True
  - name: Yong Zhang
    url: "https://en.wikipedia.org/wiki/Nathan_Rosen"
    affiliations: '2'
  - name: Ying Shan
    affiliations: '2'
  - name: Huicheng Zheng
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

<h1>Abstract</h1>

Almost all advanced face swapping approaches use reconstruction as the proxy task, i.e., the supervision only exists when the training target and the source belong to the same person. Otherwise, lacking pixel-level supervision, these methods struggle for source identity preservation. This paper proposes to construct reliable supervision, dubbed **cycle triplets**, serving as the image-level guidance when the source identity differs from the target one. Specifically, we first use real face pairs to produce synthetic ones via traditional image blending techniques in computer graphics, aiming at preserving true identity of the source. Then based on the cycle relationship among real and synthetic faces, we reversely take synthetic ones as training inputs while real ones as supervisions to avoid the inheritance of artifacts in blended faces. Moreover, the identity extractors in previous method are face recognition models that cares about distinct facial features globally but tends to ignore some local attributes easy to recognize by human, particularly in nose, mouth, and face shape. To remedy this issue, we propose a **LowerNet** focusing on details of lower face. Our face swapping framework, named **SuperSwap**, does not depend on a specific backbone, where any existing network can be treated as a plug-in component. Extensive experiments demonstrate the efficacy of our SuperSwap, especially in identity preservation.

<h1>Cycle triplet relationship</h1>

Almost all advanced face swapping approaches use reconstruction as the proxy task, i.e., the supervision only exists when the training target and the source belong to the same person. Otherwise, lacking pixel-level supervision, these methods struggle for source identity preservation. This paper proposes to construct reliable supervision, dubbed **cycle triplets**, serving as the image-level guidance when the source identity differs from the target one. Specifically, we first use real face pairs to produce synthetic ones via traditional image blending techniques in computer graphics, aiming at preserving true identity of the source. Then based on the cycle relationship among real and synthetic faces, we reversely take synthetic ones as training inputs while real ones as supervisions to avoid the inheritance of artifacts in blended faces. Moreover, the identity extractors in previous method are face recognition models that cares about distinct facial features globally but tends to ignore some local attributes easy to recognize by human, particularly in nose, mouth, and face shape. To remedy this issue, we propose a **LowerNet** focusing on details of lower face. Our face swapping framework, named **SuperSwap**, does not depend on a specific backbone, where any existing network can be treated as a plug-in component. Extensive experiments demonstrate the efficacy of our SuperSwap, especially in identity preservation.

<h1>LowerNet</h1>

Almost all advanced face swapping approaches use reconstruction as the proxy task, i.e., the supervision only exists when the training target and the source belong to the same person. Otherwise, lacking pixel-level supervision, these methods struggle for source identity preservation. This paper proposes to construct reliable supervision, dubbed **cycle triplets**, serving as the image-level guidance when the source identity differs from the target one. Specifically, we first use real face pairs to produce synthetic ones via traditional image blending techniques in computer graphics, aiming at preserving true identity of the source. Then based on the cycle relationship among real and synthetic faces, we reversely take synthetic ones as training inputs while real ones as supervisions to avoid the inheritance of artifacts in blended faces. Moreover, the identity extractors in previous method are face recognition models that cares about distinct facial features globally but tends to ignore some local attributes easy to recognize by human, particularly in nose, mouth, and face shape. To remedy this issue, we propose a **LowerNet** focusing on details of lower face. Our face swapping framework, named **SuperSwap**, does not depend on a specific backbone, where any existing network can be treated as a plug-in component. Extensive experiments demonstrate the efficacy of our SuperSwap, especially in identity preservation.

<h1>Results</h1>

<h2>1. Image Face Swapping</h2>

Almost all advanced face swapping approaches use reconstruction as the proxy task, i.e., the supervision only exists when the training target and the source belong to the same person. Otherwise, lacking pixel-level supervision, these methods struggle for source identity preservation. This paper proposes to construct reliable supervision, dubbed **cycle triplets**, serving as the image-level guidance when the source identity differs from the target one. Specifically, we first use real face pairs to produce synthetic ones via traditional image blending techniques in computer graphics, aiming at preserving true identity of the source. Then based on the cycle relationship among real and synthetic faces, we reversely take synthetic ones as training inputs while real ones as supervisions to avoid the inheritance of artifacts in blended faces. Moreover, the identity extractors in previous method are face recognition models that cares about distinct facial features globally but tends to ignore some local attributes easy to recognize by human, particularly in nose, mouth, and face shape. To remedy this issue, we propose a **LowerNet** focusing on details of lower face. Our face swapping framework, named **SuperSwap**, does not depend on a specific backbone, where any existing network can be treated as a plug-in component. Extensive experiments demonstrate the efficacy of our SuperSwap, especially in identity preservation.

<h2>2. Video Face Swapping</h2>

Almost all advanced face swapping approaches use reconstruction as the proxy task, i.e., the supervision only exists when the training target and the source belong to the same person. Otherwise, lacking pixel-level supervision, these methods struggle for source identity preservation. This paper proposes to construct reliable supervision, dubbed **cycle triplets**, serving as the image-level guidance when the source identity differs from the target one. Specifically, we first use real face pairs to produce synthetic ones via traditional image blending techniques in computer graphics, aiming at preserving true identity of the source. Then based on the cycle relationship among real and synthetic faces, we reversely take synthetic ones as training inputs while real ones as supervisions to avoid the inheritance of artifacts in blended faces. Moreover, the identity extractors in previous method are face recognition models that cares about distinct facial features globally but tends to ignore some local attributes easy to recognize by human, particularly in nose, mouth, and face shape. To remedy this issue, we propose a **LowerNet** focusing on details of lower face. Our face swapping framework, named **SuperSwap**, does not depend on a specific backbone, where any existing network can be treated as a plug-in component. Extensive experiments demonstrate the efficacy of our SuperSwap, especially in identity preservation.

<h1>Reference</h1>

Almost all advanced face swapping approaches use reconstruction as the proxy task, i.e., the supervision only exists when the training target and the source belong to the same person. Otherwise, lacking pixel-level supervision, these methods struggle for source identity preservation. This paper proposes to construct reliable supervision, dubbed **cycle triplets**, serving as the image-level guidance when the source identity differs from the target one. Specifically, we first use real face pairs to produce synthetic ones via traditional image blending techniques in computer graphics, aiming at preserving true identity of the source. Then based on the cycle relationship among real and synthetic faces, we reversely take synthetic ones as training inputs while real ones as supervisions to avoid the inheritance of artifacts in blended faces. Moreover, the identity extractors in previous method are face recognition models that cares about distinct facial features globally but tends to ignore some local attributes easy to recognize by human, particularly in nose, mouth, and face shape. To remedy this issue, we propose a **LowerNet** focusing on details of lower face. Our face swapping framework, named **SuperSwap**, does not depend on a specific backbone, where any existing network can be treated as a plug-in component. Extensive experiments demonstrate the efficacy of our SuperSwap, especially in identity preservation.

<h1>Acknowledgements</h1>

Almost all advanced face swapping approaches use reconstruction as the proxy task, i.e., the supervision only exists when the training target and the source belong to the same person. Otherwise, lacking pixel-level supervision, these methods struggle for source identity preservation. This paper proposes to construct reliable supervision, dubbed **cycle triplets**, serving as the image-level guidance when the source identity differs from the target one. Specifically, we first use real face pairs to produce synthetic ones via traditional image blending techniques in computer graphics, aiming at preserving true identity of the source. Then based on the cycle relationship among real and synthetic faces, we reversely take synthetic ones as training inputs while real ones as supervisions to avoid the inheritance of artifacts in blended faces. Moreover, the identity extractors in previous method are face recognition models that cares about distinct facial features globally but tends to ignore some local attributes easy to recognize by human, particularly in nose, mouth, and face shape. To remedy this issue, we propose a **LowerNet** focusing on details of lower face. Our face swapping framework, named **SuperSwap**, does not depend on a specific backbone, where any existing network can be treated as a plug-in component. Extensive experiments demonstrate the efficacy of our SuperSwap, especially in identity preservation.
