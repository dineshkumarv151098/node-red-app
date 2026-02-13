FROM nodered/node-red:latest

USER root

# Set working directory explicitly
WORKDIR /data

# Copy only package files first
COPY package.json package-lock.json* ./

# Install dependencies into /data/node_modules
RUN npm install --unsafe-perm --no-update-notifier --no-fund --only=production

# Copy flows
COPY flows.json flows_cred.json* ./

USER node-red

EXPOSE 1880
