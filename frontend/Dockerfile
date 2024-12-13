<<<<<<< HEAD
FROM nginx:alpine

COPY ./frontend /usr/share/nginx/html
=======
FROM ubuntu:latest

# Update and install nginx
RUN apt-get update && \
    apt-get install -y nginx

# Copy your custom nginx.conf file
COPY nginx.conf /etc/nginx/nginx.conf

# Copy the frontend files (e.g., HTML, CSS, JS) to the Nginx web directory
COPY . /usr/share/nginx/html

# Expose port 80 for HTTP traffic
EXPOSE 80

# Run nginx in the foreground (required for Docker container)
CMD ["nginx", "-g", "daemon off;"]
>>>>>>> 17653bf (commiting)
