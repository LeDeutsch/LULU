FROM nginx:alpine

# Copy website files to nginx default public folder
COPY . /usr/share/nginx/html

# Expose port 80 (nginx default)
EXPOSE 80

# Use the default nginx startup command
CMD ["nginx", "-g", "daemon off;"] 