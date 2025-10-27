# 🌐 Static Website Hosting on AWS S3

## 📖 Project Overview
This project demonstrates how to deploy a **static website** using **Amazon S3**.  
The website contains HTML, CSS, and JavaScript files and is fully hosted on the AWS cloud infrastructure.  
It showcases basic cloud deployment concepts suitable for beginners in **Cloud Computing** and **DevOps**.

---

## 🚀 Features
- Hosted a static website using **AWS S3**
- Configured **public access permissions**
- Set up **index.html** and custom error page
- Implemented **bucket policy** for secure object access
- (Optional) Integrated **AWS CloudFront** for CDN and **Route 53** for custom domain

---

## 🧰 Technologies Used
- **Amazon S3** – Static website hosting  
- **HTML, CSS, JavaScript** – Frontend files  
- **AWS Management Console** – Configuration and management  
- **IAM & Bucket Policy** – Access control  

---

## ⚙️ Setup and Deployment Steps

### 1. Create S3 Bucket
1. Go to AWS Management Console → S3  
2. Click **“Create bucket”**  
3. Enter a **unique bucket name**  
4. Uncheck **“Block all public access”** and confirm  

### 2. Upload Website Files
- Upload `index.html`, `style.css`, and `script.js` to the bucket root.

### 3. Enable Static Website Hosting
1. Go to **Properties → Static website hosting**  
2. Enable hosting  
3. Enter:  
   - **Index document:** `index.html`  
   - **Error document:** `error.html` *(optional)*

### 4. Set Bucket Policy
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::my-static-website7598/*"
    }
  ]
}

5. Access the Website

Copy the endpoint URL from the static hosting section, e.g.

http://my-static-website7598.s3-website-ap-south-1.amazonaws.com


Open it in your browser to view your live website 

PROJECT OUTPUT

The website displays a welcome message.

A clickable button that shows “You clicked the button

Styled using CSS and deployed on AWS S3.

🧩 Folder Structure
my-static-website/
├── index.html
├── style.css
└── script.js

 Learning Outcome

Hands-on experience with AWS S3 static website hosting

Understanding of bucket policies, public access, and content delivery

Improved knowledge of cloud deployment workflows

 Author

Cloud & DevOps Enthusiast
📧 Email: boobalank18@gmail.com
🔗 LinkedIn: linkedin.com/in/boobalan-k-81a00b289
