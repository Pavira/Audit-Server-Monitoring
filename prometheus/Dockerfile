# Use official Prometheus base image (stable & secure)
FROM prom/prometheus:v2.45.0

# Copy Prometheus main configuration file into the container
COPY prometheus.yml /etc/prometheus/prometheus.yml

# Copy alert rules file (CPU, disk, server down alerts)
COPY alert_rules.yml /etc/prometheus/alert_rules.yml

# Create directory for time-series data storage
RUN mkdir -p /prometheus

# Expose Prometheus UI port
EXPOSE 9090

# Start Prometheus with required arguments
CMD ["--config.file=/etc/prometheus/prometheus.yml", "--storage.tsdb.path=/prometheus"]

