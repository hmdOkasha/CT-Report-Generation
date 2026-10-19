# CT-Vision 🩻

CT-Vision is an automated system that diagnoses and detects abnormalities in chest CT-scans and generates a full structured medical report according to the scan. The system consists of a deep learning vision language model integrade inisde a user-friendly web application

## Deep Learning Model 🧠

The deep learning **vision language model** consists of 2 models connected together: a **vision transformer** that extracts **the visual embeddings** of the image, and an **LLM** that generates the medical report text according to the given **visual embeddings**. We created the model by following these steps:

1. 🛠️ **Adjusted the architecture** of google's vision transformer to accept 3D volumes instead of 2D images and fine-tuned it by training it on chest CT volumes
2. 🔁 Passed the visual embeddings through a **projection layer** to make it the same dimensions as text embeddings
3. 🔗 Passed the projected **visual embeddings** concatenated with a **text prompt** (Telling the LLM to generate a medical report) to **LLaMa LLM**
4. 🧾 **LLaMa** generates a **full medical report** according to the visual embeddings and the prompt

## Web App Features 🌐

The deep learning model that detects abnormalities in the scans and then generates a medical report is integrated inside a **user-friendly web applications** for doctors to use. The web app has multiple **features** such as:

1. 📤 **Reprot generation** on scan upload
2. ✏️ The report is **editable** so the doctor can edit it if there are mistakes
3. 📧 The report could be **sent to the patient by email**
4. 🧾 The doctor can **choose the template** of the report
5. ⚡ **PACS integration** so the scan will be processed and report generated immediately so the doctor won't be waiting for a long time
6. 📚 **Previous scans** with their corresponding reports are **saved and displayed in a page** so the doctor can access them whenever for future reference

## Technologies and Tools Used 🛠️

1. Python, pytorch, transformers
2. Kaggle, Google Colab, Huggingface
3. HTML, CSS, JS
4. ReactJS, TailwindCSS
5. NodeJS
6. MongoDB
7. Docker
8. Github, Postman, Figma
   
## Demo Video
**Click on the image to view video**

[![Watch the video](https://github.com/user-attachments/assets/96702942-1f38-479c-9c8c-43b3964628be)](https://drive.google.com/file/d/16IuY9drqwz0dCLMLqIbX5qE11ppc2851/view?usp=sharing)
