# 🎙️ Story Narrator - Text to Speech using AWS

A serverless **Text-to-Speech** web application built using **AWS Lambda, Amazon Polly, Amazon S3, DynamoDB, API Gateway, HTML, CSS, and JavaScript**.

Users can upload a `.txt` file or write a story directly in the browser. The application converts the text into natural speech using Amazon Polly, stores the generated MP3 file in Amazon S3, saves metadata in DynamoDB, and displays the narrated stories with an audio player.

---

# 🚀 Features

- Upload `.txt` files
- Write stories directly in the browser
- Convert text to speech using Amazon Polly
- Store generated audio in Amazon S3
- Save narration metadata in DynamoDB
- Display previously narrated stories
- Built using AWS Serverless Architecture
- Responsive Web Interface

---

# 🏗️ Architecture

```
                User
                  │
                  ▼
         HTML / CSS / JavaScript
                  │
                  ▼
            API Gateway
             /         \
            ▼           ▼
     TextToSpeech    GetAudioFiles
         Lambda          Lambda
            │               │
            ▼               ▼
       Amazon Polly     DynamoDB
            │               ▲
            ▼               │
          Amazon S3 ─────────
```

---

# ⚙️ AWS Services Used

| Service | Purpose |
|----------|----------|
| Amazon S3 | Store uploaded text files and generated audio |
| AWS Lambda | Process uploaded text and generate speech |
| Amazon Polly | Convert text into natural speech |
| DynamoDB | Store narration metadata |
| API Gateway | Expose REST APIs |
| CloudWatch | Logging and Monitoring |

---

# 📂 Project Structure

```
.
├── index.html
├── style.css
├── script.js
├── README.md
└── images/
```

---

# 🔄 Workflow

### Step 1

User uploads a text file or writes a story.

↓

### Step 2

The request is sent to API Gateway.

↓

### Step 3

API Gateway invokes the **TextToSpeech Lambda**.

↓

### Step 4

Lambda uploads the text file to Amazon S3.

↓

### Step 5

Lambda reads the uploaded text.

↓

### Step 6

Amazon Polly converts the text into speech.

↓

### Step 7

The generated MP3 is stored inside Amazon S3.

↓

### Step 8

Metadata is stored in Amazon DynamoDB.

↓

### Step 9

The website calls **GetAudioFiles Lambda**.

↓

### Step 10

Previously generated narrations are displayed with an audio player.

---

# 📸 Screenshots

## Amazon S3 Bucket

<img width="1530" height="492" alt="Screenshot 2026-07-17 104133" src="https://github.com/user-attachments/assets/dcc9b405-f25a-4e54-a4ab-dd4a4331ce87" />


---

## Project Fils

<img width="597" height="631" alt="Screenshot 2026-07-17 104143" src="https://github.com/user-attachments/assets/4a9ea236-af41-430b-aa97-166703405671" />


---

## AWS Lambda Configuration

<img width="1900" height="815" alt="Screenshot 2026-07-17 104159" src="https://github.com/user-attachments/assets/e33dbf3a-ee5b-4a7e-ab97-0580c7db4bf2" />


---

## API Gateway Routes

<img width="1867" height="657" alt="Screenshot 2026-07-17 104231" src="https://github.com/user-attachments/assets/4b9e1cf2-a857-4cc4-a395-808730972f8b" />


---

## Home Page

<img width="1716" height="855" alt="Screenshot 2026-07-17 104304" src="https://github.com/user-attachments/assets/fd368d9f-42f7-4392-8bc3-d974f3f66912" />


---

## Narrated Stories audio

<img width="1712" height="656" alt="Screenshot 2026-07-17 104317" src="https://github.com/user-attachments/assets/7abe4997-79f7-4ff0-aa99-52edee960114" />


---

# 🛠️ Technologies Used

- HTML5
- CSS3
- JavaScript
- AWS Lambda
- Amazon Polly
- Amazon S3
- Amazon DynamoDB
- API Gateway
- CloudWatch

---

# API Endpoints

## Upload Story

```
POST /upload
```

Uploads a text file or story for narration.

---

## Get Narrated Stories

```
GET /audio
```

Returns all narrated stories stored in DynamoDB.

---

# Future Improvements

- Voice selection
- Multiple language support
- Delete narration
- Download generated MP3
- User authentication
- Search and filter narrations

---

# Author

**Yash Patil**

AWS | Full Stack Developer | AI & ML Student

---
