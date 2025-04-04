# NestJS Docker Application

This is a NestJS application running in Docker with MySQL database.

## Prerequisites

- Docker
- Docker Compose

## Environment Variables

Create a `.env` file in the root directory with the following variables:

```env
DB_USERNAME=nestjs
DB_PASSWORD=nestjs_password
DB_NAME=nestjs_db
DB_ROOT_PASSWORD=root_password
```

## Running the Application

1. Install dependencies:
```bash
npm install
```

2. Start the application using Docker Compose:
```bash
docker-compose up --build
```

The application will be available at `http://localhost:3000`.

## Development

- The application runs in development mode with hot-reload enabled
- MySQL data is persisted in a Docker volume
- The API service is configured to restart automatically when code changes are detected

## Production

For production deployment:
1. Set `synchronize: false` in the TypeORM configuration
2. Build and run the containers:
```bash
docker-compose -f docker-compose.yml up --build
```

## API Documentation

The API documentation will be available at `http://localhost:3000/api` when the application is running. 