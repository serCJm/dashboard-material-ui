# Use Node.js 18 image
FROM node:18

# Update and install packages
RUN apt update && \
    apt upgrade -y && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

# Set the working directory
WORKDIR /usr/src/app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install project dependencies
RUN npm install

# Copy the rest of the code
COPY . .

# Keep the container running
CMD ["tail", "-f", "/dev/null"]