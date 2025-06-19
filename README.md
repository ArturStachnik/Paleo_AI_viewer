# Paleo AI Residual Viewer

**Paleo AI Viewer** is a Jupyter Notebook that loads Holocene paleotemperature data, applies an ensemble of trained neural networks, and visualizes the results as an interactive scatter plot comparing predicted and true temperature values.

The viewer includes a dropdown menu to color-code the data points by season, proxy type, or archive type, enabling intuitive exploration of the model's predictions.

---

## 🔗 Open in Google Colab

> If you're viewing this on GitHub, you can launch the notebook directly in Google Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ArturStachnik/Paleo_AI_viewer/blob/main/Paleo_AI_Viewer.ipynb)

---

## 📂 Repository Structure

Paleo_AI_Viewer.ipynb # Main notebook (for Colab)
Holocene_T_clean.csv # Input dataset
models/
├── model_0.pt # Trained model weights
├── model_1.pt
└── scaler.pkl # Scikit-learn scaler

---

## ⚙️ How to Use

### Option 1: Run in Google Colab (Recommended)

1. Click the "Open in Colab" badge above.
2. Execute all cells in order.
3. The notebook will:
   - Clone this repository
   - Load the dataset and models
   - Generate the interactive scatter plot

> **Note**: If you open the notebook directly from Colab, cloning the repo will still fetch the models and data automatically.

---

## 📈 Output: Residuals Interactive Plot

The final cell generates a scatter plot of predicted vs. true temperatures, including:

- A diagonal reference line for perfect prediction (y = x)
- Color dropdown to group points by:
  - Season (`annual`, `warm`, `cold`)
  - Proxy type
  - Archive type

---

## 💡 Customization Tips

To adjust the appearance of the graph, modify this section inside the notebook:

```python
fig.update_layout(
    yaxis_scaleanchor="x",
    height=1000,
    width=2000,
    ...
)
