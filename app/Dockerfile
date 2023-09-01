FROM php:7.2-fpm-alpine

RUN docker-php-ext-install -j$(nproc) mysqli opcache

ADD php.ini /usr/local/etc/php.ini 

LABEL maintainer="Kinsta devs"

# Set the working directory to /app
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app

# Install any needed packages specified in package.json
RUN npm install

# Run app when the container launches
CMD ["npm", "start"]
