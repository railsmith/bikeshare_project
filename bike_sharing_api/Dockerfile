# Use a slim Python image as the base image
FROM python:3.12.1-slim

# Set the working directory inside the container
WORKDIR /bikeshare_api

# Copy the application code into the container
COPY . /bikeshare_api

# Install dependencies from requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# If you have a .whl file in your app directory, install it
RUN pip install --no-cache-dir bikeshare_model-0.0.1-py3-none-any.whl

# Expose port 8001 since your app is running on that port (as per your main.py code)
EXPOSE 8001

# Run FastAPI app with Uvicorn when the container starts
# Since the if __name__ == "__main__": block is in main.py, we'll directly run `python` with the file
CMD ["python", "app/main.py"]
