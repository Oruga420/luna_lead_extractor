Luna Lead Extractor
Luna Lead Extractor is a Flask-based web application that automates the extraction of lead data from images using OpenAI's GPT model. The app processes images (e.g., PNG, JPG, JPEG, GIF), extracts relevant lead information such as company name, email, name, phone number, etc., and saves the extracted information into a CSV file for further use.

Features
Image Upload: Upload multiple images for processing.
AI-Powered Data Extraction: Uses OpenAI's GPT model to extract structured lead information from the images.
CSV Export: Automatically saves extracted information into a CSV file.
Error Handling: Provides clear error messages and logs issues during the upload and processing stages.
Requirements
To run the Luna Lead Extractor, you need the following:

Python 3.x
Flask
Pillow
OpenAI API credentials
You can install the dependencies with:

bash
Copy code
pip install -r requirements.txt
Installation
Clone the repository:

bash
Copy code
git clone https://github.com/Oruga420/luna_lead_extractor.git
cd luna_lead_extractor
Install the required Python libraries:

bash
Copy code
pip install -r requirements.txt
Set your OpenAI API key as an environment variable:

bash
Copy code
export OPENAI_API_KEY='your-api-key'
Run the Flask app:

bash
Copy code
python app.py
Access the app via your browser at http://localhost:5000.

Usage
Uploading Images:
Navigate to the upload page.
Select multiple images (PNG, JPG, JPEG, or GIF) for processing.
Processing:
The app will process each image, extract relevant lead information such as:
Company Name
Email
Name
Last Name
Phone
Extra Info
Download CSV:
Once processed, you can download the extracted data in a CSV format.
Configuration
The config.json file is not required. The application uses a web interface where you upload images directly, and extraction is performed based on hardcoded logic.

Code Overview
app.py: The main Flask application file that handles file uploads, image processing, and downloading the extracted data.
image_processor.py: Handles image resizing and extraction of information from images using the extract_info_from_image function.
openai_handler.py: Interacts with the OpenAI API to extract specific fields (Company Name, Email, Name, etc.) from the images.
requirements.txt: Lists the dependencies required for the project.
Example Output
After uploading and processing images, the extracted lead information will be saved to a CSV file, which may look like this:

Company Name	Email	Name	Last Name	Phone	Extra Info
Example Corp	john@example.com	John	Doe	123-456-7890	Sales Lead
Another Co	jane@another.com	Jane	Smith	987-654-3210	Key Contact
Error Handling
The application handles errors such as:

Invalid file types.
API errors from OpenAI.
File size limits exceeding 16MB.
General server errors are logged and returned as JSON responses.
Contributing
Feel free to fork the repository and submit pull requests for new features or bug fixes.

License
This project is licensed under the MIT License. See the LICENSE file for details.
