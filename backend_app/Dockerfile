FROM python:3.9-slim

# Set the working directory inside the container
WORKDIR /app

# Copy only the requirements file first to leverage Docker cache
COPY requirements.txt .

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the application code
COPY . .

# Expose the port your Flask app will run on
EXPOSE 5000

# Use Gunicorn for production (recommended) instead of Flask's built-in server
CMD ["gunicorn", "-b", "0.0.0.0:5000", "app:app"]
