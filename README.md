
---

# QR Code Generator

This Python script generates a QR code for a specified URL using the `qrcode` library. The QR code image is saved as a PNG file.

## Prerequisites

Ensure you have Python installed on your system. You will also need to install the `qrcode` library along with its `PIL` (Python Imaging Library) dependencies.

## Installation

To install the required library, use the following command:

```bash
pip install --user qrcode[pil]
```

## Usage

1. Clone or download this repository to your local machine.

2. Open a terminal or command prompt in the directory where the script is located.

3. Run the script using Python:

```bash
python generate_qr.py
```

This will generate a QR code image file named `tardis_project_qr.png` in the same directory.

## Script Details

The script contains the following main sections:

1. **Import the `qrcode` library**:
    ```python
    import qrcode
    ```

2. **Specify the URL to encode**:
    ```python
    url = "https://www.youtube.com"
    ```

3. **Create a QR code instance**:
    ```python
    qr = qrcode.QRCode(
        version=1,
        error_correction=qrcode.constants.ERROR_CORRECT_L,
        box_size=10,
        border=4,
    )
    ```

4. **Add the URL data to the QR code and generate the image**:
    ```python
    qr.add_data(url)
    qr.make(fit=True)
    img = qr.make_image(fill_color="black", back_color="white")
    ```

5. **Save the image to a file**:
    ```python
    img.save("YouTube_qr.png")
    ```

## License
