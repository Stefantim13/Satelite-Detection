# 🛰️ Satellite Object Detection with YOLOv1-OBB

This project focuses on detecting objects in satellite images using a custom-trained YOLOv11 model with Oriented Bounding Boxes (OBB). The model has been fine-tuned on satellite imagery data and is capable of predicting both the location and orientation of detected objects.

## 🧾 Detected Classes

The model is trained to detect the following 15 object types commonly found in aerial or satellite imagery:

- `plane`
- `ship`
- `storage-tank`
- `baseball-diamond`
- `tennis-court`
- `basketball-court`
- `ground-track-field`
- `harbor`
- `bridge`
- `large-vehicle`
- `small-vehicle`
- `helicopter`
- `roundabout`
- `soccer-ball-field`
- `swimming-pool`

These are defined in your `names` list and matched to class indices in model outputs (via `box.cls` in inference).

---

## 🚀 Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/Satelite-Detection.git
   cd Satelite-Detection
   ```

2. Install required Python packages:
   ```bash
   pip install -r requirements.txt
   ```
   Or, for Jupyter Notebook:
   ```bash
   pip install ultralytics opencv-python matplotlib numpy
   ```

---

## 📦 Dataset Preparation

- Place your satellite images in `./dataset/images/train` and `./dataset/images/valid`.
- Place the corresponding label `.txt` files in `./dataset/labels_start/train` and `./dataset/labels_start/valid`.
- The notebook will convert and normalize the labels for YOLO OBB format.

---

## 🏃 Usage

Open `Main.ipynb` in Jupyter Notebook or VS Code and run the cells step by step:

1. **Label Conversion:** Converts raw labels to YOLO OBB format.
2. **Training:** Trains the YOLOv11-OBB model on your dataset.
3. **Testing:** Runs inference on a sample image and saves the result as `predicted_output.png`.

---

## 🖼️ Example Output

![Sample Prediction](predicted_output.png)

```
OBB 0: Center=(0.5, 0.5), Size=(0.1, 0.2), Angle=45.0, Confidence=0.98, Class=plane
...
```

---

## 📚 References

- [YOLOv1-OBB (Ultralytics)](https://github.com/ultralytics/ultralytics)
- [DOTA Dataset](https://captain-whu.github.io/DOTA/dataset.html)