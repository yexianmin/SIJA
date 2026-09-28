# When the Editing Intent Is Split: A Cross-Modal Jailbreak Attack for Large Image Editing Models

Official implementation of **SIJA** and **SI2ESBench**.

🌐 **[Project Page](TODO)** | 🎨 **[Dataset](TODO)** | 📄 **[Paper](TODO)**

---

## 📢 Updates

- **[2026-XX-XX]** Code and SI2ESBench released.
- **[2026-XX-XX]** Paper available on arXiv.

---

## ⚡️ Highlights

### Split-Intent Jailbreak Attack

We identify **split-intent**, a cross-modal safety threat in large image editing models.

Unlike existing attacks that place the complete harmful editing intent in either text or vision, **SIJA distributes complementary components of the editing intent across textual and visual inputs**. The textual instruction identifies the editing referent, while safety-critical editing semantics are concealed through graphical visual cues.

The complete unsafe transformation emerges only when the model jointly interprets the multimodal inputs.

<p align="center">
  <img src="assets/overview.png" width="95%">
</p>

### SI2ESBench

We introduce **SI2ESBench**, a benchmark for evaluating split-intent jailbreak attacks on large image editing models.

SI2ESBench covers **10 risk categories** and evaluates whether models can reconstruct and execute harmful transformations from distributed multimodal intent.

Each instance contains:

- a source image;
- a referent-identifying textual instruction;
- an auxiliary visual cue;
- the corresponding risk category and editing intent.

### Editing-Intent Reconstruction Defense

Motivated by SIJA, we formulate image-editing safety as an **editing-intent reconstruction** problem.

Instead of assessing individual inputs independently, the safeguard jointly reconstructs the intended editing reference, action, and specification from all textual and visual inputs, and evaluates the safety of the resulting transformation.

---

## 🚀 Setup

```bash
git clone TODO/SIJA.git
cd SIJA

conda create -n sija python=3.10 -y
conda activate sija
pip install -r requirements.txt
```

Detailed instructions for attack evaluation, defense evaluation, and benchmark usage will be provided with the code release.

---

## 📊 Evaluation

We evaluate SIJA on representative commercial and open-source image editing models using four metrics:

| Metric | Description |
|---|---|
| **ASR** | Attack Success Rate, measuring refusal bypass |
| **HS** | Harmfulness Score of the edited output |
| **EV** | Editing Validity of the intended transformation |
| **HRR** | High-Risk Ratio, measuring effective harmful edits |

Detailed model-wise and category-wise results are reported in the paper.

---

## 🗂 SI2ESBench

The benchmark will be released on Hugging Face.

🎨 **[Download SI2ESBench](TODO)**

A benchmark instance contains the source image, textual instruction, auxiliary visual cue, decomposed editing intent, and risk-category annotation.

---

## 🎓 Citation

If you find this work useful, please consider citing:

```bibtex
@misc{ye2026sija,
  title  = {When the Editing Intent Is Split: A Cross-Modal Jailbreak Attack for Large Image Editing Models},
  author = {Xianmin Ye and Zhiyuan Fan and Tianju Liu and Yuhang Wang and TODO},
  year   = {2026},
  eprint = {TODO},
  archivePrefix = {arXiv},
  primaryClass  = {cs.CV}
}
```

---

## ❌ Disclaimer

This repository is intended solely for academic research on AI safety and the evaluation of large image editing models.

The benchmark may contain unsafe or sensitive examples for safety evaluation. The released materials should only be used for responsible research and in compliance with applicable laws, model licenses, and platform policies.
