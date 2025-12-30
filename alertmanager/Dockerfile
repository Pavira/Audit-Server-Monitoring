FROM prom/alertmanager:v0.27.0

# Copy Alertmanager config
COPY alertmanager.yml /etc/alertmanager/alertmanager.yml

EXPOSE 9093

CMD ["--config.file=/etc/alertmanager/alertmanager.yml"]
