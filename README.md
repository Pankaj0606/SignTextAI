# Sign-Language-to-Text Project Documentation
## Project Overview
### Purpose
This project aims to convert American Sign Language (ASL) gestures captured via webcam into text in real-time. It leverages Convolutional Neural Networks (CNNs) trained on a custom-made dataset of ASL signs.
### Key Features
*   **Real-time Translation:** Converts ASL gestures to text as the user signs in front of a webcam.
*   **CNN-based Model:** Employs a CNN model for accurate sign recognition.
*   **Custom Dataset:** Trained on a dataset specifically created for this project.
*   **GUI Interface:** Provides a user-friendly graphical interface using Tkinter.
*   **Layered Prediction:** Uses multiple models for specific letters to improve accuracy.
### Supported Platforms/Requirements
*   **Operating System:**  Tested on macOS, but should be compatible with other operating systems (Windows, Linux) with appropriate dependencies installed.
*   **Python:** Python 3.6 or higher.
*   **Webcam:** A functional webcam is required for capturing video input.
*   **Dependencies:** See the "Getting Started" section for a list of required Python packages.
## Getting Started
### Installation/Setup Instructions
1.  **Clone the Repository:**
    ```bash
    git clone <repository_url>
    cd Sign-Language-to-Text
    ```
    
2.  **Create a Virtual Environment (Recommended):**
    ```bash
    python3 -m venv venv
    source venv/bin/activate  # On Linux/macOS
    venv\Scripts\activate  # On Windows
    ```
    
3.  **Install Dependencies:**
    *   **Using pip:**
        ```bash
        pip install -r requirements_pip.txt
        ```
        
    *   **Using conda:**
        ```bash
        conda create --name <env_name> --file requiremnets_conda.txt
        conda activate <env_name>
        ```
        Replace `<env_name>` with your desired environment name.
4.  **Download Model Weights:**
    *   Ensure the `model` directory exists.
    *   Place the following files in the `model` directory:
        *   `model-bw.json`
        *   `model-bw.h5`
        *   `model-bw_dru.json`
        *   `model-bw_dru.h5`
        *   `model-bw_smn.json`
        *   `model-bw_smn.h5`
        *   `model-bw_tkdi.json`
        *   `model-bw_tkdi.h5`
    *Note: These model files are not included in the repository due to size constraints. You will need to obtain them separately.*
5.  **Run the Application:**
    ```bash
    python app.py
    ```
    
### Dependencies/Prerequisites
The project relies on the following Python packages:
*   absl-py
*   Pillow
*   opencv-python
*   Keras
*   tensorflow (or tensorflow-gpu)
*   numpy
*   matplotlib
*   scikit-learn
*   pandas
*   hunspell (optional, for word suggestions)
*   tkinter (usually included with Python installations)
A complete list of dependencies can be found in `requirements_pip.txt` and `requiremnets_conda.txt`.
## Code Structure
The project's code is organized as follows:
*   `.gitignore`: Specifies intentionally untracked files that Git should ignore.
*   `app.py`: Contains the main application logic, including the GUI and real-time sign language translation.
*   `collect-data.py`: Script for collecting image data for training the CNN model.
*   `image_processing.py`: Contains image processing functions used for preprocessing images before prediction.
*   `LICENSE`: Contains the licensing information for the project.
*   `preprocessing.py`: Script for preprocessing the collected image data.
*   `README.md`: This documentation file.
*   `requirements_pip.txt`: Lists the Python dependencies required for the project (pip).
*   `requiremnets_conda.txt`: Lists the Python dependencies required for the project (conda).
*   `train.py`: Script for training the CNN model.
*   `data/`: Directory containing the training and testing datasets.
*   `data2/`: Directory containing the preprocessed training and testing datasets.
*   `model/`: Directory containing the saved CNN model (`model-bw.json` and `model-bw.h5`) and layered models.
*   `Pictures/`: Directory containing images for the "About" section in the GUI.
## API Documentation
This project does not expose a public API. It is a standalone application designed to be run locally.
