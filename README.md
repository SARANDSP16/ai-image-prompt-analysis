# AI Image Prompt-Output Match Analysis

## 🌟 Overview

This project is a detailed analysis of the **match quality** between AI-generated images and their corresponding **text prompts**. It utilizes a Vision-Language Model (such as CLIP) to calculate and quantify the semantic similarity between three components:
1.  **Prompt** (The original user input) and the **Generated Image**.
2.  **Caption** (A machine-generated description of the image) and the **Generated Image**.

The goal is to evaluate the fidelity of the image generation model—how accurately the output image reflects the input prompt—and to compare this against a secondary, auto-generated caption.

---

## 📊 Analysis Summary

The following statistics were generated from the run performed on **2025-10-30**, analyzing **5000** generated images.

### Key Insights

| Metric | Value | Interpretation |
| :--- | :--- | :--- |
| **Average Match Quality (Prompt-Image)** | **32.05/100** | The mean semantic similarity score between the input text prompt and the resulting image. |
| **High-Quality Matches (>25)** | **95.22%** | The percentage of samples where the Prompt-Image similarity score was above 25, indicating a strong performance. |
| **Poor Matches (<20)** | **0.56%** | A very small percentage of samples where the model significantly failed to match the prompt. |
| **Avg Prompt vs Caption Diff** | **3.1109** | The average difference in similarity when comparing the **Prompt-Image** score to the **Caption-Image** score. |

### Detailed Similarity Scores

#### Prompt-Image Similarity

This measures how well the image matches the **original user prompt**.

| Statistic | Value |
| :--- | :--- |
| **Mean** | 32.0450 |
| **Median** | 32.2188 |
| **Standard Deviation** | 4.0317 |
| **Minimum Score** | 5.1875 |
| **Maximum Score** | 46.0000 |

#### Caption-Image Similarity

This measures how well the image matches a machine-generated **caption of the image**.

| Statistic | Value |
| :--- | :--- |
| **Mean** | 28.9341 |
| **Median** | 28.9688 |
| **Standard Deviation** | 3.5953 |
| **Minimum Score** | 15.7344 |
| **Maximum Score** | 40.2188 |

---

## 🚀 Setup and Usage

The analysis is contained within the `AI_Image_Prompt_Output_Match_Analysis.ipynb` Jupyter Notebook.

### Prerequisites

* **Execution Environment:** The notebook is optimized for a **Google Colaboratory** environment, ideally with **GPU acceleration** (e.g., T4 GPU) for fast model inference.
* **Data:** A dataset containing columns for the original **prompts** and either the generated **images** or a representative feature set derived from them.

### Dependencies

To run the notebook locally, you will need the following libraries (among others like `pandas` and `numpy`):

```bash
pip install transformers torch torchvision matplotlib
