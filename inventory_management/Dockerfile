# Use Python slim-buster image, which is a lightweight version of Python
FROM python:slim-buster

# Set the working directory inside the container to /app
WORKDIR /app

# Copy the contents of the `app` directory on the host machine into `/app` in the container
COPY ./app/. ./

# Copy the requirements file into the container
COPY requirements.txt ./

# Install Python dependencies listed in the requirements file
RUN pip install --no-cache-dir -r requirements.txt

# Command to run the FastAPI app using Uvicorn, which will listen on any host without defining a port in the Dockerfile
CMD ["uvicorn", "main:app", "--host", "0.0.0.0"]
