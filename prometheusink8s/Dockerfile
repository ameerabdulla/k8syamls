# Use a base image that includes a minimal Linux distribution.
FROM alpine:latest

# Download and install Node Exporter.
RUN wget https://github.com/prometheus/node_exporter/releases/download/v1.6.1/node_exporter-1.6.1.linux-amd64.tar.gz && \
    tar xvfz node_exporter-1.6.1.linux-amd64.tar.gz && \
    mv node_exporter-1.6.1.linux-amd64/node_exporter /bin/ && \
    rm -rf node_exporter-1.6.1.linux-amd64 node_exporter-1.6.1.linux-amd64.tar.gz

# Expose the Node Exporter port.
EXPOSE 9100

# Start Node Exporter when the container is run.
ENTRYPOINT ["/bin/node_exporter"]





