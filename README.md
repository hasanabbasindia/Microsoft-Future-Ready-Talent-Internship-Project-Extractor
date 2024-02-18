# Text Extractor

## Features

- Extract text from images or documents using Azure AI Computer Vision.
- Translate extracted English text to multiple languages with the Azure AI Translator.
- Supports various image formats, including JPEG, PNG, and PDF.
- User-friendly interface for easy image upload and documents.
- Seamless integration with Streamlit for interactive usage.

## Project Details

- [Project Demo Link Here](https://textractor.azurewebsites.net/)
- [Project Video Tutorial Link](https://youtu.be/GcEk-7DMi3E) Added Later*

## Azure Services Used

&rarr;This project utilizes a total of **three Azure Technologies** which are 
- Azure AI Services | Computer Vision
- Azure AI Services | Translator
- Azure App Service

&rarr;Brief Description on the Services Used:
* **Azure AI Services**
  * **Azure AI Translator**: To provide translation services for the extracted text to multiple languages.
  * **Azure Computer Vision**: To perform optical character recognition(OCR) and extract text from images or documents.
* **Azure App Service**: To host the streamlit on Azure portal.

![Screenshot 2024-02-09 at 8 18 32 PM](https://github.com/mohammadabbas-blr/Microsoft-Future-Ready-Talent-Internship-Project-Text-Extractor/assets/150517265/6399d07c-04bb-4df2-90cd-3fb44ee5ec67)

---
### Azure AI Services | Computer Vision
- In this project, this service is employed to perform character extraction on images(PNG, JPEG). It can effortlessly extract text from the mentioned and even PDF files. With its robust capabilities, it's an essential component for extracting text from scanned documents or images and making it available for further processing within your application.
- It takes in any type of document or images written in English and is sent to the service to extract data from it
- Inside Computer Vision Studio under the Optical Character Recognition , the feature Extract Text from Image is used to do the work of getting any complicated written text from the different formates.
![Screenshot 2023-12-02 at 8 49 50 PM](https://github.com/hasanabbas-blr/Microsoft-Future-Ready-Talent-Internship-Project-Hasans-Extractor/assets/150517265/511ab307-65e0-43c3-8a31-8d3f3a60273a)


- The given image below is the example of an extracted text from a pdf file into a json format
![Screenshot 2023-12-02 at 8 53 25 PM](https://github.com/hasanabbas-blr/Microsoft-Future-Ready-Talent-Internship-Project-Hasans-Extractor/assets/150517265/0f83db4b-799a-4ea7-aa1c-e938387db076)


- After the text is extracted it sent one by one inside a for-loop to the Azure Translator API.
- Below given is the Azure postal under Computer Vision:
![Screenshot 2024-02-09 at 8 19 53 PM](https://github.com/mohammadabbas-blr/Microsoft-Future-Ready-Talent-Internship-Project-Text-Extractor/assets/150517265/31a54566-7668-45ab-b79d-48ddc52e48c7)
![Screenshot 2024-02-09 at 8 20 12 PM](https://github.com/mohammadabbas-blr/Microsoft-Future-Ready-Talent-Internship-Project-Text-Extractor/assets/150517265/34c29942-2620-436c-8dd2-79feaf5a87e5)

---
### Azure AI Services | Translator
- This Azure Service plays a crucial role in making the application multilingual and accessible to a global audience. This service is used to translate the extracted English text into multiple languages. It enables the application to break language barriers, providing seamless communication and understanding for users regardless of their language preferences. This feature is especially valuable in applications where content needs to be translated or localized, broadening the reach and impact of your project.

- In this the extracted text is sent and then each line-by-line is translated from English to any preferred language provided in the application.

- Below given image is an example of the translated English text into "Spanish" and like-wise the user can translated into any desired language from English to any language. This is the translated language from the previous previous example in a JSON format.
![Screenshot 2023-12-02 at 8 57 46 PM](https://github.com/hasanabbas-blr/Microsoft-Future-Ready-Talent-Internship-Project-Hasans-Extractor/assets/150517265/8d769f4b-75c6-447b-bd48-2a79ffce29e3)
- Below given is the Azure postal under Translator:

![Screenshot 2024-02-09 at 8 20 47 PM](https://github.com/mohammadabbas-blr/Microsoft-Future-Ready-Talent-Internship-Project-Text-Extractor/assets/150517265/0a07eeaa-5930-439e-aabf-82222c6fe89f)
![Screenshot 2024-02-09 at 8 20 59 PM](https://github.com/mohammadabbas-blr/Microsoft-Future-Ready-Talent-Internship-Project-Text-Extractor/assets/150517265/95dbb554-f71b-4499-86eb-f98215b9388f)

---
### Azure App Service
- Azure App Service serves as the hosting platform for the application's user interface. With this service, I can deploy my application in a convenient and scalable manner. It allows me to focus on the development of my application without the need to manage the underlying infrastructure. This simplifies the deployment process and ensures that the application is easily accessible to users via the Azure portal. Azure App Service provides a robust and reliable environment for your Streamlit-based application, making it available to a broad audience.

- The entire code related from extraction, translations to Streamlit(web-application) is pushed to the Github.
- After the code is pushed successfully, the github project URL is then given to the Azure App service and then the deployment starts automatically.
- Below is the deployment status of the website.
![Screenshot 2024-02-09 at 8 21 28 PM](https://github.com/mohammadabbas-blr/Microsoft-Future-Ready-Talent-Internship-Project-Text-Extractor/assets/150517265/99f8637a-18f5-415d-bf8e-cfc95786f897)

- Below given is the Azure postal under App Service:

![Screenshot 2024-02-09 at 8 22 37 PM](https://github.com/mohammadabbas-blr/Microsoft-Future-Ready-Talent-Internship-Project-Text-Extractor/assets/150517265/7ffa624d-05fc-4a69-86a9-69c82fb8165f)

---

## Python Package

The project uses the following Python libraries:

- `azure-cognitiveservices-vision-computervision`: Python SDK for Azure Computer Vision.
- `requests`: For making HTTP requests to the Azure Translator API.
- `streamlit`: For creating the user interface and interactive web app.
- `opencv-python`: For capturing and processing images from the webcam.
- `#created/requirements.txt`

## Usage

1. Clone the repository:

```bash
git clone https://github.com/yourusername/your-repo.git
cd your-repo
```

2. Install the required dependencies:

```bash
pip install -r requirements.txt
```

3. Run the Streamlit app:

```bash
streamlit run main_script.py
```
---

## Steps to Use
- First  we select any image or PDF to upload by clicking on the **Browse files** button.
![Screenshot 2024-02-09 at 8 27 54 PM](https://github.com/mohammadabbas-blr/Microsoft-Future-Ready-Talent-Internship-Project-Text-Extractor/assets/150517265/5f1e877c-0c03-42be-8270-24d64b433250)
---
- After the the file is selected then the **Azure AI Computer Vision** processes and then a extracted text is displayed below.
![sample_azure](https://github.com/mohammadabbas-blr/Microsoft-Future-Ready-Talent-Internship-Project-Text-Extractor/assets/150517265/7a3f56c9-ecc8-4924-b31f-9c97cdd5bd46)
---
- **This is the extracted text from the above image:**
![Screenshot 2024-02-09 at 8 28 16 PM](https://github.com/mohammadabbas-blr/Microsoft-Future-Ready-Talent-Internship-Project-Text-Extractor/assets/150517265/011db0a9-765d-4747-bcf6-2d28fbfd9904)
---
- Then we go down and select the preferred language you want to translate.
- Once that is selected the **Azure AI Translator API** translates and displays the text below.
- **In this example I have chosen Hindi and Arabic:**
![Screenshot 2024-02-09 at 8 28 50 PM](https://github.com/mohammadabbas-blr/Microsoft-Future-Ready-Talent-Internship-Project-Text-Extractor/assets/150517265/14b258ab-57d7-454c-849a-4c7e59b65e23)
![Screenshot 2024-02-09 at 8 29 45 PM](https://github.com/mohammadabbas-blr/Microsoft-Future-Ready-Talent-Internship-Project-Text-Extractor/assets/150517265/490ca7d9-4e76-4c05-b91b-16b4bafdcb11)


---


## Screenshots

![Screenshot 2024-02-09 at 8 30 10 PM](https://github.com/mohammadabbas-blr/Microsoft-Future-Ready-Talent-Internship-Project-Text-Extractor/assets/150517265/3e55a9e1-6c70-45e8-8f58-ca024fb443c0)

![Screenshot 2024-02-09 at 8 44 24 PM](https://github.com/mohammadabbas-blr/Microsoft-Future-Ready-Talent-Internship-Project-Text-Extractor/assets/150517265/ab32cace-3ac9-4aae-8efe-cc37688b597a)





## **Account IDs**
**Git Hub ID:** mohammadabbas-blr

**Azure Account ID:** hasanabbasofficial2@gmail.com

## **Acknowledgements**
My sincere thanks, to Microsoft for an impressive static web apps service on MS Azure Cloud to deploy my website easily. It was a wonderful experience learning this and would like to explore more in next years of my B.Tech. Sincere appreciation to Team of Future Ready Talent who supported and encouraged us to work on this project. 
