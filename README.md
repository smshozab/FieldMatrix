# FieldMatrix
An Agriculture Research Project for precision farming based on Computer Vision CNN Algorithm. Our purpose is to train CNN U-NET model on our agricultural field dataset. It's currently in the process and soon we'll be at the final stages and onto deployment

# Plant Spacing Detection Using U-NET CNN

<h2>Introduction</h2>
Ensuring optimal plant spacing is crucial for maximizing crop yield and health. This project implements a U-NET Convolutional Neural Network (CNN) model to detect plant positions and evaluate spacing using image processing techniques. The goal is to automate the assessment of plant spacing to aid in precision agriculture.

<h2>Features</h2>
<ul>
<li>Automated detection of plants from aerial images.</li>
<li>Calculation of distances between detected plants.</li>
<li>Visualization of correctly and incorrectly spaced plants.</li>
<li>High accuracy and efficiency in plant detection and spacing analysis.</li>
</ul>

<h2>Installation</h2>
To get started with the project, follow these steps:

1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/plant-spacing-detection.git
    cd plant-spacing-detection
    ```

2. Create a virtual environment and activate it:
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

## Usage

1. **Prepare the Dataset:**
    - Place your training and validation images in the `data/train` and `data/val` directories, respectively.
    - Ensure your images are labeled appropriately for training the U-NET model.

2. **Train the Model:**
    ```bash
    python train.py --data_dir data/train --val_dir data/val --output_dir models
    ```

3. **Evaluate the Model:**
    ```bash
    python evaluate.py --model_path models/best_model.h5 --data_dir data/val
    ```

4. **Run Inference:**
    ```bash
    python inference.py --model_path models/best_model.h5 --input_dir data/test --output_dir results
    ```

## Model Architecture

The U-NET model architecture consists of an encoder-decoder structure with skip connections. It is specifically designed for image segmentation tasks. The encoder captures the context, while the decoder enables precise localization.
![2](https://github.com/user-attachments/assets/400d7636-f29c-4f53-b220-542e6df4d457)

Distance between plant 0 and plant 1: 181.90 meters

![image](https://github.com/user-attachments/assets/176896d6-6143-4783-a108-a49710ae828e)
