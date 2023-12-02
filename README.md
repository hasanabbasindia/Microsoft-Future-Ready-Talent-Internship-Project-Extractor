# Hasan's Extractor

##Note: Changing bg color now.

## Features

- Extract text from images or documents using Azure AI Computer Vision.
- Translate extracted English text to multiple languages with the Azure AI Translator.
- Supports various image formats, including JPEG, PNG, and PDF.
- User-friendly interface for easy image upload and documents.
- Seamless integration with Streamlit for interactive usage.

## Project Details

- [Project Demo Link Here](https://hasansextractor.azurewebsites.net/)
- [Project Video Tutorial Link](https://youtu.be/HulJI52bx5Q)

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

![Screenshot 2023-12-02 at 8 41 50 PM](https://github.com/hasanabbas-blr/Microsoft-Future-Ready-Talent-Internship-Project-Hasans-Extractor/assets/150517265/65b6a8d6-b819-4bcc-9624-768bc9d5078f)
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
![Screenshot 2023-12-02 at 8 55 53 PM](https://github.com/hasanabbas-blr/Microsoft-Future-Ready-Talent-Internship-Project-Hasans-Extractor/assets/150517265/3d4d905a-673e-4b89-91d3-99b4658f3b73)
![Screenshot 2023-12-02 at 8 41 59 PM](https://github.com/hasanabbas-blr/Microsoft-Future-Ready-Talent-Internship-Project-Hasans-Extractor/assets/150517265/de791cad-f301-43da-aebe-5ee76901f8ff)

---
### Azure AI Services | Translator
- This Azure Service plays a crucial role in making the application multilingual and accessible to a global audience. This service is used to translate the extracted English text into multiple languages. It enables the application to break language barriers, providing seamless communication and understanding for users regardless of their language preferences. This feature is especially valuable in applications where content needs to be translated or localized, broadening the reach and impact of your project.

- In this the extracted text is sent and then each line-by-line is translated from English to any preferred language provided in the application.

- Below given image is an example of the translated English text into "Spanish" and like-wise the user can translated into any desired language from English to any language. This is the translated language from the previous previous example in a JSON format.
![Screenshot 2023-12-02 at 8 57 46 PM](https://github.com/hasanabbas-blr/Microsoft-Future-Ready-Talent-Internship-Project-Hasans-Extractor/assets/150517265/8d769f4b-75c6-447b-bd48-2a79ffce29e3)
- Below given is the Azure postal under Translator:

![Screenshot 2023-12-02 at 8 59 09 PM](https://github.com/hasanabbas-blr/Microsoft-Future-Ready-Talent-Internship-Project-Hasans-Extractor/assets/150517265/c92f1d9a-c6b0-4640-a207-3c7eddece96b)
![Screenshot 2023-12-02 at 8 42 13 PM](https://github.com/hasanabbas-blr/Microsoft-Future-Ready-Talent-Internship-Project-Hasans-Extractor/assets/150517265/05550de1-e9d9-4827-8e1f-b055382f2e01)

---
### Azure App Service
- Azure App Service serves as the hosting platform for the application's user interface. With this service, I can deploy my application in a convenient and scalable manner. It allows me to focus on the development of my application without the need to manage the underlying infrastructure. This simplifies the deployment process and ensures that the application is easily accessible to users via the Azure portal. Azure App Service provides a robust and reliable environment for your Streamlit-based application, making it available to a broad audience.

- The entire code related from extraction, translations to Streamlit(web-application) is pushed to the Github.
- After the code is pushed successfully, the github project URL is then given to the Azure App service and then the deployment starts automatically.
- Below is the deployment status of the website.
![Screenshot 2023-12-02 at 5 09 42 PM](https://github.com/hasanabbas-blr/Microsoft-Future-Ready-Talent-Internship-Project-Hasans-Extractor/assets/150517265/553345b4-4841-472e-aa88-4a58db01f9ce)
- Below given is the Azure postal under App Service:

![Screenshot 2023-12-02 at 9 03 15 PM](https://github.com/hasanabbas-blr/Microsoft-Future-Ready-Talent-Internship-Project-Hasans-Extractor/assets/150517265/031b3223-6bd8-4bee-a6cb-d1e89b76dcd1)
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
![Screenshot 2023-12-02 at 9 04 43 PM](https://github.com/hasanabbas-blr/Microsoft-Future-Ready-Talent-Internship-Project-Hasans-Extractor/assets/150517265/1ba0718b-2283-413c-a244-e87a05631ff1)
---
- After the the file is selected then the **Azure AI Computer Vision** processes and then a extracted text is displayed below.
![sample_azure](https://github.com/hasanabbas-blr/Microsoft-Future-Ready-Talent-Internship-Project-Hasans-Extractor/assets/150517265/c6174bbd-dfe1-4ddc-b449-ac96ce43e858)
---
- **This is the extracted text from the above image:**
![Screenshot 2023-12-02 at 9 06 16 PM](https://github.com/hasanabbas-blr/Microsoft-Future-Ready-Talent-Internship-Project-Hasans-Extractor/assets/150517265/cfc51d04-9227-41fb-8491-043a43fdc497)
---
- Then we go down and select the preferred language you want to translate.
- Once that is selected the **Azure AI Translator API** translates and displays the text below.
- **In this example I have chosen Hindi and Arabic:**
![Screenshot 2023-12-02 at 9 07 38 PM](https://github.com/hasanabbas-blr/Microsoft-Future-Ready-Talent-Internship-Project-Hasans-Extractor/assets/150517265/dd2c79a1-47d2-4833-8f69-8e0c56efe4bf)
![Screenshot 2023-12-02 at 9 08 20 PM](https://github.com/hasanabbas-blr/Microsoft-Future-Ready-Talent-Internship-Project-Hasans-Extractor/assets/150517265/c47e49cd-d52a-4fa5-80fb-3902ac2be5e7)

---


## Screenshots

![Screenshot 2023-12-02 at 9 09 34 PM](https://github.com/hasanabbas-blr/Microsoft-Future-Ready-Talent-Internship-Project-Hasans-Extractor/assets/150517265/0542c4c7-3393-4c4e-affb-d1ef48887ece)

![Screenshot 2023-12-02 at 9 09 44 PM](https://github.com/hasanabbas-blr/Microsoft-Future-Ready-Talent-Internship-Project-Hasans-Extractor/assets/150517265/a7d7c363-f308-40e7-94da-ae5e57447df9)




## **Account IDs**
**Git Hub ID:** hasanabbas-blr

**Azure Account ID:** hasanabbasofficial2@gmail.com

## **Acknowledgements**
My sincere thanks, to Microsoft for an impressive static web apps service on MS Azure Cloud to deploy my website easily. It was a wonderful experience learning this and would like to explore more in next years of my B.Tech. Sincere appreciation to Team of Future Ready Talent who supported and encouraged us to work on this project. 
