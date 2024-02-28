# WatMart - A Shopping Platform for University of Waterloo Students

## Overview

WatMart is an online shopping platform specifically designed for students at the University of Waterloo. It provides a convenient and user-friendly way for students to buy and sell products online. Built using Django, WatMart ensures a robust and scalable service.

## Features

- User-friendly interface for buying and selling goods.
- Secure login and user authentication system.
- Integration with MySQL for database management.
- Redis for caching and session storage.
- SMTP server for email notifications.
- Celery for task queue management.
- Flower for real-time monitoring of Celery tasks.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

To run this project, you need to have Docker and Docker Compose installed on your system. If you don't have Docker installed, follow the instructions here: [Install Docker](https://docs.docker.com/get-docker/).

### Installation

1. **Clone the repository**

git clone [your-repo-link]
cd [your-repo-name]


2. **Setup Environment**

Before starting the service, ensure you have set up the necessary environment variables. Modify the `MYSQL_ROOT_PASSWORD` in the `docker-compose.yml` file as per your security requirements.

3. **Build and Run with Docker Compose**

docker-compose up --build


This command builds the Docker images and starts the services defined in your `docker-compose.yml` file.

### Accessing the Application

- The Django application will be accessible at `http://localhost:8000`.
- MySQL is accessible on port `3306`.
- Redis is running on port `6379`.
- SMTP server is available on port `25` and the web interface on `5001`.
- Access Flower for Celery task monitoring on `http://localhost:5555`.

## Usage

After starting the services, you can use the Django application to manage products, users, and orders. The Celery workers handle background tasks like sending emails and processing data.

## Testing

For running tests, use the `tests` service defined in the Docker Compose file.

docker-compose run tests