# When the Editing Intent Is Split: A Cross-Modal Jailbreak Attack for Large Image Editing Models

Official repository for **SIJA** and **SI2ESBench**.

🤗 **[SI2ESBench](https://huggingface.co/datasets/xianminye/SI2ESBench)** | 📄 **Paper (arXiv coming soon)**

---

## 📢 Updates

- **[2026-09]** SI2ESBench is released on Hugging Face.
- **[2026-09]** Our paper has been submitted to arXiv.

---

## ⚡️ Overview

We identify a **split-intent safety threat** in large image editing models and propose the **Split-Intent Jailbreak Attack (SIJA)**.

Unlike text-centric or vision-centric jailbreak attacks, SIJA distributes an unsafe editing intent across textual and visual inputs: the textual instruction identifies the editing referent, while the safety-critical action and specification are conveyed through graphical visual semantics in an auxiliary cue.

Neither component independently specifies the complete unsafe transformation. The intended edit emerges only through joint interpretation of the source image, textual instruction, and visual cue.

<p align="center">
  <img src="assets/overview.png" width="95%">
</p>

---

## 🗂 SI2ESBench

We introduce **SI2ESBench**, a benchmark for evaluating large image editing models under split-intent inputs.

SI2ESBench contains **766 manually validated instances** across **10 risk categories**, covering diverse editing operations and source-image contexts.

Each instance contains:

- a source image;
- a referent-identifying textual instruction;
- an action icon;
- an edit-specification image;
- semantic annotations and the corresponding risk category.

🤗 **Dataset:**  
https://huggingface.co/datasets/xianminye/SI2ESBench

---

## 📊 Evaluation

We evaluate SIJA using four complementary metrics:

- **ASR**: Attack Success Rate
- **HS**: Harmfulness Score
- **EV**: Editing Validity
- **HRR**: High-Risk Ratio

Our experiments cover seven representative commercial and open-source image editing models, together with one defense-enhanced configuration.

Detailed results and evaluation protocols are provided in the paper.

---

## 🛡️ Defense

To mitigate split-intent attacks, we formulate **editing-intent reconstruction** as a defense principle.

Instead of assessing individual inputs independently, the safeguard reconstructs the complete editing reference, action, and specification from the joint multimodal context before evaluating the safety of the resulting transformation.

---

## 🚀 Code

Code for SIJA evaluation and the editing-intent reconstruction defenses will be released soon.

---

## 🎓 Citation

The BibTeX entry will be updated once the arXiv page becomes publicly available.

---

## ❌ Disclaimer

This repository and SI2ESBench are intended solely for academic research on AI safety and the evaluation of large image editing models.

The benchmark contains unsafe or sensitive examples constructed for controlled safety evaluation. The released materials should be used responsibly and in compliance with applicable laws, model licenses, and platform policies.
