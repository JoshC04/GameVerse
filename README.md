# GameVerse

GameVerse is a full-stack social platform where users can post to a feed, find and join groups, discover parties/events, and message each other in real time. Built as a 5-person capstone project over one semester (330+ commits).

**Stack:** React · Spring Boot · MongoDB · Railway (deployment)

## My Contribution

I configured and managed the deployment pipeline (Railway + MongoDB Atlas) and wrote the automated test suite, including unit tests and Selenium-based behavioral tests covering core user flows.

## Features

- Social feed with posts and interactions
- Group creation and membership
- Party/event finding
- Real-time messaging

## Getting Started

### Prerequisites
- [Node.js](https://nodejs.org/en/)
- [Java 17](https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html)
- [Maven](https://maven.apache.org/download.cgi)
- [MongoDB Compass](https://www.mongodb.com/products/compass) (for local database management)

### Setup
1. Clone the repo and install frontend dependencies:

git clone https://github.com/JoshC04/GameVerse.git

cd GameVerse/frontend

npm install

3. Install MongoDB Compass and connect to a local database on port `27017`.
4. Configure `application.properties` with your local database name and port.

### Running Locally
From the project root — starts the Spring Boot backend

mvn spring-boot:run

In a separate terminal — starts the React frontend

cd frontend
npm start

Once both are running, the app will be available at the localhost URL shown in your terminal.

## Deployment

GameVerse is deployed on Railway, with MongoDB Atlas as the production database.
1. Set up a database in MongoDB Atlas and get the connection string.
2. Deploy the backend on Railway (from GitHub), adding the Atlas connection string as an environment variable.
3. Deploy the frontend as a separate Railway project with root set to `/frontend`.

Railway auto-redeploys on every push to `main`.

## Testing

- Unit tests: `/GameVerse/test/java/com/GameVerse/GameVerse`
- Selenium behavioral tests: `/GameVerse/test/java/com/GameVerse/GameVerse/selenium`

Run with:

./mvnw test

(Make sure both the backend and frontend are running first, since Selenium drives the live app.)

## Team

- Alandis Patterson
- Gage Hulbert
- Joshua Cook
- Quintarius Floyd
- Jamius Cheatham
