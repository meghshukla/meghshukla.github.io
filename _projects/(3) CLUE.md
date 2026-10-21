---
name: "CLUE: Modeling Uncertainty Propagation in 3D Morphable Models"
slug: clue
tools: [PhD Thesis, Uncertainty Estimation, 3D Morphable Models, Human Mesh Recovery]
image: /files/images/clue/card.jpg
description: '<img src="https://upload.wikimedia.org/wikipedia/commons/b/bc/ArXiv_logo_2022.svg" alt="arXiv Logo" style="width: 80px; height: auto;">'
---

<style>
.responsive-video {
  width: 100%;
  height: auto;
  max-width: 100%;
}
</style>


# Modeling Uncertainty Propagation in 3D Morphable Models
<br><br>
<span style="font-size:20px;">**Megh Shukla**, Edo Collins, Prashanth Chandran, Karel Petránek, Sergio Orts-Escolano, Mathieu Salzmann, Alexandre Alahi <br>
*EPFL, Google · arXiv preprint, 2026*</span>


<a href="https://arxiv.org/abs/2610.24646"><img alt="arXiv" src="https://img.shields.io/badge/arXiv-Paper%20(link)-black?style=flat&logo=arxiv&logoColor=%23B31B1B&logoSize=auto&labelColor=white" style="width: auto; height: 25px;"></a> <a href="https://github.com/vita-epfl/CLUE"><img alt="GitHub" src="https://img.shields.io/badge/GitHub-Code%20(link)-gray?style=flat&logo=GitHub&logoColor=black&logoSize=auto&labelColor=white" style="width: auto; height: 25px;"></a> <a href="https://huggingface.co/spaces/meghshukla/clue-demo"><img alt="Demo" src="https://img.shields.io/badge/Demo-Try%20it%20(link)-%23FF9D00?style=flat&logo=huggingface&logoColor=%23FFD21E&logoSize=auto&labelColor=white" style="width: auto; height: 25px;"></a> <a href="https://huggingface.co/meghshukla/clue"><img alt="Weights" src="https://img.shields.io/badge/Weights-Hugging%20Face%20(link)-%23C78C06?style=flat&logo=huggingface&logoColor=%23FFD21E&logoSize=auto&labelColor=white" style="width: auto; height: 25px;"></a><br>

<hr style="border: 1px solid gray;">

<video class="responsive-video" controls loop autoplay muted playsinline>
  <source src="/files/videos/clue/six_friends.mp4" type="video/mp4">
</video>
<span style="font-size: 14px; color: darkgray;"><em>For every person, CLUE predicts a 3D body mesh and colours each of its 18,439 vertices by how uncertain it is: blue where the model is sure, red where it is not. SAM 3D Body (grey) is shown for comparison.</em></span>
<br><br>


## TL;DR

3D Morphable Models describe a face or a body with a few hundred numbers, their parameters. Many methods also predict how uncertain they are about each of these numbers. But we never look at the numbers: we look at the mesh. **CLUE** translates uncertainty about the parameters into uncertainty at every point of the mesh, in closed form: no sampling, and fast enough to use in training. Trained with CLUE, a SAM 3D Body model matches SAM 3D Body's accuracy with a third of the training images, and tells you exactly which parts of the body it is unsure about.

<br><br>


## Why uncertainty on the mesh?

3D Morphable Models (3DMMs) such as FLAME for faces, and SMPL-X and MHR for bodies, are the backbone of digital humans. A typical application is human mesh recovery: reconstructing a person in 3D from a single photo. In-the-wild photos are hard: limbs are hidden behind other people, blurred by motion, or twisted into unusual poses. A good model should therefore not only reconstruct the person, but also say *how sure* it is.

Probabilistic models do this by predicting a spread, a variance, for each parameter. However, a variance on "joint angle number 47" or "shape coefficient number 3" means little to a person or to a downstream system. What we care about is **where** the reconstruction is uncertain: is it the hidden arm, the blurred leg, or the whole body? To answer that, the uncertainty has to be carried from the parameters onto the mesh.

<br><br>


## Moving uncertainty onto the mesh is expensive

Until now, there were two ways to do this:
1. **Sampling.** Draw around a hundred sets of parameters from the predicted distribution, build a hundred meshes, and measure how much each vertex moves across them.
2. **Error propagation.** Linearise the model and push the uncertainty through its derivatives (the Jacobian).

Both work, but both are slow and memory hungry: too slow to run at every training step or on a phone or a headset. The Jacobian is also not supported by some on-device machine learning runtimes.

<img src="/files/images/clue/runtime.jpg" alt="Runtime of CLUE, sampling and the Jacobian" style="width: 45%; height: auto;">
<br>
<span style="font-size: 14px; color: darkgray;"><em>Time to compute the per-vertex uncertainty of a FLAME face on one CPU. CLUE takes 3.5 ms, about 40 times faster than sampling 100 meshes.</em></span>

<br><br>


## CLUE in a nutshell (no equations, promise!)

A 3DMM builds a mesh in two steps. First, it adds shape and expression offsets to a template, giving a mesh in a neutral pose. Then, it poses this mesh by rotating each joint of a skeleton. CLUE follows the same two steps, and asks one question for each:

🔹 **Shape and expression.** If the shape is uncertain, how much does each vertex move on the neutral mesh? This uncertainty then simply travels with the vertex into the final pose.

🔹 **Pose.** If the rotation of a joint is uncertain, every vertex below it in the skeleton swings around it, like the end of a lever. The further the vertex is from the joint, the more it moves: the same uncertain shoulder moves the fingertips more than the elbow. Uncertainty flows down the skeleton, from the shoulder to the hand, but never across it.

CLUE adds the two contributions, separately for every vertex. Since both follow directly from the structure of the 3DMM, the result comes out in closed form: no samples, and no derivatives of the model. As a bonus, the uncertainty stays interpretable, since we know how much of it comes from shape, expression or pose. For the derivation, please refer to Section 3 and Appendix A of the [paper](https://arxiv.org/abs/2610.24646).

<br><br>


## Watch uncertainty propagate

To build some intuition, we move one parameter back and forth while giving it some uncertainty, and colour the mesh by the per-vertex uncertainty that CLUE computes: blue where the mesh is certain, red where it is not.

<div style="display: flex; justify-content: space-between; gap: 12px; text-align: center;">
  <div style="width: 32%;">
    <video class="responsive-video" autoplay loop muted playsinline>
      <source src="/files/videos/clue/sweep_smplx_shoulder_hip.mp4" type="video/mp4">
    </video>
    <span style="font-size: 14px; color: darkgray;"><em>Shoulder and hip rotation: the uncertainty grows towards the hand and the foot, like the end of a lever.</em></span>
  </div>
  <div style="width: 32%;">
    <video class="responsive-video" autoplay loop muted playsinline>
      <source src="/files/videos/clue/sweep_smplx_spine.mp4" type="video/mp4">
    </video>
    <span style="font-size: 14px; color: darkgray;"><em>Spine rotation: everything above the waist becomes uncertain, the hands most of all.</em></span>
  </div>
  <div style="width: 32%;">
    <video class="responsive-video" autoplay loop muted playsinline>
      <source src="/files/videos/clue/sweep_smplx_shape.mp4" type="video/mp4">
    </video>
    <span style="font-size: 14px; color: darkgray;"><em>Body shape: the uncertainty spreads over the whole body, centred on the torso.</em></span>
  </div>
</div>
<br>
<div style="display: flex; justify-content: space-between; gap: 12px; text-align: center;">
  <div style="width: 32%;">
    <video class="responsive-video" autoplay loop muted playsinline>
      <source src="/files/videos/clue/sweep_flame_expression.mp4" type="video/mp4">
    </video>
    <span style="font-size: 14px; color: darkgray;"><em>An expression: the corners of the mouth.</em></span>
  </div>
  <div style="width: 32%;">
    <video class="responsive-video" autoplay loop muted playsinline>
      <source src="/files/videos/clue/sweep_flame_jaw.mp4" type="video/mp4">
    </video>
    <span style="font-size: 14px; color: darkgray;"><em>The jaw: the chin and the lower lip.</em></span>
  </div>
  <div style="width: 32%;">
    <video class="responsive-video" autoplay loop muted playsinline>
      <source src="/files/videos/clue/sweep_flame_neck.mp4" type="video/mp4">
    </video>
    <span style="font-size: 14px; color: darkgray;"><em>The neck: the whole head, and its top most of all.</em></span>
  </div>
</div>

**Play with it.** Each of the FLAME, SMPL-X and MHR folders in our [code](https://github.com/vita-epfl/CLUE) comes with an interactive viewer. Every parameter has a second slider for its uncertainty: move either one, and CLUE recolours the mesh as you go.

<img src="/files/images/clue/flame_viewer.png" alt="FLAME interactive viewer: parameter and uncertainty sliders on the left, the mesh coloured by per-vertex uncertainty on the right" style="width: 100%; height: auto;">
<span style="font-size: 14px; color: darkgray;"><em>The FLAME viewer: giving one expression parameter some uncertainty lights up the mouth and the cheeks.</em></span>

```bash
cd FLAME            # or SMPLX, MHR
python demo.py
```

<br><br>


## Is CLUE accurate?

We first test CLUE as a pure translation from parameter uncertainty to mesh uncertainty. We give random faces and bodies some parameter uncertainty, compute the "true" per-vertex uncertainty from 10,000 samples, and compare each method against it.

<img src="/files/images/clue/flame_error_maps.jpg" alt="FLAME error maps" style="width: 100%; height: auto;">
<span style="font-size: 14px; color: darkgray;"><em>Left: the true per-vertex uncertainty of four random FLAME faces. Right: the error of each method against it (the lighter the face, the smaller the error). Sampling needs around 1,000 meshes to become accurate; the Jacobian and CLUE are accurate right away.</em></span>

CLUE comes close to the Jacobian's accuracy, while needing about 4 MB of extra memory instead of 410 MB, and over 50 times fewer operations than sampling 100 meshes. This makes CLUE suitable for on-device uncertainty estimation. CLUE is an approximation: it ignores how vertices move together and the small pose-dependent corrections of the 3DMM, so it can slightly overestimate the uncertainty, for instance on the forehead when the jaw moves.

<details>
  <summary> <strong>More error maps: FLAME, SMPL-X and MHR</strong> </summary>

<img src="/files/images/clue/error_maps_flame_groups.jpg" alt="FLAME error maps per parameter group" style="width: 100%; height: auto;">
<span style="font-size: 14px; color: darkgray;"><em>FLAME: one parameter group at a time (shape, expression, jaw, neck).</em></span>

<img src="/files/images/clue/error_maps_smplx.jpg" alt="SMPL-X error maps" style="width: 100%; height: auto;">
<span style="font-size: 14px; color: darkgray;"><em>SMPL-X.</em></span>

<img src="/files/images/clue/error_maps_mhr.jpg" alt="MHR error maps" style="width: 100%; height: auto;">
<span style="font-size: 14px; color: darkgray;"><em>MHR.</em></span>

</details>

<br><br>


## Training a human mesh model with CLUE

Next, we use CLUE to train an in-the-wild human mesh recovery model. We take SAM 3D Body's architecture, keep its DINOv3 backbone frozen, and train the rest from scratch. A small variance head, two layers on top of the decoder, predicts how uncertain each shape and pose parameter is. CLUE turns these into an uncertainty for every vertex and every joint, so the model can be trained to be both correct and honest directly on the mesh and the joints. Since CLUE carries the uncertainty through the body's geometry, the geometry guides what the model learns about its own uncertainty.

<video class="responsive-video" controls loop autoplay muted playsinline>
  <source src="/files/videos/clue/backflip.mp4" type="video/mp4">
</video>
<span style="font-size: 14px; color: darkgray;"><em>A dancer's back walkover: the uncertainty rises as the body turns and the limbs blur.</em></span>
<br><br>

We compare CLUE against deterministic training (no uncertainty) and three probabilistic objectives that predict the uncertainty directly over the parameters (Parameter NLL, Matrix-Fisher and Normalizing Flow), all trained the same way on 1.2M images. CLUE is trained on the 3DMM parameters and the joints. Errors are in millimetres, lower is better: MPJPE measures the joints, PVE the surface of the body.

| Training objective | 3DPW MPJPE | 3DPW PVE | EMDB MPJPE | EMDB PVE |
|---|:-:|:-:|:-:|:-:|
| Deterministic | 62.7 | 72.9 | 71.9 | 85.5 |
| Parameter NLL | 57.9 | 68.9 | 66.4 | 79.5 |
| Matrix-Fisher | 58.0 | 68.8 | 68.8 | 81.7 |
| Normalizing Flow | 58.3 | 68.9 | 68.0 | 80.7 |
| **CLUE** | **56.1** | **67.0** | **65.4** | **77.9** |

All probabilistic objectives beat deterministic training, and CLUE is the best of them. When trained longer, CLUE also holds its own against the released SAM 3D Body, which was trained on three times as many images:

| | Training images | 3DPW MPJPE | 3DPW PVE | EMDB MPJPE | EMDB PVE |
|---|:-:|:-:|:-:|:-:|:-:|
| SAM 3D Body | 3.8M (with multi-view) | 56.0 | 67.1 | **63.2** | **74.7** |
| **CLUE** | **1.2M** (single view) | **55.8** | **66.4** | 64.9 | 77.0 |

CLUE is slightly better on 3DPW and slightly behind on EMDB. Our take: probabilistic training reasons better under ambiguity, but cannot invent poses it has never seen, so it pairs best with a diverse dataset.

<img src="/files/images/clue/hmr_error_maps.jpg" alt="Per-vertex error maps of the baselines and CLUE" style="width: 100%; height: auto;">
<span style="font-size: 14px; color: darkgray;"><em>Per-vertex error against the reference mesh (yellow). The baselines struggle with occluded limbs and complex poses, and in hard poses spread their error over the whole body. CLUE keeps the error on the extremities.</em></span>

**Does the uncertainty match the error?** A useful uncertainty is high exactly where the model is wrong. For each of the 19 parts of the MHR body, we measure how well each method's predicted uncertainty ranks its actual errors. CLUE has the highest correlation for every part of the body.

<img src="/files/images/clue/spearman.jpg" alt="Correlation between uncertainty and error for each body part" style="width: 100%; height: auto;">
<span style="font-size: 14px; color: darkgray;"><em>Correlation between the predicted uncertainty and the actual error, for each part of the body (blue is better).</em></span>

<details>
  <summary> <strong>More error maps</strong> </summary>

<img src="/files/images/clue/hmr_error_maps_more.jpg" alt="More per-vertex error maps" style="width: 100%; height: auto;">

</details>

<br><br>


## What can you do with fine-grained uncertainty?

**Data mining.** Since CLUE's uncertainty is fine-grained, we can ask questions that parameter uncertainty cannot answer, such as: *in which images is the left arm much more uncertain than the rest of the body?* To compare vertices and methods fairly, each vertex's uncertainty is expressed as a percentile: how unusual it is for that vertex. CLUE pinpoints the limbs that are hidden or blurred, while the rest of the body stays confident. The baselines tend to light up the whole body: they can tell that an image is hard, but not why.

<img src="/files/images/clue/data_mining.jpg" alt="Uncertainty based data mining" style="width: 100%; height: auto;">
<span style="font-size: 14px; color: darkgray;"><em>Images retrieved automatically by asking for a limb whose uncertainty stands out from the rest of the body.</em></span>

Our code includes this as an [Agent Skill](https://github.com/vita-epfl/CLUE/tree/main/data-mining) for coding agents: ask *"find the frames where the left arm is most uncertain"*, or *"find the people whose body shape is hard to estimate"*, and get the frames back.

<details>
  <summary> <strong>More data mining examples</strong> </summary>

<img src="/files/images/clue/data_mining_more.jpg" alt="More data mining examples" style="width: 100%; height: auto;">

</details>
<br>

**Decision making.** In a headset, a camera looks at the lower face to animate an avatar (this study uses an internal dataset). When a hand covers the mouth, the tracker should not keep going blindly. With CLUE, the uncertainty concentrates on the covered region and grows as more of it is hidden, so the system can pause tracking, trust it less, or switch to another sensor until the face is visible again.

<img src="/files/images/clue/egocentric.jpg" alt="Uncertainty in egocentric face tracking" style="width: 100%; height: auto;">
<span style="font-size: 14px; color: darkgray;"><em>Top: frames from a headset camera, with the mouth progressively covered. Bottom: the tracked face, coloured by per-vertex uncertainty in millimetres.</em></span>

<br><br>


## SAM 3D Body (CLUE): uncertainty for your SAM 3D Body pipeline

Already using Meta's [SAM 3D Body](https://github.com/facebookresearch/sam-3d-body)? We trained a small uncertainty head (6 MB) on top of the frozen, released model. Our [plugin](https://github.com/vita-epfl/CLUE/tree/main/ITW/inference/plugin) attaches it to your existing code: the meshes, keypoints and cameras stay exactly the same, and each person gets a per-vertex uncertainty on top.

```python
from sam3dbody_clue import SAM3DBodyCLUE

clue = SAM3DBodyCLUE(estimator)                 # Add a hook to integrate CLUE into SAM 3D Body

# CLUE supported for inference_type = 'body', for 'full' original code behaviour maintained without CLUE
outputs = estimator.process_one_image(image, inference_type="body")   # outputs[i]["vertex_sigma_cm"]: per-vertex std in cm
```

<video class="responsive-video" controls loop autoplay muted playsinline>
  <source src="/files/videos/clue/sam3dbody_clue.mp4" type="video/mp4">
</video>
<span style="font-size: 14px; color: darkgray;"><em>SAM 3D Body (CLUE) on in-the-wild videos.</em></span>

<details>
  <summary> <strong>More examples</strong> </summary>

<img src="/files/images/clue/sam3dbody_clue_1.jpg" alt="SAM 3D Body and SAM 3D Body (CLUE), part 1" style="width: 100%; height: auto;">
<img src="/files/images/clue/sam3dbody_clue_2.jpg" alt="SAM 3D Body and SAM 3D Body (CLUE), part 2" style="width: 100%; height: auto;">

</details>

<br><br>


## Try it yourself

🔹 **In your browser:** the [demo](https://huggingface.co/spaces/meghshukla/clue-demo) runs SAM 3D Body and CLUE side by side on your own images and videos, no installation needed.<br>
🔹 **On your machine:** the [code](https://github.com/vita-epfl/CLUE) runs SAM 3D Body, SAM 3D Body (CLUE) and CLUE on images, videos and folders, and reproduces our experiments on FLAME, SMPL-X and MHR.<br>
🔹 **The weights:** CLUE and SAM 3D Body (CLUE) are on [Hugging Face](https://huggingface.co/meghshukla/clue).<br>

<br><br>


## Conclusion

Our study is best concluded by the following points:<br>
🔹 Uncertainty is most useful when you can see where it is: on the mesh, not in parameter space.<br>
🔹 CLUE maps parameter uncertainty onto every vertex in closed form: accurate, about 40 times faster than sampling, and light enough for on-device use.<br>
🔹 In training, CLUE lets the body's geometry guide the uncertainty: better meshes than deterministic and probabilistic baselines, and uncertainty that tracks the actual error.<br>
🔹 Fine-grained uncertainty enables data mining and safer decisions downstream, and SAM 3D Body (CLUE) brings it to SAM 3D Body in three lines of code.<br>

<br><br>


## Citation

If our work is useful, please consider citing the accompanying paper and starring our code on GitHub!

```
@misc{shukla2026modelinguncertaintypropagation3d,
      title={Modeling Uncertainty Propagation in 3D Morphable Models},
      author={Megh Shukla and Edo Collins and Prashanth Chandran and Karel Petránek and Sergio Orts-Escolano and Mathieu Salzmann and Alexandre Alahi},
      year={2026},
      eprint={2610.24646},
      archivePrefix={arXiv},
      primaryClass={cs.CV},
      url={https://arxiv.org/abs/2610.24646},
}
```
