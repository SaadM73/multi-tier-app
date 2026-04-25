# Use official Nginx image as base
FROM nginx:alpine
# Remove default nginx content
RUN rm -rf /usr/share/nginx/html/*
# Copy our HTML files into nginx’s serving directory
COPY src/ /usr/share/nginx/html/
# Copy custom nginx configuration
COPY nginx.conf /etc/nginx/conf.d/default.conf
# Expose port 80 (nginx default)
EXPOSE 80
# Nginx starts automatically--- no CMD needed
