FROM debian:jessie

ENV API_UMBRELLA_VERSION 0.14.2-1~jessie

# Install API Umbrella
RUN echo "deb http://dl.bintray.com/nrel/api-umbrella-debian jessie main" >> /etc/apt/sources.list.d/api-umbrella.list
RUN apt-get update && apt-get -y --allow-unauthenticated install api-umbrella

# Define mountable directories
VOLUME ["/etc/api-umbrella", "/opt/api-umbrella/var/db", "/opt/api-umbrella/var/log"]

# Expose HTTP and HTTPS ports
EXPOSE 80 443

# Run the API Umbrella service
CMD ["api-umbrella", "run"]
