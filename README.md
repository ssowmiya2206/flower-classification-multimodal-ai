# 🌸 Multimodal Flower Classification & Sentiment Analysis

A deep learning project that combines **Computer Vision** and **Natural Language Processing** into a single multimodal AI pipeline — capable of identifying flower species from images *and* analyzing user reviews for sentiment.

---

## 🚀 Demo

| Input Image | Review Text | AI Output |
|---|---|---|
| 🌻 Sunflower photo | "This sunflower is so beautiful and bright!" | **Sunflowers (93.4%) — Positive 😊 — Highly Recommended ⭐** |

---

## 🧠 What It Does

1. **Image Classification** — Identifies the flower species from a photo
2. **Sentiment Analysis** — Determines if a text review is Positive or Negative
3. **Multimodal Pipeline** — Combines both models for a unified recommendation output

---

## 📊 Results

| Model | Train Accuracy | Validation Accuracy |
|---|---|---|
| Basic CNN (from scratch) | 97% | 68% ❌ |
| CNN + Dropout | 96% | 63% ❌ |
| **MobileNetV2 (Transfer Learning)** | **93%** | **88% ✅** |

---

## 🌼 Flower Classes

The model classifies 5 flower species from 3,670 images:

- 🌹 Roses (641 images)
- 🌻 Sunflowers (699 images)
- 🌷 Tulips (799 images)
- 🌼 Daisies (633 images)
- 🌾 Dandelions (898 images)

---

## 🛠️ Tech Stack

| Category | Tools |
|---|---|
| Language | Python 3 |
| Deep Learning | TensorFlow, Keras |
| Pretrained Model | MobileNetV2 (ImageNet weights) |
| NLP | Scikit-learn, TF-IDF, Logistic Regression |
| Visualization | Matplotlib |
| Environment | Google Colab / Kaggle Notebooks |

---

## 📁 Project Structure

```
flower-classification-multimodal-ai/
│
├── notebook.ipynb          # Main Colab notebook (full pipeline)
├── sunflower.jpg           # Sample test image
└── README.md               # Project documentation
```

---

## ⚙️ How to Run

### 1. Open in Google Colab
Click the badge below or open `notebook.ipynb` directly in [Google Colab](https://colab.research.google.com/).

### 2. Download the dataset
The dataset is loaded automatically from TensorFlow's public servers:
```python
dataset_url = "https://storage.googleapis.com/download.tensorflow.org/example_images/flower_photos.tgz"
data_dir = tf.keras.utils.get_file('flower_photos', origin=dataset_url, untar=True)
```

### 3. Run all cells
Execute each cell in order. Training takes ~5 minutes on a T4 GPU.

### 4. Test with your own image
Upload any flower photo when prompted and the pipeline will return:
- Predicted flower species + confidence
- Sentiment of your review
- Final recommendation

---

## 🔍 Key Concepts Demonstrated

- **Convolutional Neural Networks (CNN)** — Extracting visual features from images
- **Transfer Learning** — Reusing MobileNetV2 pretrained on 1M+ ImageNet images
- **Overfitting & Dropout** — Diagnosing and fixing model generalization issues
- **TF-IDF Vectorization** — Converting text into numerical features
- **Multimodal AI** — Fusing vision and language models into one pipeline

---

## 📈 Training Progress (MobileNetV2)

```
Epoch  1  →  val_accuracy: 83%
Epoch  6  →  val_accuracy: 89%
Epoch 10  →  val_accuracy: 88%
```

---

## 🙋 Author

Built as part of an AI/ML learning journey.  
Feel free to fork, star ⭐, or raise issues!

---

## 📄 License

This project is open source under the [MIT License](LICENSE).
