# CODE BY GREG JONES


# Cancellation Rotation List

The Cancellation Rotation List is a Python program designed to manage the rotation of therapists for cancellations. It includes functionality to update the list of therapists based on who is working on a given night, handle sick calls, requested cancellations, and import the current night's list of therapists from a JPEG image of an Excel-formatted schedule using Optical Character Recognition (OCR).

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
```

Replace `C:\path\to\tesseract.exe` with the actual path to your Tesseract installation.

## Usage

To use the Cancellation Rotation List program, simply run the script in your terminal or command prompt. If the program requires the list of therapists working on the current night, you will be prompted to provide the path to the JPEG image of the schedule.

The program will then perform OCR on the image to extract the list of working therapists and proceed with the cancellation rotation logic based on the extracted list and any special cases (e.g., sick calls or requested cancellations).

## Functions

### `get_current_date()`

Returns the current date in a readable format (`YYYY-MM-DD`).

### `find_next_to_cancel(working_therapists, therapists)`

Finds the next therapist to cancel who is actually working.

### `adjust_for_sick_call(sick_therapist, therapists)`

Adjusts the cancellation list to account for a therapist calling out sick.

### `update_cancellation_list(working_therapists, therapists, sick_therapist=None, requested_cancellation=None)`

Updates the cancellation list based on who is working, handles sick calls, and requested cancellations.

### `extract_text_from_image(image_path)`

Extracts text from an image file using OCR. This function is used to import the list of therapists working on the current night from a JPEG image of a schedule.

## Contributing

Contributions to the Cancellation Rotation List program are welcome. Please feel free to fork the repository, make changes, and submit pull requests.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
