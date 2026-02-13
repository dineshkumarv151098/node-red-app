FROM nodered/node-red:latest

# Switch to root
USER root

# Copy package.json first
COPY package.json /data/package.json

# Install dependencies
RUN npm install --unsafe-perm --no-update-notifier --no-fund --only=production

# Copy flows
COPY flows.json /data/flows.json

USER node-red

EXPOSE 1880
