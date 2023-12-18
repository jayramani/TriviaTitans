# TriviaTitans: A Serverless multi-cloud online trivia game

## Getting Started

### **Description:**

Trivia Titans is a multi-cloud serverless online trivia game that allows users to form teams, compete against other teams in real-time, and track their progress on global and category-specific leaderboard.

The primary goal of this project is to comprehend and implement a microservices architecture. Each microservice is created using either AWS or GCP services. The front end is exclusively deployed on GCP Cloud Run, while the backend services operate as Google Cloud Functions or AWS Lambda functions.

### **Prerequisites:**

Before using this project, you'll need to have the following installed:

- Node version 18.0 or higher 
- Mongo version 6.0 or higher
- A text editor (Visual Studio Code, Atom, Sublime Text, etc.)
- Git
- npm version 8.0 or higher


### **Installation:**

To install this project, follow these steps:

1. Clone the repository: git clone https://github.com/jayramani/StaySpot.git
2. Navigate to the backend directory: cd StaySpot/backend
3. Install the backend dependencies: npm install
4. Start the server: npm start
5. Navigate to the frontend directory: cd StaySpot/frontend
6. Install the frontend dependencies: npm install
7. Navigate back to the project directory: npm start

### **Environment Variables:**

This project requires the following environment variables to be set:

- MONGO_URI=<MONGO_CONNECTION_STRING>
- SECRET=<JWT_SECRET>
- REGION=<AWS_REGION>
- ACCESS_KEY_ID=<AWS_ACCESS_KEY>
- SECRET_ACCESS_KEY=<AWS_SECRET_ACCESS_KEY>
- SESSION_TOKEN=<AWS_SESSION_TOKEN><!-- Optional -->


### **Application Architecture**

![Final Architecture Diagram](https://github.com/jayramani/TriviaTitans/assets/37774914/2ad060a8-a6fe-441d-818e-6bd3f665f339)

### **Application Flow Diagram**
![Flow_diag](https://github.com/jayramani/TriviaTitans/assets/37774914/f62c0bf3-07fb-4f54-b5ad-295ee318f289)


### **AWS Services Used**

| Service | Purpose |
| --- | --- |
| `AWS Cognito` | To authenticate and authorize the users|
| `Lambda` | To configure serverless architecture that runs backend APIs |
| `DynamoDB` | To store the user data and team data  |
| `API Gateway` | To create an API that takes the data from the front end and puts it on AWS SQS  |
| `SQS` | To hold the payload from the API Gateway that will trigger the lambda  |
| `SNS` | To send an email notification to users |
| `AWS Lex` | To implement the chatbot that helps users with navigation, ranking, and scores  |


### **GCP Services Used**

| Service | Purpose |
| --- | --- |
| `Cloud function` | To host the APIs for 2-factor authentication |
| `Cloud Run` | To deploy and run the front end of an application |
| `Firestore` | To store the user login question answer |
| `Big Query` | To store the score and rankings that can be used for analysis  |
| `Looker Studio` | To show the leaderboard for teams and users |

