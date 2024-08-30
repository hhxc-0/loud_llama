# loud_llama

loud_llama is an AI voice assistant that utilizes Whisper for speech recognition, Ollama for large language model (LLM) capabilities, and XTTS for text-to-speech functionality.

## Table of Contents
- [Setup](#setup)
- [Usage](#usage)

## Setup

Follow these steps to set up the project:

1. **Install Python** (version 3.11.x is recommended):  
   Download from the official website: [Python Downloads](https://www.python.org/downloads/)

2. **Download the Project**:  
   You can either clone the repository or download it as a ZIP file:
   - Clone with Git:
     ```bash
     git clone https://github.com/GongXiPing/loud_llama.git
     ```
   - Or download as a ZIP:  
     Go to **Code > Download ZIP** on the GitHub page.

3. **Install Required Packages**:  
   Navigate to the project directory and install the necessary packages using pip:
   ```bash
   pip install -r requirements.txt
   ```

4. **Install PyTorch**:  
   Download and install a suitable version of PyTorch for your system. Visit the [PyTorch website](https://pytorch.org/get-started/locally/) and follow the instructions to select the appropriate configuration (OS, package manager, Python version, and CUDA version). For example, a typical command for installing PyTorch might look like this:
   ```bash
   pip install torch torchvision torchaudio --extra-index-url https://download.pytorch.org/whl/cu113
   ```

5. **Install Whisper for Speech Recognition**:  
   You can install Whisper either as a package or as an individual model:
   - **Install as a Package (Recommended for Beginners)**:
     1. Install using pip:
        ```bash
        pip install openai-whisper
        ```
     2. Set `using_as_package=True` in the **Initialization and Parameters** section of your code.
     3. Choose a `model_name`:
        - For English only: 
          ```python
          model_name = "small.en"
          ```
        - For multilingual support: 
          ```python
          model_name = "small"
          ```
        - Consider using larger models for improved transcription quality.
   - **Install as an Individual Model**:
     1. Download a model from the [Whisper series on Hugging Face](https://huggingface.co/models?other=whisper).
     2. Set the `model_path` to your model directory (absolute path is recommended):
        ```python
        model_path = "path/to/your/model/whisper-small.en/"
        ```

6. **Install Ollama for LLM Service**:  
   Follow the instructions on the [Ollama GitHub page](https://github.com/ollama/ollama).

## Usage

To use loud_llama:

1. **Start the Ollama Service**:
   - Open a terminal and run the following command to start the Ollama service:
     ```bash
     ollama serve
     ```

2. **Start the Assistant**:
   - If you have an IDE that supports **.ipynb** files, open **assistant.ipynb** and run all the cells.
   - Alternatively, you can run it in the command line:
     ```bash
     ipython assistant.ipynb
     ```

3. **Interact with the Assistant**:
   - Speak into the microphone when **"Recording..."** is displayed.
   - Wait for the assistant's vocal response.
   - To pause the conversation, simply stop speaking. 
   - Press Enter to resume the conversation, type 'new' to start a new thread, or type 'bye' to exit.

## Compatibility

Please note that loud_llama has currently only been tested on Windows and Python 3.11.9.

## Issues

If you encounter any problems while using the program, please feel free to [post an issue](https://github.com/GongXiPing/loud_llama/issues) in the GitHub repository, and we will do our best to assist you.
