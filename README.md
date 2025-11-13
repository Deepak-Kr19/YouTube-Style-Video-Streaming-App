📺 YouTube-Style Video Streaming App (Flutter + AWS + FastAPI + Microservices)

A full-stack, production-grade video streaming platform built using Flutter for the frontend and a microservices-based backend powered by FastAPI, Docker, PostgreSQL, AWS, and FFmpeg.
Supports video upload, transcoding, HLS/DASH adaptive bitrate streaming, user authentication, CDN distribution, and secure state management — just like YouTube.

🚀 Features
🔐 Authentication

AWS Cognito User Pools

Signup, Login, Logout

HMAC-SHA256 Secret Hash

Access Token + Refresh Token

Secure session management using HTTP-only cookies

Persistent authentication using Flutter Secure Storage

🎥 Video Uploading

Upload videos and thumbnails using AWS S3 Pre-Signed URLs

Video metadata stored in PostgreSQL

Error handling for large uploads

Thumbnail preview + validation

🛠 Video Processing Pipeline

Dockerized microservice to poll AWS SQS

FFmpeg for:

Transcoding

Segmentation

Adaptive Bitrate Streaming (ABR)

Output formats:

HLS (.m3u8)

MPEG-DASH

Automatic status updates stored in DB

⚡ Streaming & Delivery

Player supports DASH adaptive streaming

CDN caching with AWS CloudFront

Low-latency global delivery

Secure media URLs

📱 Flutter Frontend

Beautiful UI built with Material 3

Screens:

Login / Signup

Confirm Signup

Home Feed

Upload Page

Video Player Page

State Management using Cubit (Bloc)

API integration + error handling

Token refresh + secure persistence

💾 Backend

FastAPI REST APIs

PostgreSQL + SQLAlchemy ORM

Docker Compose for DB, Backend, Processor

ECS + ECR for scalable deployment

🧰 Tech Stack
Frontend

Flutter

Dart

Cubit (Bloc)

Flutter Secure Storage

Video Player (DASH Support)

Backend

FastAPI

Python

SQLAlchemy

PostgreSQL

Docker

Docker Compose

Cloud / DevOps

AWS Cognito

AWS S3

AWS SQS

AWS CloudFront

AWS ECS

AWS ECR

FFmpeg

Ngrok (for tunneling during testing)

🏗 Architecture Overview
Flutter App 
    ↓
FastAPI Backend (Auth + Video Metadata)
    ↓
AWS S3 (Uploads via Pre-Signed URL)
    ↓
AWS SQS (Upload notifications)
    ↓
Dockerized Processor (FFmpeg)
    ↓
AWS S3 (HLS/DASH segments)
    ↓
AWS CloudFront CDN
    ↓
Flutter Video Player


This pipeline supports scalable, fault-tolerant video streaming, just like large platforms (YouTube, Vimeo, Hotstar, etc.).

📸 Screenshots (Add Your Images Here)
assets/
 ├── login.png
 ├── signup.png
 ├── home_feed.png
 ├── upload.png
 └── video_player.png

🧪 How to Run
Frontend
flutter pub get
flutter run

Backend (Local)
docker-compose up --build

Environment Variables

Create a .env file:

AWS_ACCESS_KEY_ID=your_key
AWS_SECRET_ACCESS_KEY=your_secret
AWS_REGION=ap-south-1
COGNITO_CLIENT_ID=xxxx
COGNITO_USER_POOL_ID=xxxx
DATABASE_URL=postgresql://user:password@db:5432/app

🔥 Key Highlights

Production-grade architecture

Secure authentication & token lifecycle

ABR streaming using HLS/DASH

Cloud-native infrastructure

Real-time video pipeline

Scalable & maintainable codebase

🧑‍💻 Future Improvements

Comments, likes, subscriptions

Video recommendations (ML-based)

Creator dashboard

Analytics dashboard

Multi-quality manual switching

🙌 Author

Deepak Kumar
Flutter Developer | Full-Stack Learner
GitHub: add your link
LinkedIn: add your link
