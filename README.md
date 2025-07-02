# React + Node.js Lambda Fullstack App (Deployed on AWS)

This is a simple fullstack serverless web application built using:

- 🔹 **React** frontend (hosted on AWS S3)
- 🔹 **Node.js (ES Module)** Lambda function backend (via API Gateway)
- 🔹 **Serverless architecture on AWS**

---

## 🚀 Live Demo

Frontend hosted on:  
🔗 [http://sahilok12345.s3-website-us-east-1.amazonaws.com](http://sahilok12345.s3-website-us-east-1.amazonaws.com)

API endpoint (example):  
🔗 `https://<your-api-id>.execute-api.us-east-1.amazonaws.com/helloLambda`

---

## 📁 Project Structure

react-lambda-app/
├── frontend/ # React app (S3 hosted)
│ └── .gitignore
│ └── src/
├── backend/ # AWS Lambda function (Node.js)
│ └── index.mjs
└── README.md


---

## 🛠 Tech Stack

- ⚛️ React (Create React App)
- 🟩 Node.js 18.x (ES Modules)
- 🧬 AWS Lambda
- 🌐 API Gateway
- 🗂️ S3 Static Hosting

---

## ⚙️ Lambda Function (`index.mjs`)

```js
export const handler = async (event) => {
  return {
    statusCode: 200,
    headers: {
      "Access-Control-Allow-Origin": "*"
    },
    body: JSON.stringify({ message: "Hello from Lambda ES Module!" })
  };
};



📦 Deployment Steps
🔹 Frontend
Build React app:
npm run build
Upload contents of build/ folder to your S3 bucket (e.g., sahilok12345)
Enable static website hosting

🔹 Backend
Zip the index.mjs file:
zip function.zip index.mjs
Upload to AWS Lambda
Create an API Gateway → Route /helloLambda → Integrate with Lambda
Add Lambda permissions to allow API Gateway access

🧠 Learnings
Serverless deployment using Lambda and S3
CORS handling between frontend and backend
Minimal fullstack project using AWS services only

📌 Author
Sahil Shakya
GitHub | LinkedIn
