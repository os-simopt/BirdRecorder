# BirdRecorder Repository

## Public BirdRecorder Models and Algorithms

This repository contains various models and algorithms developed as part of the BirdRecorder project, aimed at facilitating bird monitoring and research. It includes state-of-the-art techniques for bird detection, classification, and recognition.

---

## Classification Birds CNN

The **Classification Birds CNN** project implements a Convolutional Neural Network (CNN) for bird image classification, with a particular focus on distinguishing the red kite from other classes. The project demonstrates:

- **Data Loading & Preprocessing:**  
  Loading training and validation data from `.npy` files, expanding grayscale images to include a channel, and normalizing pixel values.

- **Model Definition:**  
  Defining a CNN architecture using TensorFlow/Keras with optional support for distributed training (MultiWorker/MultiGPU).

- **Training with Data Augmentation:**  
  Utilizing `ImageDataGenerator` to augment data during training. The training loop supports dynamic learning rate adjustments, checkpointing, and live plotting of training progress.

- **Evaluation & Visualization:**  
  Evaluating the trained model on the validation set and displaying sample predictions with visual cues (e.g., colored borders indicating correct/incorrect classifications).

---

## Repository Structure

```
BirdRecorder/
├── classification_birds_cnn/
│   ├── birds_cnn.ipynb       # Main notebook/script for the CNN model
│   ├── data/                 # Directory containing .npy sample files
│   │   ├── bird_classification_train_data.npy
│   │   ├── bird_classification_train_targets.npy
│   │   ├── bird_classification_val_data.npy
│   │   └── bird_classification_val_targets.npy
│   ├── weights/              # Directory where model weights and full model are saved
│   └── README.md             # This README file
└── ...                       # Other BirdRecorder projects and scripts
```

---

## Requirements

- Python 3.7+
- TensorFlow 2.x
- NumPy
- Matplotlib
- IPython
- scikit-learn
- seaborn

It is recommended to use a virtual environment. Install the required dependencies using:

```bash
pip install -r requirements.txt
```


---

## Usage

1. **Data Preparation:**  
   Ensure that the sample `.npy` files are placed in the `data/` directory as specified.

2. **Run the Notebook/Script:**  
   Open and run the `birds_cnn.ipynb` notebook (or execute the corresponding `.py` script) to start training.  
   The script supports both single-GPU/CPU and distributed training (MultiWorker/MultiGPU).  
   Adjust training parameters and augmentation settings in the code as needed.

3. **Evaluation:**  
   After training, the model is evaluated on the validation set. Sample predictions are displayed with visual cues indicating correct and incorrect classifications.

---

## Reproducibility

For reproducibility, please refer to the provided `requirements.txt` file for dependency versions. Random seeds are set where applicable to ensure consistent results across runs.

---

## License

This project is licensed under the MIT License.

---

## Acknowledgments

The authors thank Ursula Amann, Kay Ohnmeiss, Amit Skanda, Frank Musiol, and Herbert Stark for discussions. They also acknowledge funding from the German Federal Agency for Nature Conservation (grant no. 3518 86 010B), support from the state of Baden-Württemberg through the project BirdRecorderValid (grant no. L75 32102), and funding from the German Federal Ministry for Economic Affairs and Climate Action (grant no. 03EE2047A).

---

## Author

**Nico Klar**  
Center for Solar Energy and Hydrogen Research (ZSW)  
Meitnerstraße 1, 70563 Stuttgart, Germany  
Email: [nico.klar@zsw-bw.de](mailto:nico.klar@zsw-bw.de)