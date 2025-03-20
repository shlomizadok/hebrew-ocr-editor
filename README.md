# Hebrew OCR Editor

A web-based OCR application specifically designed for Hebrew text extraction from images. The application allows users to select specific areas of text, perform OCR, edit the extracted text, and save it as a DOCX file.

## Features

- 📷 Image upload and display
- 🔍 Interactive area selection for text extraction
- 🔤 Hebrew text OCR using Tesseract
- ✏️ Real-time text editing
- 💾 Export to DOCX with RTL support
- 🖼️ Image preprocessing for better OCR results

## Prerequisites

- Python 3.8+
- Tesseract OCR
- Hebrew language data for Tesseract

### Installing Tesseract

#### macOS
```bash
brew install tesseract
brew install tesseract-lang
```

#### Ubuntu/Debian
```bash
sudo apt-get update
sudo apt-get install tesseract-ocr
sudo apt-get install tesseract-ocr-heb
```

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/hebrew-ocr-editor.git
cd hebrew-ocr-editor
```

2. Create a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Set up Tesseract data path:
```bash
# On macOS (when installed via Homebrew)
export TESSDATA_PREFIX=/opt/homebrew/share/tessdata/

# On Linux
export TESSDATA_PREFIX=/usr/share/tesseract-ocr/4.00/tessdata/
```

## Usage

1. Start the application:
```bash
python app.py
```

2. Open your browser and navigate to `http://localhost:5000`

3. Upload an image containing Hebrew text

4. Click and drag to select the area containing text

5. Click "Process Selected Area" to perform OCR

6. Edit the extracted text if needed

7. Click "Save as DOCX" to download the result

## Deployment

The application can be deployed to various platforms:

### Heroku
```bash
heroku create your-app-name
heroku buildpacks:add https://github.com/heroku/heroku-buildpack-apt
git push heroku main
```

### Other Platforms
See deployment documentation for Railway.app or Google Cloud Run in the docs folder.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

### Areas for Improvement

- [ ] Support for Rashi script recognition
- [ ] Multiple area selection
- [ ] Additional export formats
- [ ] Improved image preprocessing options
- [ ] Batch processing capabilities

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Tesseract OCR team for their amazing OCR engine
- Flask team for the web framework
- All contributors and users of this project 