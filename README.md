🚀 Serverless File Upload System (AWS SAM)

📌 Project Overview

This project is a serverless file upload and download system built using AWS services and Infrastructure as Code (IaC).

It allows users to:

- Generate a secure upload URL
- Upload files directly to Amazon S3
- Generate a secure download URL

All resources are provisioned and managed using AWS SAM (Serverless Application Model).

---

🧠 Architecture

Client → API Gateway → Lambda → S3

Flow:

1. Client requests "/upload-url"
2. Lambda generates a pre-signed S3 upload URL
3. Client uploads file directly to S3
4. Client requests "/download-url?fileName=..."
5. Lambda returns a pre-signed download URL

---

⚙️ Technologies Used

- AWS Lambda
- API Gateway
- Amazon S3
- AWS SAM (Infrastructure as Code)
- Python (boto3)

---

📂 Project Structure

serverless-sam-project/
├── hello_world/
│   └── app.py
├── template.yaml
└── README.md

---

🔥 Key Features

- ✅ Secure file upload using pre-signed URLs
- ✅ Secure file download access
- ✅ Fully serverless architecture
- ✅ Infrastructure defined as code (SAM)
- ✅ IAM permissions managed securely
- ✅ Easily deployable with one command

---

🚀 Deployment

This project uses AWS SAM for deployment.

Deploy:

sam deploy

---

🧪 API Endpoints

🔹 Generate Upload URL

GET /upload-url

Response:

{
  "uploadUrl": "...",
  "fileName": "..."
}

---

🔹 Generate Download URL

GET /download-url?fileName=your-file-id

Response:

{
  "downloadUrl": "..."
}

---

🧠 What I Learned

- How to build serverless applications using AWS
- How API Gateway integrates with Lambda
- How to securely upload/download files using S3 pre-signed URLs
- How to use Infrastructure as Code (AWS SAM)
- Debugging real-world issues:
  - API Gateway path differences (REST vs HTTP API)
  - IAM policy errors
  - CloudFormation deployment failures

---

💡 Why This Project Matters

This project demonstrates:

- Real-world backend system design
- Cloud architecture understanding
- DevOps practices using Infrastructure as Code
- Ability to debug and fix production-level issues

---

📌 Future Improvements

- Add authentication (JWT / Cognito)
- Add file type validation
- Add logging dashboard & monitoring
- Add frontend interface

---

👨‍💻 Author

Jolomi Ayu
