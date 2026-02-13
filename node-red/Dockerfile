FROM nodered/node-red:3.1.0

USER root

# Install dependencies directly into /data without changing WORKDIR
COPY package.json /data/package.json
COPY package-lock.json* /data/

RUN cd /data && \
    npm install --unsafe-perm --no-update-notifier --no-fund --only=production

# Copy flows
COPY flows.json /data/flows.json
COPY flows_cred.json /data/flows_cred.json

USER node-red

EXPOSE 1880
