# Codin 1 Website - Dockerized

This project demonstrates a basic React app that displays an `<h1>` tag with the text "Codin 1". The project is dockerized to ensure consistent development and production environments. This README will guide you through setting up the development environment using Docker.

## Prerequisites

Make sure you have the following installed on your machine:
- [Docker](https://www.docker.com/get-started)
- A web browser to access the application

## Getting Started

Follow the steps below to set up and run the application in a Docker container.

### 1. Clone the Repository

If you're working with this code locally, clone the repository or download the project files.

```bash
git clone git@github.com:simarjotsingh2/Singh_simarjot_Projectsite.git
cd Singh_simarjot_Projectsite
```

### 2. Build the Docker Image

In the project directory (where the `Dockerfile` is located), build the Docker image using the following command:

```bash
docker build -t Singh_simarjot_coding_assignment11 .
```

This command will create a Docker image named `Singh_simarjot_coding_assignment11`.

### 3. Run the Docker Container

Once the image is built, you can run the container using the following command:

```bash
docker run -p 7775:7775 Singh_simarjot_coding_assignment11
```

This command maps port `7775` of your local machine to port `7775` of the Docker container.

### 4. Access the Application

Open your web browser and go to `http://localhost:7775` (or `127.0.0.1:7775`). You should see the web page displaying "Codin 1" as an `<h1>` tag.

### 5. Stop the Docker Container

To stop the container, press `CTRL + C` in the terminal where the container is running.

Alternatively, you can list and stop the container using:

```bash
docker ps    # Lists running containers
docker stop Singh_simarjot_coding_assignment11
```

## Project Structure

```plaintext
├── public/
├── src/
│   └── App.js          # Displays the "Codin 1" text
├── Dockerfile          # Docker configuration file
├── package.json        # Project configuration and dependencies
└── README.md           # Project instructions (this file)
```

## Dockerfile Overview

- **Base Image**: Uses `node:16-alpine` for lightweight Node.js.
- **Working Directory**: `/Singh_simarjot_Projectsite`.
- **Ports**: Exposes port `7775` for local development.
- **Command**: Runs `npm start` to start the React app.

## Troubleshooting

- If you can't access `http://localhost:7775`, make sure Docker is running and check if the container is properly started.
- If you encounter issues, you can rebuild the image by running `docker build` again.