Deep Learning Model Training with PyTorch and TensorFlow

This repository contains implementations of two separate deep learning pipelines, chosen to demonstrate practical applications of deep learning frameworks in different scenarios: a multi-class image classification task using PyTorch and a binary classification task using TensorFlow. These pipelines showcase complementary approaches, highlighting versatility in tackling real-world problems.

---

 PyTorch Implementation: CIFAR-10 Classification

 Features
- Data Augmentation using `torchvision.transforms` (includes random horizontal flips, rotations, resized cropping, color jitter, and normalization) to enhance model generalization.
- Custom Convolutional Neural Network (CNN) architecture.
- Early Stopping and Learning Rate Scheduling.
- Training and Validation Loss Visualization.
- Model Evaluation with Metrics like Precision, Recall, and F1-Score.

 Requirements
- Python 3.7+
- PyTorch
- torchvision
- tqdm
- matplotlib
- scikit-learn

 How to Run
1. Install the required libraries:

   Note: If you encounter issues during installation, ensure your Python version is compatible with the listed libraries. For example, use a virtual environment to manage dependencies and prevent conflicts.
   
   `pip install torch torchvision scikit-learn matplotlib tqdm`
   
2. Run the training script:
   
   `python cifar10_pytorch.py`
   
3. View the results and learning curves generated during training.

---

 TensorFlow Implementation: Cats vs Dogs Classification

 Features
- Preprocessing and filtering of corrupted images.
- Use of MobileNetV2 as a pretrained feature extractor.
- Fine-tuning with frozen and trainable layers.
- Binary classification with data augmentation.

 Requirements
- Python 3.7+
- TensorFlow
- tensorflow-datasets

 How to Run
1. Install the required libraries:
   
   pip install tensorflow tensorflow-datasets
   
2. Run the training script:
   
   `python cats_vs_dogs_tensorflow.py`
   
3. The script will train and evaluate the model, displaying metrics like accuracy.

---

 Key Concepts
 PyTorch
- Early Stopping: Stops training when the validation loss stops improving.
- Custom CNN: Designed from scratch for the CIFAR-10 dataset.

 TensorFlow
- Transfer Learning: Leveraging MobileNetV2's pretrained weights for binary classification.
- Fine-Tuning: Training some layers of the base model for improved performance.

---

 Results
 PyTorch Model:
- Achieved classification metrics (Precision, Recall, F1-Score) per class on the CIFAR-10 dataset.

 TensorFlow Model:
- Trained a binary classifier for Cats vs Dogs achieving high accuracy on the validation set.

---

 Future Improvements
- Add support for additional datasets, such as MNIST, Fashion-MNIST, or ImageNet, to broaden the applicability of the models.
- Incorporate tasks like semantic segmentation or object detection for a more comprehensive exploration of deep learning capabilities.
- Explore different model architectures and hyperparameter tuning.
- Extend TensorFlow implementation for multi-class classification tasks.

---

License:
This repository is licensed under the MIT License. For more details, see the (https://opensource.org/licenses/MIT). Feel free to use and modify the code.
