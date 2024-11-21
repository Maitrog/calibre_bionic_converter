# Calibre Bionic Converter

This script scans your Calibre library for eBooks, allows you to select which books to convert, and applies Bionic Reading typography to the selected books. The Bionic Reading conversion is handled by a script from the repository [arcanite24/libre-bioread](https://github.com/arcanite24/libre-bioread). Ensure that the `apply_bioread.py` script is downloaded and placed in the same directory as this script.

---

## Features
1. Scans your Calibre library to find all supported eBook formats (e.g., `.epub`, `.mobi`, `.pdf`, etc.).
2. Interactively prompts you to select which books to convert.
3. Applies Bionic Reading typography to the selected books using the `apply_bioread.py` script.
4. Provides a visual loading spinner during the conversion process.

---

## Prerequisites

1. **Python 3.8 or higher** installed on your system.
2. **Dependencies**: Install required Python libraries using:
   ```bash
   pip install python-dotenv
3. Calibre Library Path: Ensure your .env file includes the following:
   ```lua
   CALIBRE_LIBRARY_PATH=C:\path\to\your\calibre\library
Replace the path with the actual location of your Calibre library.
4. Bionic Reading Script: Download the Bionic Reading script apply_bioread.py from (arcanite24/libre-bioread)[https://github.com/arcanite24/libre-bioread] and place it in the same directory as this script.

## Usage

1. **Prepare Your Environment**:
   - Ensure Python 3.8 or higher is installed on your system.
   - Set your Calibre library path in a `.env` file with the following format:
     ```
     CALIBRE_LIBRARY_PATH=C:\path\to\your\calibre\library
     ```
     Replace the path with the actual location of your Calibre library.
   - Download the `apply_bioread.py` script from [arcanite24/libre-bioread](https://github.com/arcanite24/libre-bioread) and place it in the same directory as this script.

2. **Run the Script**:
   Execute the script using:
   ```bash
   python main.py
3. Follow the prompts: 
    - The script will scan your Calibre library for eBooks and display a count of the files found.
    - For each book, it will ask:
   ```sql
   Would you like to convert 'example_book.epub'? (y/n):
 Select y to convert or n to skip.
 4. Conversion: 
    -The selected books will be processed, and you’ll see a loading spinner during the conversion process. Once completed, a message will confirm the conversion.

### Supported Formats
By default, the script supports the following eBook formats:.epub, .mobi, .pdf, .azw3, .fb2

You can customize this list in the find_ebooks_in_calibre_library function by modifying the supported_formats parameter.

## Credits

This script integrates the Bionic Reading conversion functionality from [arcanite24/libre-bioread](https://github.com/arcanite24/libre-bioread). Full credit for the Bionic Reading typography application goes to the original author of that repository.