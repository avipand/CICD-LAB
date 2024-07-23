# Use the official Jenkins LTS image
FROM jenkins/jenkins:lts

# Switch to root user to install plugins
USER root

# Copy plugins.txt file into the container
COPY plugins.txt /usr/share/jenkins/ref/plugins.txt

# Install Jenkins plugins
RUN jenkins-plugin-cli --plugin-file /usr/share/jenkins/ref/plugins.txt

# Expose port 8080 for Jenkins web interface
EXPOSE 8080

# Expose port 50000 for Jenkins agent
EXPOSE 50000

# Switch back to the Jenkins user
USER jenkins

# Start Jenkins
CMD ["java", "-jar", "/usr/share/jenkins/jenkins.war"]
