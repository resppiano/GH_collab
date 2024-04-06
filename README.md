# CODE BY GREG JONES

# Cancellation Rotation List

This Python program is designed to manage the rotation of therapists for cancellations. It includes functionality to update the list of therapists based on who is working on a given night, handle sick calls, requested cancellations, and import the current night's list of therapists from a JPEG image of a schedule using Optical Character Recognition (OCR).

## Features

- **Current Date Retrieval**: Fetches the current date in a readable format.
- **Cancellation Rotation Management**: Finds the next therapist to cancel who is actually working, adjusts the cancellation list for sick calls, and updates the cancellation list based on various conditions.
- **OCR Integration**: Extracts the list of working therapists from a JPEG image of a schedule using OCR technology.
- **Flexible Therapist Handling**: Can handle different numbers of therapists working on any given night.

## Installation

Before running the Cancellation Rotation List program, you need to install the following dependencies:

1. **Tesseract-OCR**: An open-source OCR engine. Installation instructions can be found on the [Tesseract GitHub page](https://github.com/tesseract-ocr/tesseract).

2. **Python Libraries**: The program requires Python 3 and the following Python libraries: `Pillow`, `pytesseract`, and `opencv-python`. You can install these using pip:

    ```bash
    pip install Pillow pytesseract opencv-python
    ```

## Configuration

After installing Tesseract-OCR, you may need to configure the path to the Tesseract executable in the program if it's not already in your system's PATH:

```python
pytesseract.pytesseract.tesseract_cmd = r'C:\path\to\tesseract.exe'

# Python code goes here


To import this Markdown document to GitHub, follow these steps:

1. Create a new repository or navigate to an existing one on GitHub.
2. Click on the 'Add file' button and select 'Create new file'.
3. Name the file "Cancellation Rotation List.md".
4. Copy and paste the Markdown content into the editor.
5. Scroll down, add a commit message, and commit the new file to the repository.

