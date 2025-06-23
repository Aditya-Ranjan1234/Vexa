# Base Python image
FROM python:3.10-slim

# Set working directory
WORKDIR /app

COPY ./services/transcription-collector/requirements.txt /app/
COPY ./services/transcription-collector/ /app/

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Expose port (internal only, but good practice)
EXPOSE 8000

# Command to run the application
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"] 