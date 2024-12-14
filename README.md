# Image Text Extraction Using OpenAI GPT-4

This Python script extracts text from images using OpenAI's GPT-4 API. The script supports both image URLs and base64-encoded images as inputs. Extracted text can be saved to a local file for further use.

---

## Features

- **Text Extraction from Image URLs:** Extract text directly from an image available online.
- **Text Extraction from Base64 Images:** Extract text from locally stored images by converting them into base64 encoding.
- **Accurate Text Parsing:** Ensures completeness by carefully extracting all text elements, including faint or small text, and preserving the original structure.
- **Output to File:** Saves extracted text to a specified file.

---

## Requirements

- Python 3.7+
- OpenAI Python SDK
- Base64 library (standard library)

---

## Installation

1. Clone this repository or download the script.
2. Install the required dependencies:
   ```bash
   pip install openai
   ```
3. Ensure you have an OpenAI API key.

---

## Usage

### Extracting Text from an Image URL

1. Uncomment the relevant section in the script:
   ```python
   # image_url = "https://example.com/image.jpg"
   # extracted_text = image_to_text_from_url(image_url)
   # output_file_path = "path/to/extracted_text.txt"
   # with open(output_file_path, "a", encoding="utf-8") as text_file:
   #     text_file.write(extracted_text)
   #     text_file.write("\n")
   ```
2. Replace the `image_url` with the URL of your image.
3. Run the script and view the extracted text in the specified file.

### Extracting Text from a Local Image

1. Provide the path to your local image:
   ```python
   local_image_path = "path/to/image.png"
   ```
2. The script will automatically convert the image to base64 encoding and extract text.
3. View the extracted text in the console or in the specified output file.

---

## Code Structure

### Functions

1. **`image_to_base64(image_path)`**
   - Converts a local image to base64 encoding.

2. **`image_to_text_from_url(image_url)`**
   - Extracts text from an image using its URL.

3. **`image_to_text_from_base64(image_base64)`**
   - Extracts text from an image provided in base64 format.

### Example Workflow

- **Input:** Image URL or local image file.
- **Process:**
  - For URLs: Direct API call.
  - For local files: Convert to base64, then API call.
- **Output:** Extracted text saved to a file.

---

## Configuration

- Update your OpenAI API key in the `client` initialization:
  ```python
  client = OpenAI(
      api_key="your-openai-api-key"
  )
  ```
- Specify the file path for saving the extracted text.

---

## Limitations

- The script requires an active OpenAI API key with appropriate permissions.
- Limited by the capabilities of the GPT-4 model for OCR tasks.

---

## Contributing

Feel free to fork this repository and submit pull requests for new features or improvements.

---

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
