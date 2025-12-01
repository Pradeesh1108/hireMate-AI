# Docker Instructions for Backend

## Prerequisites
- Docker Desktop installed and running.

## Build the Image
Run this command from the `backend-python` directory:

```bash
docker build -t backend-python .
```

## Run the Container
Run the container mapping port 8000 and passing your environment variables:

```bash
docker run -p 8000:8000 --env-file .env backend-python
```

## Verify
Visit `http://localhost:8000/api/test` to verify the server is running.
