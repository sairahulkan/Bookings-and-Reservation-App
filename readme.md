# Hotel Booking and Reservation Web Application

This project is a comprehensive web application designed for hotel bookings and reservations. It features multiple HTML pages styled with Bootstrap and other CSS libraries and includes a robust backend built with Go. The project adheres to modern web application standards, emphasizing security and user session management.

## Features

- **HTML Pages**: 
  - `about.html`: Information about the hotel.
  - `index.html`: Main landing page with a carousel for showcasing images or promotions.
  - `contact.html`: Contact form for inquiries.
  - `generals.html` and `majors.html`: Detailed information about different room types.
- **Styling**: Utilizes Bootstrap and other CSS libraries for a responsive and modern design.
- **Navigation Bar**: Provides easy access to different sections like About, Contact, and Room Information.
- **Carousel**: Featured on the main page (`index.html`) for highlighting images or special promotions.

## Backend Features

- **Go Version 1.15**: Utilized for building the server-side component.
- **Chi Router**: For efficient routing.
- **Alex Edwards SCS**: Session management for handling user sessions.
- **Nosurf**: CSRF protection to ensure security.

## Technologies Used

- **Frontend**:
  - HTML
  - CSS (Bootstrap)
  - JavaScript
- **Backend**:
  - Go 1.15
  - Chi Router
  - Alex Edwards SCS for session management
  - Nosurf for CSRF protection
- **Containerization**: Docker
- **Orchestration**: Kubernetes
- **Cloud Services**: AWS
- **CI/CD**: GitHub Actions

## Getting Started

### Prerequisites

- Go 1.15+
- Docker
- Kubernetes (kubectl and a cluster)
- AWS CLI
- PostgreSQL
- Redis

### Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/your-username/hotel-booking.git
    cd hotel-booking
    ```

2. Set up the environment variables:

    Create a `.env` file and add the necessary configuration values.

    ```plaintext
    DB_SOURCE="postgresql://user:password@localhost:5432/hotelbooking?sslmode=disable"
    REDIS_ADDRESS="localhost:6379"
    JWT_SECRET="your_jwt_secret"
    PASETO_SECRET="your_paseto_secret"
    AWS_REGION="your_aws_region"
    ```

3. Run the application:

    ```bash
    go run src/main.go
    ```

## Deployment

### Docker

1. Build the Docker image:

    ```bash
    docker build -t hotel-booking .
    ```

2. Run the Docker container:

    ```bash
    docker run -p 8080:8080 --env-file .env hotel-booking
    ```

### Kubernetes

1. Apply the Kubernetes configurations:

    ```bash
    kubectl apply -f k8s/deployment.yaml
    kubectl apply -f k8s/service.yaml
    ```

2. Check the status of your pods:

    ```bash
    kubectl get pods
    ```

## CI/CD with GitHub Actions

This project uses GitHub Actions for continuous integration and continuous deployment. The configuration file is located at `.github/workflows/ci.yml`.

### Setting Up GitHub Actions

1. Create a `.github/workflows/ci.yml` file with your CI/CD pipeline configuration.
2. Ensure your repository secrets are set for AWS credentials, Docker Hub credentials, and any other required environment variables.

