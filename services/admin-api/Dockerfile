# Base Python image
FROM python:3.10-slim

# Set working directory
WORKDIR /app

# Copy application code and requirements
COPY ./services/admin-api/requirements.txt /app/
COPY ./services/admin-api/app /app/app

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Expose port - Use a different port than bot-manager (8080)
EXPOSE 8001

# Command to run the application
CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8001"]
