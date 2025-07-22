
# Morse Blink Decoder

A Morse code decoder using eye blinks. This project combines real-time computer vision with deep learning to enable hands-free communication using eye blinks as input. It uses YOLOv8 for eye detection and a CNN model to classify eye states (open or closed).

## 🚀 Features

- Real-time eye detection using YOLOv8
- Eye state classification with a CNN (open vs closed)
- Morse code decoding based on blink patterns
- Fully interactive interface via Jupyter Notebook
- Hands-free input method useful for accessibility

## 📁 Project Structure

Vpo_Project/
├── best.pt # YOLOv8 model weights
├── eye_blink_cnn_model.h5 # CNN model for eye classification
├── eye_cnn_model.ipynb # Notebook for CNN training
├── main_morse_blink_app.ipynb # Main application
├── dlib-19.24.99-...whl # Dlib wheel for installation
├── shape_predictor_68_face_landmarks.dat # Dlib face landmarks
├── eye_data/ # Training dataset
└── .ipynb_checkpoints/

## 🛠️ Requirements

opencv-python
numpy
tensorflow
keras
ultralytics
dlib==19.24.0
matplotlib
scikit-learn

You can install the dependencies with:

```bash
pip install -r requirements.txt
```
(You may need to install dlib using the provided .whl file for compatibility.)

⚠️ YOLOv8 GPU Support:
This project was tested with YOLOv8 on Google Colab, which provides free GPU acceleration (NVIDIA Tesla T4).
If you're running locally, ensure your environment has CUDA-compatible GPU and drivers, or use Colab for best performance.
## How It Works
1. YOLOv8 detects the position of both eyes in real-time.

2. The CNN model classifies each eye as open or closed.

3. Blink durations are analyzed and converted into dots (.) and dashes (-).

4. The resulting Morse code is translated into human-readable text.

## Example Use
Run the notebook main_morse_blink_app.ipynb to start real-time detection and decoding.

## License
This project is licensed under the MIT License.

